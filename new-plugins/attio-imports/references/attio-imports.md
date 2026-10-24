# Attio CSV decisions and sources

All URLs below loaded successfully and were read 2026-10-11. No publication/update date was shown in the retrieved article bodies. These are dated observations; recheck relevant official documentation when the requested answer depends on current behavior not established by supplied evidence. Summaries are paraphrases. Scope: Attio's official CSV importer, with an explicitly separate optional migration path.

## CSV import: destination, matching and limits
https://attio.com/help/reference/imports-exports/csv-imports/import-data-into-attio-via-csv

CSV needs headers; caps are 100,000 rows, 100 columns, 100 MB. Object attributes belong to records; list attributes to workflow entries. People/company data goes through People; adding deals requires another Deals import. Unique values match primary and linked records. Deals require name, owner and stage. Attio IDs update existing items; unmatched IDs skip. Blank cells preserve existing values; multi-values append. Lists distinguish adding another entry from updating. Multiple linked targets accept only their unique fields, so other linked attributes need separate imports. Map columns → Data preview shows up to 100 rows; Preview import estimates changes without comparing new rows with one another; new repeated keys inflate creation estimates. Notes/tasks cannot import through CSV. Object imports require admin or write/full access; list-only Entry-ID updates have a narrower permission exception.

Email-only People imports automatically create companies from business email domains and link Company ↔ Team. Public email providers (for example gmail.com, outlook.com, icloud.com) are excluded. This does not establish the source employer or a way to disable linking. See “Importing a single object.” Email/domain enrichment is separate from matching by a configured unique attribute; the troubleshooting article below explicitly supports other unique attributes.

## Formats
https://attio.com/help/reference/imports-exports/csv-imports/csv-import-formatting-guide

Text accepts line breaks and URLs. Numbers truncate beyond four decimals; infinity fails. Currency has the same four-decimal precision limit and removal of additional digits as numbers; it is numeric without symbols, in the configured currency. Dates require choosing ISO/European/American interpretation; ISO dates use YYYY-MM-DD. Timestamps use ISO8601 by default. Checkboxes accept 1/true/TRUE/#t and 0/false/FALSE/#f; blank is described as unchecked, while the import guide says blanks skip existing updates: do not use blank as an erase operation. Select/status labels ignore case. Commas separate multi-select values and cannot occur inside their labels. Users match membership ID, email, full name, then first name; no/ambiguous match fails. Phone numbers require E.164. Location components belong together in one mapped column. Full person names or separate first/last fields work. Foundation date retains only the year, truncating a supplied full date. Preserve originals outside upload files and obtain acceptance of lossy mapping; those preservation steps are authored safeguards.

## Error interpretation and recovery
https://attio.com/help/reference/imports-exports/csv-imports/troubleshooting-csv-imports

Required-value failures need the missing attribute. Multiple list matches require Entry IDs. Missing primary/linked Record IDs require real Attio IDs. Object-rule failures require satisfying the condition. Hidden attributes/filters can explain apparent missing data. Preview overcounts repeated new keys. Distinguish duplicate records from repeat list entries with different workflow values. Stuck imports can follow concurrent runs or incomplete cancellation; finish or fully cancel one before another. Do not assume cancellation reverses earlier writes.

## Relationship model
https://attio.com/help/reference/managing-your-data/attributes/relationship-attributes

Relationships have attributes on both sides and mirror links. Each side can permit one or multiple records. Creating/managing custom relationships requires Pro/Enterprise and admin or Full access on both objects. Check existing system relationships before proposing custom ones; don't claim all existing relationships require a plan upgrade.

## Conditional object requirements
https://attio.com/help/reference/managing-your-data/objects/create-and-manage-rules

Rules apply to object records, not lists, on creation/update. A satisfied condition with an unmet requirement blocks changes. Pro/Enterprise supports these rules; Pro allows eight per object, Enterprise has no rule-count cap. Rule creation requires admin or Full object access. Fix the data rather than bypassing a workspace policy.

## Saved imports
https://attio.com/help/reference/imports-exports/csv-imports/view-and-manage-csv-imports

CSV management is available on all plans. Admin history: Workspace settings → Objects/Lists → destination → Import history. Initiator history: Account settings → Import history. Drafts preserve setup. History distinguishes Draft, In progress, Canceled and Failed. Deleting a draft removes setup and uploaded file, not a general rollback mechanism.

## Optional documented migration path
https://attio.com/help/reference/imports-exports/migrate-data-from-another-crm

Attio documents Import2 for supported CRMs, including notes/tasks/files. It requires a paid plan and admin; the service is described as free for Attio users. It maps objects to objects, not lists, and doesn't update existing record attribute values. Source-specific restrictions apply; Salesforce Cases are excluded. Verify the current supported-source list rather than assuming a CRM is supported. This package only explains setup if asked and does not connect to that service.

## Authored preparation decisions

The following are workflow safeguards, not claimed Attio requirements: preserve foreign IDs; resolve source foreign keys before mapping target keys; hold ambiguous identities, dates and conflicting same-key values; retain unresolved relationships and notes separately; deliver unaffected rows; use a CSV writer; retry only confirmed failures after checking partial results; do not delete data or disable rules to pass an import. No universal numeric deduplication score or guaranteed migration count is asserted.

## Applying these decisions to the requested answer

Lead with the requested result and include only relevant import rules. Required deal values are separate from matching safeguards: updates/retries need reliable matching; confirmed-new creation does not universally require a configured unique deal key. Preserve source IDs in recovery data without requiring new destination attributes, and map only established relationships. Apply checks internally; report the specific correction, held values and necessary verification rather than a fixed report. Confirm unchanged fields for scoped edits, and deliver resolved retries independently of held rows. These are authored preparation decisions; the safeguards above remain in force.
