# Official Ramp rule register

Read and independently rechecked for bfix 2026-10-11. All five official URLs loaded with relevant current article content. No visible publication or revision date is exposed in the retrieved pages; this records observation, not an invented effective date. Reopen before planned submission around 2026-10-20. No future validity is assumed.

| Source URL | Sections and supported decisions |
|---|---|
| https://support.ramp.com/custom-accounting-csv-exports/ | Transactions; required content types for single/double-line and refund setting; CSV Customization setup; scope excludes reimbursements. |
| https://support.ramp.com/exporting-your-data-to-csv/ | Expenses accounting dimensions; enabled optional fields; exact repeated suffixes; Accounting readiness and reporting-export separation. |
| https://support.ramp.com/universal-csv-overview/ | Mandatory coding fields; card export reset; reimbursement partial/final batch behavior and payment reset. |
| https://support.ramp.com/marking-transactions-as-synced/ | Direct-ERP previews versus Mark as synced; direct card sync is permanent; ERP deletion does not reset Ramp; split readiness and Plus permissions. |
| https://support.ramp.com/quickbooks-desktop-file-export-overview | CSV and IIF choices; statement payments excluded from IIF; IIF import privileges and single-user mode. |

## Bill Pay field requirements

Custom bill expense single-line: vendor name/ID, account name/ID, Bill Date, Invoice Number and Bill Amount. Double-line replaces Bill Amount with debit and credit.
Custom bill payment single-line: vendor name/ID, account name/ID, Payment Date, Payment ID, Invoice Number and Payment Amount. Double-line replaces Payment Amount with debit and credit. Source: custom-accounting-csv-exports, bill and payment requirements, read 2026-10-11.

## Scope and authored checks

Universal CSV customization rules are not universal requirements for every ERP. Target-import rules come from the supplied template, not these articles. Optional Expenses headers depend on enabled fields and accounting configuration. The register defines no timeout or generic ERP error code.

This plugin's rule of thumb: compare row identity, target completeness, separate currency totals and supplied split amounts before calling mapped rows ready. Positive debit/credit conversion follows the user's target convention, not a Ramp-mandated universal sign scheme. Row preservation, missing-value markers and source-as-data boundaries are authored operating instructions.

## Fix verification

The split-readiness rule applies to the separate unready transaction, not the ready preview transaction. Source: https://support.ramp.com/marking-transactions-as-synced/ (split readiness), read 2026-10-11. Signed-to-debit/credit formulas are authored conversions conditional on supplied direction; positive liability movements can be credits. Nonnegative magnitudes do not select the direction. Accounting reimbursement customization is excluded by https://support.ramp.com/custom-accounting-csv-exports/; reporting-field selection remains available under Reimbursements > History in https://support.ramp.com/exporting-your-data-to-csv/, both read 2026-10-11.
