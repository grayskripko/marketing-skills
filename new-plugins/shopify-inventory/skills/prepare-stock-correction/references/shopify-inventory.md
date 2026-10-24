# Shopify inventory evidence

Verified live on 2026-10-11. The three pages loaded; none displayed an update/publication date. These are current observed rules, not a promised future version. Publisher maintenance note: recheck these sources before package submission around 2026-10-14. This is not a runtime retrieval instruction or a prerequisite for the user’s CSV submission.

## Inventory CSV

https://help.shopify.com/en/manual/inventory-and-locations/setup/inventory-csv — read 2026-10-11

All states exports offer current/new on-hand checking; Available-only exports do not. Retain current and edit new. Conflicts reject affected rows with email details. Clearing current disables checking. Blank new leaves quantity alone. Imports must not exceed 15 MB. Whole-number values may be negative or zero; Not stocked is distinct from zero.

Identity requires handle, location and used option values. Location case must match. No-option value: Default Title. SKU is optional and not changed here. Titles and option names do not rename variants. Non-editable states remain untouched.

Packed sizes require positive values, all four fields together, and cm/in units. Four blanks clear dimensions. Variant rows across locations/bins must agree, including blank groups; disagreement rejects that variant while other variants can import. Preserve unrelated metadata. Native import includes summary review before Start import. Inactive locations stay inactive after stocking. Quantity imports are absolute targets, not signed adjustments.

## Inventory states

https://help.shopify.com/en/manual/inventory-and-locations/fundamentals/inventory-states — read 2026-10-11

On hand combines Available, Committed and Unavailable. Incoming is outside that total until received. A placed, unfulfilled order can move units from Available to Committed, leaving the on-hand total unchanged. Changing On hand shifts Available by the same amount. Thus an on-hand comparison cannot detect every intervening order. This limitation is an inference from the documented state definitions and CSV comparison, not an extra Shopify guarantee.

## Adjustment history

https://help.shopify.com/en/manual/inventory-and-locations/adjusting-inventory/adjustment-history — read 2026-10-11

Product/variant history covers the last 180 days; older changes require the Inventory adjustment changes report. History shows the adjustment first and resulting total second; a dash means that state was unaffected, not that stock equals zero. Staff, apps and channels can cause changes. Native path: Products > product > variant if needed > Inventory > View adjustment history, with tracking enabled. Activities include Inventory correction, Transfer created and Reservation created; use state deltas to distinguish physical movement from reservations. For older evidence, guide the user to open Analytics > Reports, filter Category to Inventory, and select Inventory adjustment changes, then filter the available report by the relevant variant/product, location and date range and supply the relevant rows. Align the supplied timestamps with the count and import timezone. Read adjustment deltas rather than treating resulting totals as movements. For an unexplained rejection, request the full error and outcome from the user, analyze supplied evidence to check whether the correction applied and inspect later movements, and ask the user for any missing history and a refreshed export before preparing the retry. Do not invent a meaning for an unknown processing code.

Report navigation source: https://help.shopify.com/en/manual/reports-and-analytics/shopify-reports/report-types/default-reports/inventory-reports — read 2026-10-11.

## Authored operating choices

The reconciliation formulas, held-row decisions, successful-row exclusion, grouping variants when splitting files, and no-network scope are authored safeguards, not platform promises. CSV quantity checking is not an all-state or file-wide transaction. Do not equate equal on-hand totals with an absence of intervening activity. Preserve count basis, times and the evidence that a discrepancy remains unapplied.
