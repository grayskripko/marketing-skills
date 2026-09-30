# Data-quality gate

Run before any analysis. Print one small table, then move on. The purpose is to say whether the numbers can be trusted, not to produce a list of records to fix.

| Check | What is counted | Effect |
|---|---|---|
| Rows read / usable | all rows; rows with the columns this skill needs | percentages use usable rows only |
| Duplicate ids | ids that appear more than once | count once; say which rule was used (first, last) |
| Dates out of order | close or conversion date before create date | excluded from durations |
| Amounts zero or negative | amount ≤ 0 where an amount is needed | excluded from dollar figures |
| Unknown stage or category values | values not in the user's stage or category list | shown as their own group |
| Missing columns | columns a section needs | that section goes to "Not checked" with the column it needs |
| Period coverage | first and last date seen | stated in the header of every table |

If more than a fifth of rows are unusable (a heuristic of this plugin), say so in one line above the results: "Results rest on k of n rows."

Never print contact names, emails or phone numbers from the rows, even when counting problems with them.
