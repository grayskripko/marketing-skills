# Viability rules

All thresholds here are rules of thumb of this plugin; in the answer they appear as plain recommendations (ground rule 4).

## Profiles

A row's profile is its values in the columns that set a page apart. Rows with the same profile would be the same page under different names; they share one page. A single row is a profile of one, not a duplicate.

## Which profiles earn a page

Apply the following eligibility test:
- Default: require 3 filled independent decision-relevant facts and differences on 2 jointly filled decision-relevant fields from every other profile. Use 2 filled facts and 1 differing field only when supplied user tasks or customer questions show that this field alone changes the required action and the page fully answers that task. Name the task, field, counts and selected test. Missing values, identifiers and correlated restatements never count as differences or extra facts; identical profiles still share one page.

Edge cases:
- Two profiles are compared only on columns both have filled.
- Default: apply the 3-fact/2-difference test and merge one-field variants; use the 2-fact/1-difference task exception defined above when the supplied data meets it. State which test was used.
- Being the most common profile is not a fault; it is judged like any other.
- Default: apply the 3-fact/2-difference test and merge one-field variants; use the 2-fact/1-difference task exception defined above when the supplied data meets it. State which test was used.

## Verdict (no gaps)

Page share = pages earned ÷ rows pasted. Compared before rounding, printed with 1 decimal by default; use extra digits or exact counts when rounding obscures a boundary and say unrounded values decided the verdict.

| Verdict | Rule |
|---|---|
| Build qualifying profiles | page share >=70% |
| Build some plus hub | page share >=20% and <70% |
| One hub page instead | page share <20% |

Default: page share >=70% means build qualifying profiles; 20% to <70% means build named qualifying profiles plus a hub; <20% means start with a hub. For supplied page types or categories with distinct purposes, calculate these bands within each group and state its denominator. Below 20%, use a hub plus named qualifying profiles only when supplied relevant queries or necessary user destinations justify those profiles; name the evidence. Never infer demand or create pages for failed profiles. List actual pages and the rows they cover; the label does not override eligibility.

## Output per verdict

- Default at page share >=70%: build qualifying profiles, one page per profile that earns one; use hub plus named qualifying profiles under the supplied-demand/navigation exception even below 20%, and state the plan used; rows sharing a profile share its page. The template still needs a specification and a sample check.
- Build some: list each page and the rows it covers. The other rows go into one hub page with a table of all rows, or stay unbuilt until their data is filled.
- One hub page instead: one hub page with a filterable table, or a small number of broader pages grouped by one column that sets pages apart.

## Sample size

Default: below 30 rows, label an incomplete list "small sample; result covers these rows only". Use "complete supplied list" when the user confirms these are all planned rows, regardless of count; still flag unrepresented categories when an incomplete sample of any size omits them. Say which coverage status was used.
