# Verified BambooHR rules

Read 2026-10-11. Official documentation pages below loaded during this build. These are retrieval dates, not future verification or a promised submission date. The pages identify current replacements where older routes are deprecated. Reopen these URLs before the planned 2026-10-17 submission and refresh changed rules. No retirement date was supplied for the legacy route.

## Legacy report population and serialization

https://documentation.bamboohr.com/reference/request-custom-report

Read 2026-10-11; page marked deprecated, displayed “Updated 5 months ago.” All-status population differs from UI active default. `onlyCurrent` controls historical values. Maximum 400 requested fields; unknown/unreadable fields disappear on success. `lastChanged` restricts modified employees; null dates may cover pre-June-2011 records. `filterDuplicates` is enabled unless `no`. JSON needs exact Content-Type; unsupported inferred Accept/format gives 404. These rules apply to the legacy ad-hoc route, not every UI report. Short deciding passage: “both Active and Inactive”.

## Directory publication population

https://documentation.bamboohr.com/reference/get-employees-directory

Read 2026-10-11; displayed “Updated 6 months ago.” One response, configured publication population; inactive/former and excluded employees absent. Directory `onlyCurrent` checks hire/status effective dates, unlike reports. Sharing controls fieldset and 403; org-chart-only mode lacks department/contact fields. Configuration-empty directory returns 404. This is not an authoritative roster. Short deciding passage: “not that no such employee exists”.

## Employee field meanings

https://documentation.bamboohr.com/docs/list-of-field-names

Read 2026-10-11; displayed “Updated about 1 year ago.” `id` is assigned internal ID; `employeeNumber` is company numbering. `status` is Active/Inactive. Employment categories are customizable; job fields are current unless accessing Job History. `lastChanged` records modification time, not effective event time. `originalHireDate` and current hire/termination fields cannot alone describe multiple employment spells.

## Dataset v2 field access and paging

https://documentation.bamboohr.com/reference/get-data-from-dataset-v2

Read 2026-10-11; displayed “Updated 6 months ago.” Dataset-specific names: `eeid`, `email`, `jobInformationDepartment`. Restricted fields have empty values plus `_restrictedFields`; dataset denial is 403 and inaccessible/unknown dataset is 404. Bad names: 400 INVALID_ARGUMENT, singular detail. Order fields must be selected: UE-1001. Filter cannot mix and/or; no not-in; multi-value in is for options types. Page default 1, size 100, maximum 1000; totals cover matching query rows, not necessarily unique people. Next links and total pages expose incomplete exports. Short deciding passage: “the request is not rejected”. This field restriction behavior corrects the overly broad claim in List Employees' recommendation that reporting routes always fail loudly.

## List Employees access effects

https://documentation.bamboohr.com/reference/list-employees

Read 2026-10-11; displayed “Updated 6 months ago.” Internal key is employeeId. Unreadable fields return null with restriction markers; unreadable filter/sort fields can remove employees. Unknown names ignored. Cursor pagination defaults 250, maximum 2500; meta.total counts query matches. BadPage can reflect a changed boundary employee. Restricted grouping must be compared with readable-row coverage. The page's recommendation of broader reporting routes does not override dataset field-level restrictions documented above.

## Effective-date table schemas

https://documentation.bamboohr.com/docs/table-name-fields

Read 2026-10-11; displayed “Updated about 1 year ago.” employmentStatus supplies dated category history; jobInfo supplies dated department/location/division/job/manager history. Each uses date. Compensation startDate/endDate belongs to compensation; do not treat those dates as company membership without supplied evidence.

https://documentation.bamboohr.com/reference/get-employee-table-data

Read 2026-10-11; displayed “Updated 4 months ago.” Table rows arrive unsorted. Unreadable fields are omitted. The `all` identifier means employees accessible to that caller, not unrestricted company completeness. A 404 can identify absent employee or table. This plugin analyzes supplied history; it does not call the endpoint.

## Account and dataset catalogs

https://documentation.bamboohr.com/reference/list-fields

Read 2026-10-11; displayed “Updated 6 months ago.” Account metadata includes standard/custom field identifiers, labels, types and deprecation flags. The dedicated dataset catalog below decides dataset query names.

https://documentation.bamboohr.com/reference/get-fields-from-dataset-v1_2

Read 2026-10-11; displayed “Updated about 2 months ago.” Use returned name, not label. Catalog is paginated: 500 default fields, maximum 1000; collect all pages. Unknown dataset here returns 422 DATASET_NOT_FOUND, unlike data endpoint's 404. No parent/entity/type server filter.

https://documentation.bamboohr.com/docs/api-details

Read 2026-10-11; displayed “Updated 12 months ago.” Internal employee ID is immutable and unique within a company. General HTTP guidance must yield to endpoint-specific errors. Its broad “only V1” text is older than the explicit v2 endpoint documentation; it is not used to deny v2 availability.

## Analysis conventions

The following are this plugin's rules of thumb, not BambooHR platform policies: company-scoped ID set reconciliation, no fuzzy identity matching, counting unique people rather than rows, using disjoint difference sets, requiring evidence for a causal explanation, sorting effective history and applying the user's boundary/category convention, and marking conflicting same-date history unresolved. Date boundaries and employment-category inclusion come from the user, not an invented universal HR policy.

## Fix verification — 2026-10-11

All ten official URLs above reopened during bfix. Directory sharing is independent of employee-record access; dataset v2 values are nested under each row's `fields`. Historical extraction uses `/api/v1/employees/{id}/tables/{table}` with `employmentStatus` and `jobInfo`; their effective field is `date`. Compensation boundaries do not establish employment membership. Sources: Directory, Dataset v2, Employee Table Data and Table Name & Fields above; read 2026-10-11. These concrete endpoint semantics, rather than ordinary set/date arithmetic, are the knowledge contribution.
