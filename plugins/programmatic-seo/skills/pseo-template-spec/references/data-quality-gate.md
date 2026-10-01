# Data-quality gate

Runs before any score. It answers "can these rows support a decision", not "here is what to clean".

Print one table:

| Check | Result |
|---|---|
| Rows, columns | counts |
| Key column | name; number of distinct keys; duplicate keys listed by count |
| Empty share per column | percent of rows empty, one decimal |
| Placeholder values | cells such as N/A, TBD, "-", "lorem", "sample", "x" counted as empty |
| Personal contact columns | names of columns that hold personal emails, phones or home addresses; marked "ignored" |
| Rows pasted vs rows planned | if the user says the full set is larger, say the result covers the pasted rows only |

If more than half the rows of a distinguishing column are empty, say so before the verdict: that column cannot carry pages until it is filled.
