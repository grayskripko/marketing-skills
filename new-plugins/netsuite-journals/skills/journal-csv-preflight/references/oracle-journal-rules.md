# Oracle journal import rules

Read 2026-10-11. Scope: current public NetSuite Applications Suite online help, regular and standard intercompany journals; advanced intercompany is separate. All sources loaded without account authentication. The pages do not display a last-updated date. Current means the public pages retrieved on this date, not a forecast for 2026-10-18 or evidence of the user's account release. Maintainers should refresh sources before releasing an updated package. During skill use, fetch nothing; resolve conflicting supplied settings or release evidence by marking the affected conclusion unresolved and requesting relevant pasted documentation or mappings. The 2026.2 CSV release page reports a Units Type change, not changed journal rules.

The notes below are paraphrases, not a copied manual. Actual company references and permissions come from supplied exports. Source-verification evidence is recorded in [source-check.json](../../../tests/source-check.json).

## 1. Using Journal Entry Import for Updates

URL: https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_1534490251.html
Read 2026-10-11; publication/update date not displayed; HTTP 200.

Single import cannot update. CSV Update adds incoming lines; non-keyed journal lines require full exported sublist replacement for edits. Any update of a payment-applied journal removes that payment application.

## 2. Journal Entry Import Errors

URL: https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_4570029068.html
Read 2026-10-11; publication/update date not displayed; HTTP 200.

Account errors can reflect formatting, inactivity, subsidiary association or ID mapping. Department errors call for hierarchy and active/reference-type checks; entity errors include transaction-currency compatibility. Blank headings, extra totals and start/end dates have specific remedies. Rounding errors require raw precision inspection and removal of unused-side zero amounts.

## 3. Importing a Journal Entry

URL: https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_N1472877.html
Read 2026-10-11; publication/update date not displayed; HTTP 200.

Single journal import supports 10,000 lines, with UI/performance concerns over 1,000. Regular entries need two balanced lines; standard intercompany entries need four with a debit/credit for both subsidiaries. Single import maps a lone Memo or Line Memo to line memo; with both it separates body and line. Date and Entry No. can default. Failed imports expose results.csv.

## 4. Making Journal Entries

URL: https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_N1469880.html
Read 2026-10-11; publication/update date not displayed; HTTP 200.

UI and synchronous SOAP: 1,000 lines; CSV, SuiteScript and asynchronous SOAP: 10,000 per transaction. Journal posting requires approval. Closed periods cannot be selected; unavailable periods may be recalculated according to accounting preferences.

## 5. Journal Entry Import and Intercompany Journal Entry Import

URL: https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_N418118.html
Read 2026-10-11; publication/update date not displayed; HTTP 200.

Regular and standard intercompany imports are distinct tasks. Standard intercompany has one originating and one receiving subsidiary. Multi-Book enables Accounting Book and Is Book Specific. CSV assistant route is Setup > Import/Export > Import CSV Records, Transactions, selected journal record type.

## 6. Journal Entry and Intercompany Journal Entry Header Fields Table

URL: https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_1534492479.html
Read 2026-10-11; publication/update date not displayed; HTTP 200.

New CSV records need Date; OneWorld needs Subsidiary; standard intercompany also needs To Subsidiary. Internal ID is for updates. Closed Posting Period yields an error. Imported approval needs Journal Approval. Header memo maximum 999. Class/Department move to line scope with the per-line preference. Multi-Book: true without book targets primary; omitted flag with book is book-specific; false or neither fields means ordinary journal.

## 7. Journal Entry and Intercompany Journal Entry Line-Level Fields Table

URL: https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_1534492737.html
Read 2026-10-11; publication/update date not displayed; HTTP 200.

Account required: numbering enabled accepts number/name or number alone, not name alone; disabled uses names. Debit/Credit maximum 10 digits before decimal and 2 after. Line memo maximum 4,000. Multi-Location Inventory requires Location. Standard intercompany line subsidiary is origin or receiver; use a separate Line Subsidiary heading to avoid body automapping. Defaults need subsidiary-valid references.

