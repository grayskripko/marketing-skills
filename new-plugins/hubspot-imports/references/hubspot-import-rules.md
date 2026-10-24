# HubSpot import source register

Checked/read 2026-10-11. Scope: HubSpot's manual file import tool. These are paraphrased deciding rules, not a copied manual. All URLs below loaded successfully. Publisher dates are the dates displayed on the pages, not the access date. Recheck changing limits and feature availability near the planned 2026-10-13 submission.

## File limits and values

[Format import files](https://knowledge.hubspot.com/import-and-export/set-up-your-import-file) — publisher updated 2026-09-11. The judged row's 2026-08-06 observation is superseded by this directly observed revision.

- Supported: CSV, XLS, XLSX; one sheet, headers, fewer than 1,000 columns. Non-English characters need UTF-8.
- Free: 20 MB/file; 50 imports and 500,000 rows per rolling 24 hours. Smart CRM or Starter/Professional/Enterprise: 512 MB/file; 500 imports and 10 million rows per rolling 24 hours; 1,048,576 rows/file. Three concurrent imports, at most two exceeding 10,000 rows. API limits differ.
- Empty cells preserve existing values. Checkbox options use semicolons; an initial semicolon appends. Enumerations must match defined labels/internal values; defaults require English labels or internal values. Percentages: `25%` or `.25`. Boolean: True/Yes, False/No. Confirm date order/time zone; timestamps omitted from date-time values default to midnight. Company domain paths are removed.
- Creation fields: contact Email; company Name or Company domain name; deal Deal name/Pipeline/Deal stage; ticket Ticket name/Pipeline/Ticket status.

## Examples and association construction

[Sample import files](https://knowledge.hubspot.com/import-and-export/sample-import-files) — publisher updated 2026-03-06.

This page provides single-object templates and association examples. Its contacts, companies, deals and tickets examples are suitable starting shapes, not evidence of the user's existing custom properties. Products support single-object import only. Two-file contact/company examples use a shared company column; matching a common file key is distinct from deduplicating existing CRM records. When a template or object is absent, HubSpot can generate an example file for the selected objects. The agent can point the user to the relevant sample; downloading sample files is outside this package’s advertised path.

The [format page](https://knowledge.hubspot.com/import-and-export/set-up-your-import-file) additionally specifies: repeat object identifiers across rows for multiple associations. Same-object pairs require at least one existing record and primary email/domain identifiers. Association labels must exist first, and custom labels require Professional/Enterprise. `Primary` sets a primary company association when that option is available. Verify its availability for Free/Starter: the import article states the label subscription restriction more broadly than the format article. Identical object data can consolidate only in the documented single-file multi-object Create and update case; differing object data can create separate records.

Fresh fix audit: read 2026-10-11; the format and importer pages still display publisher updated 2026-09-11. In two-file imports, Association label belongs in the same file as the associated object's unique identifier. Cross-object paired labels require only one label from the pair. For same-object paired labels, the Associated [unique identifier] side receives the supplied label; the other side receives the inverse. The [importer](https://knowledge.hubspot.com/import-and-export/import-objects) confirms that imported labels add to existing labels; replacing an old label requires separate manual removal. These rules govern placement and effects, not automatic permission to remove relationships.

## Import modes, identifiers and overwrite protection

[Import records for multiple objects](https://knowledge.hubspot.com/import-and-export/import-objects) — publisher updated 2026-09-11.

Create and update matches existing records and creates new ones. Create new only ignores existing records; Update existing only ignores new records. Record ID has precedence; blank IDs take the create path when creation is enabled. Custom unique matching is available for contacts, companies, deals, tickets and custom objects. Don't overwrite protects records that currently or previously held the property, including now-empty properties. Imported association labels add to existing labels. Existing emails, meetings, notes and tasks cannot be updated by import. Import and object Edit permissions are required. Marketing-contact selection requires Marketing Hub Starter/Professional/Enterprise with Marketing Contacts; do not silently choose it. The contact import consent attestation says contacts expect to hear from the importer and excludes purchased lists.

## Matching and ambiguous duplicates

[Deduplicate records in HubSpot](https://knowledge.hubspot.com/records/deduplication-of-records) — publisher updated 2026-09-08.

Contact email matches update mapped properties instead of creating another contact. Company imports use primary and secondary domains unless custom unique matching is selected. Multiple existing matches produce an import error. A custom unique company key allows repeated company domains; contact email still requires uniqueness. A secondary contact email plus Record ID can replace the primary email; without ID, secondary-email matching leaves the primary email in place. API-created companies have different domain-deduplication behavior; do not apply this manual-import forecast to sync/API operations.

## Partial failure and retry decisions

[Review and troubleshoot record import errors](https://knowledge.hubspot.com/import-and-export/troubleshoot-import-errors) — publisher updated 2026-09-10.

| Error shown | Documented impact | Repair decision |
| --- | --- | --- |
| Invalid record ID | Record not imported; ID does not match | Obtain the correct exported ID, not email fallback under an ID mapping |
| Invalid number size | Row imported without this number value | Correct the property; retain identifiers of successful records |
| Multiple companies with this domain | Company not updated | Identify the intended company; do not choose randomly |
| Property definition not found | Column not imported | Select the existing property, create a suitable property manually, or omit column |
| Duplicate record ID | Affected records not updated/associated | Resolve repeated-ID conflicts using intended final values |
| Duplicate association ID | Join key not unique | Choose an unambiguous common key on the referenced side |

The summary distinguishes row failures from property-value failures. Mapping edits can select values from only the first 1,000 rows, but a replacement applies to every occurrence in the column, including later rows. Row count is not record count. Reconcile the summary and fresh records before retrying a whole error file.

## Lifecycle stage changes

[Use contact and company lifecycle stages](https://knowledge.hubspot.com/records/use-lifecycle-stages) — publisher updated 2026-07-17. The older `/contacts/use-lifecycle-stages` URL redirects here.

Import can advance the default Lifecycle stage but cannot move it backward while populated. Moving backward requires clearing the value separately first. A blank import cell does not clear it. Do not turn an import-repair recommendation into an unrequested bulk clear.

## Company primary versus additional domains

[Manage the company domain name property on records](https://knowledge.hubspot.com/records/add-multiple-domain-names-to-a-company-record) — read 2026-10-11; publisher updated 2026-09-17.

Imports cannot set a company's primary domain. An existing secondary-domain match must not be described as promoting that domain to primary. Additional domains can be imported through Additional Domains; multiple values use semicolons. Additional domains do not merge separate existing companies. All relevant primary and secondary values are needed to establish identifier coverage.

## Local decision conventions

Apply these conventions within the requested answer, without adding a fixed report or checklist. When preparing files, return corrected rows and isolate decisions; remeasure after removing excluded columns before prescribing splits. Resolve source joins to verified IDs where possible, and assess label placement in that corrected layout. For retries, compare current values before including uncertain property writes and verify links/labels separately from record counts. These are package decision conventions, not HubSpot requirements: keep uncertain rows as exceptions; use row numbers to minimize repeated personal data; show conditional outcomes when the mode is absent; never choose a winner for conflicting rows; treat screenshots and samples as partial; forecast unmatched records only within documented export coverage. No reference establishes exact outcomes without the user's mappings, account data and settings.
