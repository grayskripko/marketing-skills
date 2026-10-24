# Diagnostic reference register

Read **2026-10-11**; dates are access dates unless stated otherwise. Relevant sources should be checked again before submission around 2026-10-14.

The [semantic register](../../convert-query/references/semantics.md) gives both supplied migration sources, their direction, timestamp/week differences, decimal bounds, parsing contracts and null totals. Use current function definitions to resolve conflicts with a migration overview.

- [Google: operators](https://docs.cloud.google.com/bigquery/docs/reference/standard-sql/operators). IS DISTINCT FROM never yields NULL: two NULLs compare as not distinct, NULL versus a non-null value as distinct. It supports comparable scalar fields, not a whole ARRAY or STRUCT. Ordinary nullable inequality can miss exactly the rows a comparison needs.
- [Google: run queries / dry runs](https://docs.cloud.google.com/bigquery/docs/running-queries#dry-run). The requested dry-run URL redirects to this page. A dry run validates a query and estimates bytes; it is not charged and uses no query slots. It does not execute for results. Account permissions, selected location and table visibility still matter. Choose the actual project and data location in the user's existing console; do not invent those settings.
- [Google: data types, decimal parameters](https://docs.cloud.google.com/bigquery/docs/reference/standard-sql/data-types#parameterized_decimal_type). Values exceeding declared scale are rounded on storage; exceeding precision produces OUT_OF_RANGE. A successful parse does not establish that storing or summing the value is safe. Source precision and expression result types both matter.
- [Google: conversion functions, SAFE_CAST](https://docs.cloud.google.com/bigquery/docs/reference/standard-sql/conversion_functions#safe_casting). A signature/analysis failure is not a runtime bad-string failure. Do not respond to an impossible cast by wrapping it in SAFE_CAST; choose a valid representation or identify the missing type.

Package-specific diagnostic procedure: compare snapshots and grain before blaming functions; retain duplicate occurrences; distinguish absent rows from present NULL values; identify the first changed stage. A total, hash or successful dry run is supporting evidence, not a complete equality proof. User-provided outputs establish only what those outputs show.

## Arithmetic and window checks — accessed 2026-10-11

Use the [fix-source additions](../../convert-query/references/semantics.md#fix-source-additions--accessed-2026-10-11) for the division scale formula, string-SUM conversion errors, DATE subtraction result type, alias visibility and QUALIFY stage. Compare individual quotient values before totals: seven scale-6 rounded 2/7 values give 7 × 0.285714 = 1.999998. A final rounded total does not reproduce that stage. These expectations are derived from documented rules, not captured engine results.

## Present the requested comparison

For duplicate-preserving export comparison, lead with the differing full rows and total missing/extra occurrences. Group each side by all scalar output fields, join with NULL-safe comparisons, and return source/target counts plus separate positive missing/extra counts. Use occurrence counts as presence markers. Equal totals do not identify which charge moved; obtain the report contract and available lineage with both queries and load transformations before fixing the cause.

For a minimal arithmetic fix, show the supplied per-row result and total together: 7 × 0.285714 = 1.999998, whereas rounding the unrounded sum gives 2. Decide whether midpoint uncertainty matters from the supplied denominator/workload bounds, retaining range and intermediate-rounding checks for cases where they can change the result.
