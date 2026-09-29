# Output format for copy-edit

## 1. Fact-lock table (printed first)

| F-id | Locked item | Position before | Present after | Changed? |
|---|---|---|---|---|
| F1 | 40% (invoice time cut) | 1.2 | yes | no |
| F2 | "Our AP team closed March two days early" (Priya, Globex Billing) | 3.1 | yes | no |
| F3 | Northwind Ledger | 1.1 | yes | no |

- Position is paragraph.sentence in the original draft.
- "Present after" is yes or cut. A cut must appear in the change log with its reason.
- "Changed?" must be "no" in every row. If any row would read "yes", undo that edit.

## 2. Change log (printed before the clean text)

| # | Before (up to 12 words) | After | Pass | Rule | Reason |
|---|---|---|---|---|---|
| 1 | "a revolutionary platform that empowers teams to cut" | "a platform that lets teams cut" | P5 | SP-06 | Praise adjective and empowerment verb carry no information; the claim itself is unchanged |
| 2 | "cut invoice time by 40%" | "cut invoice time by 40% [PROOF NEEDED: source and period]" | P4 | P4.1 | Number kept unchanged; source missing |
| 3 | "Learn more" | "See how matching works [DETAIL NEEDED: what the button leads to]" | P8 | P8.2 | The call to action names what the reader sees next; the destination must come from the user |

- One row per change. Merge only identical changes repeated in several places ("same change in 4 places").
- The reason is one short sentence about the reader, not about style preferences.

## 3. Clean text

The full edited text, with markers left in place.

## 4. Before/after counts

| Measure | Before | After |
|---|---|---|
| Words | | |
| Sentences with "we/our/us" as subject | | |
| Sentences with "you/your" as subject | | |
| SP-xx hits | | |
| Unsourced claims | | |
| Open markers | | |

Label the table "approximate" unless a code tool computed it.

## 5. Open markers and suggested additions

- Every `[PROOF NEEDED: …]` and `[DETAIL NEEDED: …]` with its location.
- Suggested additions (need your source): claims that would help the page if the user can back them.

## 6. Assumptions

What the edit assumed about the reader, the goal or the facts.
