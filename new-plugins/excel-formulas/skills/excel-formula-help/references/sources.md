# Sources and scope

All URLs below were opened or retrieved as full source text on 2026-10-10 (read 2026-10-10). They document product behavior, not directory approval.

- [Microsoft XLOOKUP](https://support.microsoft.com/en-us/excel/functions/xlookup-function) — Excel 2016/2019 excludes XLOOKUP; default exact/first match; reverse is last; binary search requires sorted data.
- [Microsoft MATCH](https://support.microsoft.com/en-us/excel/functions/match-function?error=error_code) — match_type 0 finds the first exact match; INDEX can use its position.
- [Microsoft SUMIFS](https://support.microsoft.com/en-us/excel/functions/sumifs-function) — All criteria hold; each criteria range has the same dimensions as sum_range.
- [Microsoft FILTER](https://support.microsoft.com/en-us/excel/functions/filter-function) — array, include, optional if_empty; matching dimensions and spill output; version list includes 365/2021/2024.
- [Google Sheets XLOOKUP](https://support.google.com/docs/answer/12405947?hl=en) — Sheets supports exact/first and reverse modes; binary modes need sorted ranges. BigQuery syntax differs.
- [Google Sheets FILTER](https://support.google.com/docs/answer/3093197?hl=en) — Conditions follow range; no Excel if_empty slot; no results returns #N/A.
- [Google Sheets SUMIFS](https://support.google.com/docs/answer/3238496?hl=en) — Sums rows meeting all supplied criteria.

Authored workflow rules, this plugin's rules of thumb: smallest useful patch; paste location and copy checks; no blanket error masking; explicit match rule; preservation of raw/ambiguous records; next-file checks; reconciliation before a reported total; text-only proposals and no fetch/file/account access. These are design choices, not vendor requirements. Month boundaries and weighted total margins follow the stated date/ratio definitions; no arbitrary performance threshold is used.
