# Reference notes

## Technical sources

- Python CSV documentation: https://docs.python.org/3/library/csv.html — read 2026-10-10. A CSV reader returns strings unless numeric conversion is requested; dialects vary. Use a real parser, not line splitting.
- OWASP CSV Injection: https://owasp.org/www-community/attacks/CSV_Injection — read 2026-10-10. Cells starting with =, +, -, @ can execute as formulas in spreadsheet viewers, and CSV quoting does not prevent it. Storing such cells as text in XLSX, or prefixing them with an apostrophe in CSV, are the usual fixes; the prefix changes the stored value.

## Cleanup recipe

When the user wants a repeatable cleanup, a recipe usually records: input columns and their mapping, which columns are IDs kept as text, date and number conventions, join key, duplicate rule, output format and columns. Save only what the user will reuse.
