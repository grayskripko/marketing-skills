# Official Looker Studio blend knowledge

Scope: Looker Studio blends. Google's current pages use Data Studio. All URLs below loaded on **2026-10-11**; each page showed **Last updated 2026-10-07 UTC**. These dates apply to the documentation, not the user's exports. Recheck whenever a UI or field rule conflicts with these notes. Statements below paraphrase Google; procedural choices in SKILL.md are authored analysis guidance, not Google requirements.

## 1. Structure, grouping and limits

Source: [How blends work](https://docs.cloud.google.com/data-studio/how-blends-work), read 2026-10-11; updated 2026-10-07.

A blend supports five tables. Included dimensions define grouping before joins; a unique ID dimension can preserve record rows. Source metrics become numeric dimensions. Join conditions compare equality, regardless of field names. Blends belong to their report, copy with it, and inherit credentials and freshness from their sources. Hiding repeated join fields affects field visibility, not duplicate-match removal. These facts explain why a SQL join of raw exports is an inadequate reproduction.

## 2. Ordering, filters and inherited settings

Source: [Blending tips and advanced concepts](https://docs.cloud.google.com/data-studio/blending-tips-and-advanced-concepts), read 2026-10-11; updated 2026-10-07.

Joins evaluate left to right. All included blend fields are computed, even those absent from the chart. Explicit table restrictions apply before joins, chart restrictions afterward. Inherited filters apply before blending when source-compatible, otherwise afterward when blend-compatible, otherwise are ignored. The documented inherited-filter sequence is table grouping, compatible source filters, joins, chart grouping, then compatible chart metric filters.

Multiple matches increase joined rows. Cross joins may cause a too-much-data error. Compute the Cartesian product; do not repeat the page's unconditional product-versus-sum comparison, which fails for small or empty tables.

## 3. Field placement and editor behavior

Source: [Create, edit, and manage blends](https://docs.cloud.google.com/data-studio/create-edit-and-manage-blends), read 2026-10-11; updated 2026-10-07.

A table calculation sees only that table. Cross-table calculations belong in the chart after components are included. Auto table date range follows the chart; Custom overrides it. Moving tables can invalidate joins. A pink Missing join field must be added to its table or removed/replaced. Automatically blending two scorecards creates a ratio: first selected is numerator, second is denominator. The chart's data-source edit icon opens blend editing; Google's page also lists Resources > Manage blends and variant menu wording.

## 4. Aggregation meanings

Source: [Aggregation](https://docs.cloud.google.com/data-studio/aggregation-article), read 2026-10-11; updated 2026-10-07.

Chart aggregation can override a source default. SUM adds values, COUNT counts values and COUNT DISTINCT counts unique values. Auto cannot be changed; it may come from a preaggregated connector or from an explicit aggregate formula. None treats a numeric field as a dimension. Fewer grouped rows do not by themselves imply that an additive measure disappeared.

## 5. Chart calculation constraints

Source: [About calculated fields](https://docs.cloud.google.com/data-studio/about-calculated-fields), read 2026-10-11; updated 2026-10-07.

Chart-specific fields support blended data and cannot reference another chart-specific calculation. They require report edit rights and Field Editing in Reports enabled in the data source. Explicit aggregated formulas preserve the intended evaluation, for example a ratio of summed additive components. A chart-level field exists in that chart; a copied chart carries its fields, but creating one does not add it to the source.

## 6. Join and source errors

Source: [Troubleshoot errors in Data Studio](https://docs.cloud.google.com/data-studio/troubleshooting-guide), read 2026-10-11; updated 2026-10-07.

Error phrases to recognize: incomplete join configuration, missing join condition, incomplete join key, pink Missing field, and a table missing its data source. Repair corresponding fields/operators; cross joins intentionally have no condition. Reconnect a missing table source and check field validity. Invalid metric/dimension combinations can be source-schema restrictions, so do not infer fanout from that error alone. Capture the actual details rather than treating every configuration error as one cause.

## 7. Connector ratio errors

Source: [Unable to aggregate ratio metrics](https://docs.cloud.google.com/data-studio/what-does-the-unable-to-aggregate-ratio-metrics-error-mean), read 2026-10-11; updated 2026-10-07.

Connector ratios can arrive already aggregated. Filtering a calculated dimension may demand a recomputation that the product cannot perform. Google's example repairs this with a supported original-dimension filter or a non-ratio metric. Re-aggregating metrics is not supported is a separate source-level restriction; SUM around an Auto connector metric is not a general repair. Raw numeric Sheets components have different capabilities. Confirm field aggregation and filter scope before choosing a formula.

## 8. Zero and missing-value formula behavior

Sources: [CASE (Searched)](https://docs.cloud.google.com/data-studio/case-searched) and [Operators](https://docs.cloud.google.com/data-studio/operators), read 2026-10-11; both updated 2026-10-07.

A CASE without ELSE returns NULL when no condition is true. The != comparison is supported; comparisons and arithmetic normally return NULL with a NULL operand. A nonzero aggregate-denominator guard prevents division by zero but does not detect individual missing rows that SUM can omit. Coverage must be checked separately.

## Authored reconciliation guidance

No universal deduplication fix follows from these docs. Reproduce the configured grouping, join multiplicity and chart calculation using complete supplied rows. Preserve the user's metric definition; a matching grand total alone is insufficient if populations or row detail change. Treat zero denominators as undefined, not zero. Where the required grains conflict, separate charts or a clearly specified upstream grouped export can preserve meaning.
