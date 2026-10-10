# Sources and scope

All URLs below were opened or retrieved as full source text on 2026-10-10 (read 2026-10-10). They document product behavior, not directory approval.

- [Microsoft merge overview](https://learn.microsoft.com/en-us/power-query/merge-queries-overview) — Join types differ in retained sides; matching columns drive nested table rows; expansion and aggregation are distinct.
- [Microsoft Table.NestedJoin](https://learn.microsoft.com/en-us/powerquery-m/table-nestedjoin) — Returns matching rows in a nested column; unspecified join kind defaults to left outer.
- [Microsoft Table.Distinct](https://learn.microsoft.com/en-us/powerquery-m/table-distinct) — A particular duplicate is not guaranteed to survive without additional controls.
- [Microsoft Table.TransformColumnTypes](https://learn.microsoft.com/en-us/powerquery-m/table-transformcolumntypes) — Culture controls conversion; absent columns error by default; MissingField options can alter handling.
- [Microsoft error handling](https://learn.microsoft.com/en-us/power-query/error-handling) — try produces a record with HasError and either Value or Error, enabling row-specific error handling.
- [Microsoft identifier preservation](https://support.microsoft.com/en-us/excel/keeping-leading-zeros-and-large-numbers) — Text preserves supplied IDs; automatic numeric conversions can remove zeros or change large numbers.

- [Microsoft M language types](https://learn.microsoft.com/en-us/powerquery-m/m-spec-types) — read 2026-10-10; record/table field types and nullable type syntax used in manual review of generated M proposals.

Authored workflow rules, this plugin's rules of thumb: smallest useful patch; paste location and copy checks; no blanket error masking; explicit match rule; preservation of raw/ambiguous records; next-file checks; reconciliation before a reported total; text-only proposals and no fetch/file/account access. These are design choices, not vendor requirements. Month boundaries and weighted total margins follow the stated date/ratio definitions; no arbitrary performance threshold is used.
