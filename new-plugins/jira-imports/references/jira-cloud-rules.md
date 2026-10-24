# Jira Cloud CSV source register

Verified by opening the six CSV pages and the service-request fallback page on 2026-10-11; reopened during bfix-jira-imports on the same date. Header, service-space and existing-parent scope findings were checked against article bodies. This is an access date, not a claimed publication date. Except where stated, no explicit last-updated date was displayed. Sources loaded as current Jira Cloud support pages; they refer to the current Parent field and old/new import experiences. Recheck before the planned 2026-10-14 submission and whenever the user's interface differs. Account configuration remains user-specific.

## Bulk creation route

[Create work items using the CSV importer](https://support.atlassian.com/jira-software-cloud/docs/create-issues-using-the-csv-importer/) — read 2026-10-11.

Deciding sections: opening permissions and hierarchy notice; CSV file requirements; aggregating values; cascading fields; field import notes.

- The non-admin bulk route caps each file at 250 work items. It cannot map parent-child hierarchy, even if the file is smaller. Use external system import for hierarchy.
- Avoid punctuation in header names apart from separator commas. Renaming needs a source-to-output-to-field map; preserve repeated headers and values. This is guidance, not a claim every punctuation mark causes failure. Summary must be mapped. Mandatory target fields must be on the relevant Create screen. Quote embedded commas/newlines and double literal quotes; keep empty delimiters.
- Multiple values use repeated column headers. Estimates are seconds. Bulk cascading-select import is unavailable through the illustrated syntax; administrators use external system import.

## Old administrator import

[Import data from a CSV file](https://support.atlassian.com/jira-cloud-administration/docs/import-data-from-a-csv-file/) — read 2026-10-11.

Deciding sections: recommended data size; updating existing work items; field mappings; field-value mappings; import notes.

- Header names should avoid punctuation apart from separator commas; preserve the source-to-output mapping when renaming. Settings → System → External System Import, switching to old experience if necessary. UTF-8 default, configurable delimiter and Java date pattern.
- The 1500-work-item batch size is a performance recommendation, not a hard maximum; no fixed completion-time promise.
- Existing Work Item Keys can update records. Verify the selected target; otherwise new keys may be assigned. A relationship ID is a different field.
- Map unresolved Resolution to Import as blank; this differs from no value mapping. Status values must exist. Existing work types must be used for team-managed targets.
- Jira Service Management comments mapped to Comments body become public. Keep private notes out of this public mapping. Supply the corrected import copy plus the exact original private-note text for separate Add internal note entry on the existing ticket; do not rely on a visibility column to make Comments body private.

## Company-managed hierarchy

[Keep work parent-child relationships during CSV import to Jira Cloud](https://support.atlassian.com/jira/kb/keep-issue-parent-child-mapping-during-csv-import-to-jira-cloud/) — read 2026-10-11; page states updated 2026-07-03.

Deciding sections: Before you begin; Map issue IDs; confirm relationships; Parent field not available.

- Cloud company-managed procedure. Current mapping uses Parent rather than Epic Link; a legacy export may require checking migration state.
- Each row has a unique numeric ID. A child's Parent is the parent's ID, not issue key. Parents must precede children, including cross-project parents imported earlier.
- Missing Parent/ID: check sub-tasks enabled and Linked Issues on screens before inventing a field.
- Existing parents must be present before children. The detailed procedure uses the old experience; it is not evidence that every new importer supports child-only retries into an existing target. Verify the retry route and its existing-parent reference mechanism before replacing failed-child references; obtain real destination IDs only when that mechanism requires them. Normal user-operated Create with the existing parent selected is a separate option for a confirmed-failed child, after checking for prior creation; do not transfer CSV ID prerequisites to it.
- Verify both child's Parent and parent's child list after import.

Source conflict: the general old-import article shows a parent after a child in its sample although its prose requires parent-first ordering. This register follows the explicit requirement and the newer hierarchy guide. Never copy the inconsistent sample order. The key column in the hierarchy example is illustrative; it does not guarantee key preservation.

## New import preparation and permissions

[Prepare a CSV file for import](https://support.atlassian.com/jira-software-cloud/docs/prepare-a-csv-file-for-import/) — read 2026-10-11.

Deciding sections: permissions; user assignments; comment structure; hierarchy; service organizations.

- Org/site/Jira administrators may use the new experience. Users allowed to create team-managed spaces may import into new team-managed business spaces, but cannot move users; assignments remain unassigned and comment tags become plain text.
- User preparation uses emails. Comments require created date, creator and body separated by semicolons; malformed structure may show Anonymous.
- Hierarchy uses work type, unique work item ID and Parent.
- Jira Service Management organization names are at most 200 characters. New service-space imports need a reporters column and work-type → request-type/status mapping. TASK/SUBTASK/other values default to NO REQUEST TYPE; GENERAL REQUEST defaults to EMAILED REQUEST; absent default status becomes IN PROGRESS. Confirm intended destination choices rather than inventing them. Documented defaults do not establish the mappings in a user's preview; when required controls are absent, lead with the supported customer-entry handoff.

## New field mapping

[Map CSV data to Jira fields](https://support.atlassian.com/jira-software-cloud/docs/mapping-csv-data-to-jira-fields/) — read 2026-10-11.

Deciding sections: dates and times; work types; cascading selects; character limits.

- Unmapped columns are excluded. Hierarchy requires all three mappings; dependency links are separate link-type mappings and also require work item ID.
- Date/time options use Java SimpleDateFormat and locale. Time fields use integer seconds; values below 60 seconds display as zero minutes.
- Cascading select uses parent then `->` then child. Missing parent fails; absent separator imports as parent. A configured parent–child pair does not establish the intended parent of a source row; present it as a candidate until confirmed.
- Documented truncation thresholds: Summary/Labels/short text 255; Description/Environment/text area 30000; work type/status/priority/resolution 60. The table also lists generic custom fields at 255; verify the actual field type instead of imposing that on text areas.

Documentation caution: the table labels RESOLUTION as a date/time field, conflicting with the old-import Resolution-value instructions. Do not teach that label as a general field-type rule. Use the actual destination field and the route's mapping screen.

## New import errors

[Fix errors in a space import](https://support.atlassian.com/jira-software-cloud/docs/fix-errors-in-a-project-import/) — read 2026-10-11.

The table applies to the new experience, including direct third-party imports; only CSV-relevant entries are supported here.

DT001 and DA002: selected locale/date/time mismatch. NU003: invalid numeric content. CS004: structural row/column or line-break problem. EM005: email format. UR006: URL format. IS007: empty Summary. TE008: estimates or spent time not digit-only seconds. ON014: organization name beyond 200 characters. PA009 concerns a direct-import access token and is outside CSV preparation; never request a token to fix CSV data.

Numeric caution: NU003's remedy describes digits 0–9 only, while field mapping describes valid number values. Preserve intended decimals/signs and confirm field acceptance rather than deleting punctuation and changing value. A partial import produces a downloadable or emailed error log; reconcile successful work before rerunning creation.

## Service-request fallback when importer controls are unavailable

[Raise a request for a customer](https://support.atlassian.com/jira-service-management-cloud/docs/raise-a-request-for-a-customer/) — read 2026-10-11.

An agent/admin can use Create in the configured service space, select the real request type and Reporter, and supply the request details; the portal also supports raising on behalf of a customer. For a small supplied file whose import screen cannot preserve those fields, this is a concrete user-operated alternative. Preserve supplied summaries/descriptions and identities. Do not create a plain text custom field as a substitute for the real Reporter or request type. Do not require the user to choose an initial status when no such preservation requirement was supplied. Verify Reporter and Request type before sending and the supplied fields afterward; stop if the real fields cannot be selected. Do not promise notification delivery without configuration evidence.

## Local preparation choices

These are preparation recommendations, not Atlassian mandates: preserve an untouched source, keep a row trace after sorting, block ambiguous values, use a small representative trial, and reconcile partial success before retries. Cycle checks and referential checks protect the requested hierarchy. No fixed local score or arbitrary row-sampling limit is imposed. CSV preparation does not prove a live account's fields or permissions.

## rename-jira-imports source check — 2026-10-11

Reopened the old CSV import and new field-mapping sources above. The old import attachment section specifies HTTP(S) URLs accessible to Jira Cloud. The new mapping section requires Work item ID for links and a selected link type; hierarchy uses separate Work type/ID/Parent mappings. Post-import count and field comparisons are preparation recommendations applied to user-supplied results.
