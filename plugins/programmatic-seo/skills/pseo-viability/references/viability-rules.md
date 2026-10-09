# Viability rules

All thresholds here are rules of thumb of this plugin; in the answer they appear as plain recommendations (ground rule 4).

## Profiles

A row's profile is its values in the columns that set a page apart. Rows with the same profile would be the same page under different names; they share one page. A single row is a profile of one, not a duplicate.

## Which profiles earn a page

A profile earns a page when both hold:
- at least 3 columns that set a page apart are filled with real values (not empty, N/A or TBD); and
- it differs from every other profile on at least 2 of those columns.

Edge cases:
- Two profiles are compared only on columns both have filled.
- Two profiles that differ on only one column share one page that shows the difference in a small table.
- Being the most common profile is not a fault; it is judged like any other.
- With fewer than 3 columns that set pages apart, no profile can earn a page; say so and go straight to the verdict.

## Verdict (no gaps)

Page share = pages earned ÷ rows pasted. Compared before rounding, printed with one decimal.

| Verdict | Rule |
|---|---|
| Build all | page share at least 70% |
| Build some | page share at least 20% and below 70% |
| One hub page instead | page share below 20% |

## Output per verdict

- Build all: one page per profile that earns one; rows sharing a profile share its page. The template still needs a specification and a sample check.
- Build some: list each page and the rows it covers. The other rows go into one hub page with a table of all rows, or stay unbuilt until their data is filled.
- One hub page instead: one hub page with a filterable table, or a small number of broader pages grouped by one column that sets pages apart.

## Sample size

With fewer than 30 rows, add "small sample; the result may change on the full list".
