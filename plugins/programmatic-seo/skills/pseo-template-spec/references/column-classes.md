# Column roles

Every column gets exactly one role. In the answer, mention a role only when it changes the result or the user asks, in plain words.

| Role | What it holds | Can set a page apart |
|---|---|---|
| page subject | what the page is about: the city, tool, product, integration, model | no |
| sets a page apart | a value that changes what the intended page visitor should know or do: price, fee, availability, opening hours, payout time, supported currencies, specifications, counts the business owns, its own review scores, its own case notes | yes |
| swaps words only | the subject repeated in another form, a region name, a synonym, a category label shared by most rows | no |
| record identifier or incidental fact | ids, slugs and URLs alone do not establish useful content; location or other facts count only when they change the reader's decision for this page purpose | context-dependent |
| personal contact | personal emails, phone numbers, home addresses | ignored, never repeated |

Rules:
- When unsure whether a column sets a page apart, ask: would an intended page visitor on this page decide differently if the value changed? If not, it only swaps words.
- Open-text columns set a page apart only if the text differs between rows by more than the subject and a few swapped words.
- A column that is empty on a row does not count for that row.
- Reassess a column's role using the requesting user's page purpose and supplied evidence, then recompute affected results. Personal-contact columns remain ignored.
