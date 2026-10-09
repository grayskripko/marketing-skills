# Column roles

Every column gets exactly one role. In the answer, mention a role only when it changes the result or the user asks, in plain words.

| Role | What it holds | Can set a page apart |
|---|---|---|
| page subject | what the page is about: the city, tool, product, integration, model | no |
| sets a page apart | a value that changes what the reader should know or do: price, fee, availability, opening hours, payout time, supported currencies, specifications, counts the business owns, its own review scores, its own case notes | yes |
| swaps words only | the subject repeated in another form, a region name, a synonym, a category label shared by most rows | no |
| unique but useless to the reader | a value that differs on every row but tells the reader nothing to act on: ids, slugs, URLs, coordinates, postcodes, population, founding year used as trivia | no |
| personal contact | personal emails, phone numbers, home addresses | ignored, never repeated |

Rules:
- When unsure whether a column sets a page apart, ask: would a reader on this page decide differently if the value changed? If not, it only swaps words.
- Open-text columns set a page apart only if the text differs between rows by more than the subject and a few swapped words.
- A column that is empty on a row does not count for that row.
- The user may change any column's role; the result is then recomputed.
