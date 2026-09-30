# Fact table template

| Fact id | Prospect | Fact | Source | Date | Age |
|---|---|---|---|---|---|
| P1-F1 | Acme (Head of Finance) | Posted an AP clerk opening | User note, line 3 | 2026-09-12 | 18 days |
| P1-F2 | Acme | Opened a second office | acme.test/news | undated | unknown |

- Fact ids: P(prospect number)-F(fact number).
- Source is the note line or the URL the user gave. Never a guess.
- Age is computed from the date against today; "undated" facts may be kept but score at most 1 unless clearly current.
- People appear by role; names only as the user gave them. No email addresses are needed.
