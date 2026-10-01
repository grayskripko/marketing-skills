# Viability rules

All thresholds here are heuristics of this plugin, printed with that label.

## UV score per row

For each distinguishing column, find its most common value across the pasted rows (the mode). If the most frequent value appears only once, the column has no mode: every filled value counts. If several values tie for most frequent, all of them count as common (no point). A row earns one point for every distinguishing column where its value is filled and not a common value. The UV score is the sum.

A row passes when its UV score is at least 3. With fewer than 3 distinguishing columns no row can pass; say so and go straight to the verdict.

## Duplicate groups

Rows identical on every distinguishing column form a group. The largest group's share of all rows is printed.

## Verdict bands (no gaps)

| Band | Rule |
|---|---|
| Go | pass share at least 70% and the largest duplicate group holds at most 5% of rows |
| Narrow | pass share at least 20% and below 70%, or pass share at least 70% with a duplicate group above 5% |
| No-go | pass share below 20% |

Percentages are compared before rounding and printed with one decimal.

## Outputs per band

- Go: the full set may be built; the template still goes through a template specification and a sample check.
- Narrow: list the ids or keys of the passing rows as the page set, keeping only the first row of any duplicate group (the others would be identical pages); print which rows were dropped for that reason. The other rows go into one hub page with a table, or stay unbuilt until their data is filled.
- No-go: one hub page with a filterable table, or a small number of broader pages grouped by a distinguishing column.

## Sample size

If fewer than 30 rows are pasted, add "thin sample, a heuristic of this plugin; the verdict may change on the full set".
