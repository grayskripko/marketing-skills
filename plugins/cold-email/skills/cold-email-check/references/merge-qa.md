# Merge check (per recipient row)

Input: one template and up to 25 sample rows (CSV, TSV or pasted lines). More rows: check the first 25 and say so (heuristic cap for careful one-to-one outreach).

Fill the template with each row and check:

| Id | Check | Fix when |
|---|---|---|
| MQ-01 | Empty field | A field the template uses is empty and has no fallback |
| MQ-02 | Raw field | The template uses a field name that is not a column, so the token would stay raw |
| MQ-03 | Value mismatch | A column contradicts the email (product, company or role named in the text differs from the row) |
| MQ-04 | Past contact | The email claims a meeting or conversation that the row gives no basis for |
| MQ-05 | Duplicate person | The same person appears twice (same name and company, or the same address if addresses were given) |
| MQ-06 | Suppressed | The row's person appears on a suppression or opt-out list the user supplied |
| MQ-07 | Prior contact in notes (ASK) | The row's notes show earlier contact ("as discussed", "met at", "asked for pricing"): this person may not be cold; confirm and use a follow-up, not the cold template |
| MQ-08 | Unverifiable row claim (ASK) | The template states something about the row ("is hiring", "just raised") that the supplied evidence does not establish in full, including the relevant role and current tense; a notice label/date alone is insufficient. If a dated notice supports it, rewrite to past tense with the date instead |

Output table:

| Row | Recipient (name or company as given; never an address) | Problem | Verdict |
|---|---|---|---|
| 2 | (empty), Globex | first_name is empty and has no fallback | fix |
| 4 | Omar, Umbrella | notes say "as discussed last week": may not be cold | ask |

Verdict per row: hold if any factual, consent, suppression or required-footer blocker remains; explain the fix or verification needed. A source label/date does not verify a claim. Pass only when all applicable blockers are resolved. Print only rows with a problem (unless the user asked for a verdict on every row); rows that pass are not counted. Ids are for your own use. Email addresses in rows are not needed for this check; the user may redact them.
