---
name: Record a counter reading in SERTICA
description: Post running-hours or meter readings that drive SERTICA maintenance planning, with the domain preconditions and the retry hazard stated up front.
api: openapi/sertica-web-api-openapi.json
operations:
  - GetCounters
  - GetCounter
  - GetReadings
  - AddCounterReading
  - GetReadingsGraphData
---

# Record a counter reading in SERTICA

This is the most commonly automated write in SERTICA: an external system (SCADA, an IoT
sensor, an ERP) already knows a running-hours value, and SERTICA needs it in order to plan
maintenance. The provider documents this flow itself.

Authenticate first — see `sertica-authenticate.md`.

## Before you write

**This operation is not idempotent and it cannot be undone.** SERTICA declares no
`Idempotency-Key` header anywhere in its 3,340-operation contract, and there is no
delete-reading operation. If you retry after a timeout you may create a second reading.

The only protection is a domain rule, and it is worth relying on deliberately:

- the new reading's date must be **later** than the last reading, and
- the new value must be **higher** than the last reading.

So read the current state first.

1. `GetCounters` — `GET /Counters` — find the counter. Or search with
   `SearchCounters` (`POST /Counters/search`) after reading `SearchInfoCounters`.
2. `GetReadings` — `GET /Counters/{counterNo}/readings` — the existing series. Take the
   latest date and value.
3. Only write if your value and date are strictly ahead of it.

## Write the reading

`AddCounterReading` — `POST /Counters/{counterNo}/readings`

```json
{ "value": 12345, "valuedate": "2026-08-27" }
```

`valuedate` is `yyyy-mm-dd`. A success returns **200**.

The provider's published PowerShell example:

```powershell
$postParamsCounter = @{"value"=<value>; "valuedate"="<date>"} | ConvertTo-Json;
Invoke-WebRequest -Uri https://<sitename>.sertica.com/api/counters/<no>/readings `
  -Method POST -Body $postParamsCounter -Headers $headers;
```

There is a second operation, `ForceAddCounterReading`
(`POST /Counters/{counterNo}/readings/force`), which bypasses the ordering rule. **Do not
call it from an agent.** It removes the only guard standing between a bad sensor value and
a corrupted maintenance schedule; leave it to a human who has looked at the series.

## Handling failures

A **400** returns a `ValidationResult`. Read `errors[].text` and `errors[].fieldName` —
that is where the reason lives ("value must be higher than last reading", a malformed date,
a counter that does not exist). Do not blind-retry a 400; the same body will fail again.

A **403** means the interface user does not hold the right to update this counter. Check
`GET /Auth/userRights`.

A **500** is unhandled server-side; the published guidance is to inspect the SERTICA logs on
that site. Do not retry in a loop.

## Verify

Read `GetReadings` back after the write, or `GetReadingsGraphData`
(`GET /Counters/{counterNo}/readings/graph/{daysToCover}`) for a trend. Because the write is
not idempotent, reading back is how you confirm — not a retry.
