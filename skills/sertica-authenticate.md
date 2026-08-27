---
name: Authenticate against a SERTICA site
description: Exchange a SERTICA user login for a 24-hour JWT and discover what that user is actually allowed to do before calling anything else.
api: openapi/sertica-web-api-openapi.json
operations:
  - CreateJwtToken
  - AuthIntegrations
---

# Authenticate against a SERTICA site

Every SERTICA deployment is a separate customer site. There is no shared host: the base URL
is `https://<sitename>.sertica.com/api`, where `<sitename>` is the customer's own site. Ask
for it — never guess it. The vendor's public API browser at `https://docs.sertica.com/api`
is for reading the contract, not for calling a customer's data.

## 1. Get a token

`CreateJwtToken` — `POST /Auth`

```json
{ "login": "<user>", "password": "<password>" }
```

The response carries `accessToken`. Send it on every subsequent request:

```
Authorization: Bearer <accessToken>
Content-Type: application/json; charset=utf-8
```

The token is reusable until it expires. The provider-documented default lifetime is
**24 hours**, so a long-running integration must re-authenticate rather than cache forever.
An expired or missing token returns **401** with the description `If user is unauthorized`.

## 2. Find out what this user can do — before you act, not after

This is the step most integrations skip, and it is the reason they see 403s. A SERTICA
request is bound to a user, and that user sees only the data and operations its rights
allow. 3,028 of the 3,340 operations declare a 403 whose description names the exact User
Right key required, for example `ChangeRequest / View`.

Three read-only calls tell you the shape of what you are working with:

- `GET /Auth/userRights` — the rights this user actually holds
- `GET /Auth/units` — the tree of Units (vessels/organisational units) this user can reach
- `GET /Auth` — the current user record

Treat the Unit tree as your tenancy boundary. A record number is unique inside a site, and
visibility follows the Unit, so a 404 can mean "outside your units" rather than "does not
exist".

`AuthIntegrations` — `GET /Auth/integrations` — returns the external authentication
integrations configured on that site. The set is site-specific; do not assume SSO.

## 3. Two-factor

Sites can require TOTP (added in release 5.15.89, November 2025). The setup operations are
`SetupTotp`, `ConfirmTotpSetup`, `GenerateRecoveryCodes` and `DisableTotp`. An unattended
integration user should be provisioned by the site administrator with this in mind.

## Rules

- Create a dedicated interface user with the minimum rights the integration needs. The
  provider's own example says so explicitly.
- Never send credentials on any host other than the customer's own `<sitename>.sertica.com`.
- There are no API keys, no OAuth scopes, and no client credentials flow. Login + password
  in exchange for a JWT is the only documented mechanism.

## Errors

| Status | Meaning | What to do |
|---|---|---|
| 400 | Invalid data — body is a `ValidationResult` | Read `errors[].fieldName` and `errors[].text` |
| 401 | Token missing, expired or invalid | Re-issue with `POST /Auth` |
| 403 | User lacks permission | Read the required right from the operation's 403 description; check `GET /Auth/userRights` |
| 500 | Unhandled error | Not retryable by you — escalate to the site administrator |
