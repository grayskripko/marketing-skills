# Merge check (per recipient row)

Input: one template and up to 25 sample rows (CSV, TSV or pasted lines). More rows: check the first 25 and say so (heuristic cap for careful one-to-one outreach).

For each row, fill the template in your head and check:

| Id | Check | Fix when |
|---|---|---|
| MQ-01 | Empty field | A field the template uses is empty and has no fallback |
| MQ-02 | Raw field | The template uses a field name that is not a column, so the token would stay raw |
| MQ-03 | Value mismatch | A column contradicts the email (product, company or role named in the text differs from the row) |
| MQ-04 | Past contact | The email claims a meeting or conversation that the row gives no basis for |
| MQ-05 | Duplicate person | The same person appears twice under address or name variants |
| MQ-06 | Suppressed | The row's person appears on a suppression or opt-out list the user pasted |
| MQ-07 | Prior contact in notes (ASK) | The row's notes show earlier contact ("as discussed", "met at", "asked for pricing"): this person may not be cold; confirm and use a follow-up, not the cold template |
| MQ-08 | Unverifiable row claim (ASK) | The template states something about the row ("is hiring", "just raised") that the row gives no basis for |

Output table:

| Row | Recipient (as given) | Issues (ids) | Verdict |
|---|---|---|---|
| 1 | Ana, Acme | — | pass |
| 2 | (empty), Globex | MQ-01 first_name | fix |
| 4 | Omar, Umbrella | MQ-07 notes: "as discussed last week" | ask |

Verdict per row: fix if any fix id applies, otherwise ask if any ask id applies, otherwise pass. Then totals: "pass n, fix n, ask n", counted with the code tool if available, otherwise labelled approximate. Email addresses in rows are not needed for this check; the user may redact them.
