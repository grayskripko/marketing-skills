# Column classes

Every column gets exactly one class. Print the class with a one-line reason and an example value.

| Class | What it holds | Counts toward the UV score |
|---|---|---|
| key | what the page is about: the city, tool, product, integration, model | no |
| distinguishing | a value that changes what the reader should know or do: price, fee, availability, opening hours, payout time, supported currencies, specifications, counts the business owns, its own review scores, its own case notes | yes |
| cosmetic | a value that only swaps words: the key repeated in another form, a region name, a synonym, a category label shared by most rows | no |
| inherently unique | a value that differs on every row but tells the reader nothing to act on: ids, slugs, URLs, coordinates, postcodes, population, founding year used as trivia | no |
| personal contact | personal emails, phone numbers, home addresses | ignored, never repeated |

Rules:
- When unsure between distinguishing and cosmetic, ask: would a reader on this page decide differently if the value changed? If not, it is cosmetic.
- Open-text columns count as distinguishing only if the text differs between rows by more than the key and a few swapped words; otherwise cosmetic.
- A distinguishing column that is empty on a row does not count for that row.
- The user may reclassify any column; the scores are then recomputed.
