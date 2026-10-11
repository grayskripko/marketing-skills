# Data check

Runs before any verdict. It answers "can these rows support a decision", not "here is what to clean".

Checks:
- rows and columns;
- the subject column: number of distinct names, repeated names listed with counts;
- empty and confirmed placeholder cells; TBD is unknown, while N/A, "-" or other ambiguous markers require their field meaning before being counted as missing;
- personal contact columns (personal emails, phones, home addresses): named and marked "ignored";
- rows pasted vs rows planned: if the user says the full set is larger, the result covers the pasted rows only.

Report only data issues that change the requested answer, next to the affected conclusion. Missing values cannot support claims on those rows; they do not invalidate supplied values on other rows. Do not add a clean-data notice or a missing-share gate.
