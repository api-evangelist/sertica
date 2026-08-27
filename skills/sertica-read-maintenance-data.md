---
name: Read maintenance data from SERTICA
description: Search and read components, jobs and job history using SERTICA's searchInfo/search pattern instead of guessing query parameters.
api: openapi/sertica-web-api-openapi.json
operations:
  - GetComponents
  - GetComponent
  - SearchComponents
  - SearchInfoComponents
  - GetJobs
  - GetJob
  - AdvancedSearchJobs
  - JobSearchInfo
  - SearchCountJobs
  - GetHistoryForJob
  - GetJobItems
  - GetJobResources
  - SearchJobHistories
---

# Read maintenance data from SERTICA

Authenticate first — see `sertica-authenticate.md`. Base URL is
`https://<sitename>.sertica.com/api`.

## The pattern that matters

SERTICA does not filter with query strings. Almost every resource ships a four-operation
search family, and the one an agent should call **first** is `searchInfo`:

| Operation | Method | What it gives you |
|---|---|---|
| `SearchInfoComponents` | `GET /Components/searchInfo` | Structured information about what and how you can search for |
| `SearchComponents` | `POST /Components/search` | Results, given a `SearchDefinition` body with filters and sorting |
| `SearchCountComponents` | `POST /Components/searchCount` | Number of hits for the same body |
| `SearchIndexComponents` | `POST /Components/searchIndex/{componentGuid}` | Position of one record inside that result set |

Jobs follow the same shape under different names: `JobSearchInfo` (`GET /Jobs/searchInfo`),
`AdvancedSearchJobs` (`POST /Jobs/search`), `SearchCountJobs`, `SearchIndexJobs`. There is
also a simple keyword form, `SearchJobs` (`GET /Jobs/search/{keyword}`).

Read `searchInfo` before building a query. It is the site's own filter vocabulary, and
because customers can add their own fields (see below) it is not the same on every site.

## Paging

List and search responses are paged with `page` and `pageSize` query parameters. The
documented default page size is **25**; the provider's example passes `?pageSize=50`. No
maximum is documented. Count with `searchCount` before walking a large result set.

## The core reads

- `GetComponents` — `GET /Components` — the equipment register, paged.
- `GetComponent` — `GET /Components/{componentNo}` — one component by its number.
- `GetJobs` — `GET /Jobs` — maintenance jobs, paged.
- `GetJob` — `GET /Jobs/{jobNo}` — one job.
- `GetHistoryForJob` — `GET /Jobs/{jobNo}/history` — what has actually been done.
- `GetJobItems` / `GetJobResources` / `GetJobProcedures` — the parts, people and procedures
  attached to a job.
- `SearchJobHistories` — `POST /JobHistories/search` — completed work across the fleet.

Job history records are addressed by GUID (`jobhistoryGuid`), while most other entities are
addressed by their business number (`componentNo`, `jobNo`, `itemNo`). Both are typed as
strings in the path.

## Customer-defined fields

Components, Jobs, Items, Documents, LogbookEvents and PurchaseOrders each expose a
`propertyDefinitions` family — for jobs, `GetJobPropertyDefinitions`
(`GET /Jobs/propertyDefinitions`) and `GetJobPropertyDefinitionListValues`. A site can add
its own fields, so do not hard-code a field list. Read the property definitions for the
resource before mapping data.

## What you will not get

No response examples are published for any operation, and there are no rate-limit headers
to pace against. Read conservatively, page properly, and reconcile by reading records back.