## 8. Single Journal Entry Import

URL: https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_N433632.html
Read 2026-10-11; publication/update date not displayed; HTTP 200.

Single import needs Make Journal Entry and Posting Period permissions, not Import CSV File. Supports simplified reference names for Account/Class/Department/Location/Subsidiary. Date and Entry No. may default. Does not send the usual failure notification email.

## 9. Journal Entry CSV Files

URL: https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_1534489651.html
Read 2026-10-11; publication/update date not displayed; HTTP 200.

CSV assistant supports combined or separate header/line files. Every row needs the transaction identifier and, in combined files, repeated header values. Entry No. or External ID identifies new records; Internal ID is update-only. Without new-entry identifiers input becomes a single import. Since 2021.2 automatic mapping uses Journal Entry - Line and Intercompany Journal Entry - Line. Keep regular and intercompany in separate jobs.

## 10. Permissions for Importing Journal Entries with the Import Assistant

URL: https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_1534489333.html
Read 2026-10-11; publication/update date not displayed; HTTP 200.

CSV assistant requires Make Journal Entry Edit/Full, Posting Period on Transactions Full and Import CSV File. Setting approval requires Journal Approval Edit/Full. OneWorld role subsidiary access affects import. Single import is available without Import CSV File.

## 11. Custom Form Specification for Journal Entry Imports

URL: https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_1534490534.html
Read 2026-10-11; publication/update date not displayed; HTTP 200.

Mapping defaults to the preferred form. CSV assistant Advanced Options can select a role-available custom form to expose its fields. Single import has no custom-form selection.

## 12. Advanced Intercompany Journal Entry Import

URL: https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_1498465157.html
Read 2026-10-11; publication/update date not displayed; HTTP 200.

Each imported advanced entry needs at least four lines with debit and credit coverage for origin and receiver. Advanced intercompany supports multiple receiving subsidiaries, a separate line sublist and feature-dependent Auto Balance using Automated Intercompany Management. Update appends; full exported lines plus Overwrite Sublists replace. Single import cannot update or choose a custom form. Do not transfer standard two-subsidiary constraints to this record type.

## 13. Making Advanced Intercompany Journal Entries

URL: https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_4803443925.html
Read 2026-10-11; publication/update date not displayed; HTTP 200.

Advanced entries respect role/account/subsidiary restrictions. First line posts to originating subsidiary. Per-subsidiary posting balance matters; a global balance alone is insufficient. Auto Balance adds elimination lines, using accounts valid for currency/subsidiary. The feature and supplied configuration decide availability; no invented balancing lines.

## 14. General CSV File Conventions

URL: https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_N453326.html
Read 2026-10-11; publication/update date not displayed; HTTP 200.

General CSV assistant limit: 25,000 records or 50 MB for the whole job across all files. Delimiter must match the selected separator. Trailing genuinely blank lines are ignored. Fields without headings are not imported. Name/ID reference types must match the supplied values.

## 15. CSV Import — NetSuite 2026.2 release notes

URL: https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_N3949069.html
Read 2026-10-11; publication/update date not displayed; HTTP 200.

Current release note documents Units Type bulk imports, not a change to journal append/overwrite rules. It confirms 2026.2 documentation exists; it does not prove the user account is on that release.

## 16. Making Intercompany Journal Entries

URL: https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_N1475891.html
Read 2026-10-11; publication/update date not displayed.

Standard intercompany lines belong only to origin or receiver; the first line posts to the header origin. Posting requires balance within each subsidiary. Advanced entries replaced legacy intercompany entries in new OneWorld accounts from 2018.1; inspect the supplied record type rather than assuming legacy availability.

## Working conventions

These are workflow choices for this package, not additional Oracle requirements: preserve CSV row numbers; classify confirmed defects separately from missing evidence; use exact decimals; ask for complete current lines before a replacement; label partial corrected output as a repair fragment; reconcile actual job success and fresh current state before retry. Never manufacture an accounting choice or an ID.
