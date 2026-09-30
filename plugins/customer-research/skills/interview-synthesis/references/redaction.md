# Redaction and personal data

This file is identical in every skill of the plugin. Apply it to every table, quote and summary you output.

## Tokens

These are the only edits allowed inside a verbatim quote.

| Found in the input | Output | Example |
|---|---|---|
| A person's name (participant, colleague, customer contact) | Role label or source id | "Maria said…" → "[NAME: ops lead]" or "S04" |
| A person's email, phone number, street address or personal handle | `[CONTACT]` | "write me at j.doe@…" → "write me at [CONTACT]" |
| A customer's company name | `[COMPANY: segment description]`, keeping firmographics | "at Brightwell" → "at [COMPANY: accounting firm, ~40 staff, UK]" |
| Health, religion, political views, union membership, sexual orientation, ethnicity, criminal records, biometric data, and similar special-category details | `[SENSITIVE]` | "after my surgery I fell behind" → "after [SENSITIVE] I fell behind" |

Keep: industry, size band, region, role or job title, tools and workflows the company uses, plan, tenure. These are what make B2B research useful and do not identify a person on their own.

If a segment description plus role would match only one or two accounts in the input, widen the size band or region (for example "10–50 staff, UK" instead of "12 staff, Leeds") and say once that you widened it.

Customer account or record ids the user supplies (CRM ids, account numbers) identify a company record, not a person. Keep them as given, or map them to C-ids and print the mapping table so the user can trace every row back.

Special-category details are never analysed, coded or counted. Say once in the output that they were replaced.

## Ids

- Interview or call sources: S01, S02 … in input order. Quotes: S03-Q07 (source 3, quote 7).
- Short feedback items (reviews, tickets, survey answers): F001, F002 …
- Churn or cancellation records: C01, C02 …
- Lost deals: L01, L02 …

Ids are pseudonyms. Someone with the original files can link them back, so the output is not anonymous. Never claim that the output is anonymised or compliant with any law.

## Matching quotes after redaction

The self-check compares each ledger quote with the input after the same redaction has been applied to the input. A token in a quote is therefore never counted as a mismatch. An excerpt joined with "…" is matched part by part: each part must appear verbatim.

## Data minimisation

- Ask for no personal detail the task does not need. A role label is enough to analyse an interview.
- Every output includes the fixed line "Reminder: remove personal data you do not need before pasting." directly under its first table (sources, frame or records).
- Never build a profile of a named person, and never list people to contact.

## Consent note (practice, not legal advice)

When a note or interview template is produced, include one line: ask the participant before recording, and say how notes will be kept and who will see them.
