# Reference notes

The workflow above is this plugin's rule of thumb, not a legal or accounting standard.

## Technical sources

- Python CSV documentation: https://docs.python.org/3/library/csv.html — read 2026-10-10. A CSV reader returns strings unless numeric conversion is requested; dialects vary. Use a real parser, not line splitting. None and empty text need separate handling if their distinction matters.
- OWASP CSV Injection: https://community.owasp.org/attacks/CSV_Injection — read 2026-10-10. Formula-looking cells can execute in spreadsheet viewers. CSV quoting is insufficient and escaping can change after save/reopen. No universal sanitization works for every consumer. This supports the inline target-consumer check; preferring explicitly typed XLSX text is this plugin's rule of thumb. Check text beginning with =, +, -, @, tabs, CR/LF and full-width counterparts. Approved numeric negatives are numbers, not automatically malicious text.

## Recipe and supporting tables

A reusable recipe records version, input identity, selected sheets, encoding/delimiter, headers, column mapping, row meaning, text IDs, date/decimal/time-zone rules, blank semantics, exact join keys and match relationship, duplicate definition and survivor rule, retained new columns, exclusions, output format and formula protection, and verification expectations. Keep user-approved row decisions separate from global rules.

Source map: output row ID → source file identity, sheet, parsed record or worksheet row. A many-source output retains every reference. Change log: source reference, column, before, after, approved rule. Exceptions: source reference, column, issue, supported options, status, decision. Ingestion record: file identity and content fingerprint, covered period if supplied, recipe version, contributing, unresolved and approved excluded source-record counts and references and output identity. These are field suggestions; omit empty logs from the answer.
