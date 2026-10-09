# Data check

Runs before any verdict. It answers "can these rows support a decision", not "here is what to clean".

Checks:
- rows and columns;
- the subject column: number of distinct names, repeated names listed with counts;
- empty share per column, one decimal; placeholder cells (N/A, TBD, "-", "lorem", "sample", "x") count as empty;
- personal contact columns (personal emails, phones, home addresses): named and marked "ignored";
- rows pasted vs rows planned: if the user says the full set is larger, the result covers the pasted rows only.

Report only the checks that found a problem, one line each. If none did, write one line, for example: "6 rows, 5 columns, no gaps or repeated names."

If more than half the rows of a column that sets a page apart are empty, say so before the verdict: that column cannot carry pages until it is filled.
