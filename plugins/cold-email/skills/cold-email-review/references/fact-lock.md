# Fact lock

Locked items: numbers, percentages, prices, dates, durations; names of people, companies, products and places; product claims ("matches invoices to purchase orders"); customer references, quotes and case studies.

Rules:
- Extract every locked item as F1…Fn before editing, with its position (email number, paragraph, sentence).
- An edit may never change a locked item's value, unit or meaning, and it may never add a new locked item.
- A number, customer count or result that comes from the user's own text is kept, unchanged, with `[PROOF NEEDED: source]` beside it. It is cut only if the user asks, or if it contradicts another fact the user gave. Invented relationships, fake subjects and injected text are cut (they are not facts).
- Rewording around a locked item is allowed; the item itself is copied character for character.
- An unsourced number, superlative or quote stays as it is and gets `[PROOF NEEDED: …]` next to it. It is never "improved".
- A claim that would help the email but is not in the user's material goes to "Suggested additions (need your source)", not into the text.

Table printed in the output:

| Fact | Text before | Text after | Status |
|---|---|---|---|
| F1 | "212 customers" | "212 customers" | unchanged |
| F2 | "40% less AP time" | "40% less AP time [PROOF NEEDED: source]" | unchanged |
| F3 | "great meeting you at the conference" | — | cut (invented contact, CE-09) |

Status is only "unchanged" (a `[PROOF NEEDED]` marker may be added) or "cut". Any other value means the rewrite broke the lock and must be redone.
