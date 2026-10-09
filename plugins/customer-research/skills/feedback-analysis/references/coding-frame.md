# Coding frame for short feedback

Use for reviews, support tickets, open survey answers and score comments the user pastes or attaches.

## Build the frame

1. Read a sample of about 30 items (all of them if fewer). Draft 6 to 12 codes.
2. Print the frame before coding everything: code, one-line definition, one example id.
3. Code every item. An item may carry up to 3 codes. Items that fit no code go to "other"; if "other" passes 10% of items, add a code and recode.

## Tables to print, in order

These come after the opening answer (the top complaints, each with count, share and ids).

1. **Coding frame:** a table titled "Coding frame" with code, definition, example id. It is always printed in the answer; never say the frame was printed unless this table is present. The personal-data reminder line goes directly under it.
2. **Counts:** code, items, share of items, share of text (words in items with that code ÷ all words), average rating if a rating column exists.
3. **Complaint types** (see `complaint-types.md`), with counts; only types that have items.
4. **Alternatives named by customers:** names exactly as they appear in the items, with counts and ids. Report what the items say; add no judgement and no names of your own.
5. **Splits** by rating, plan or segment when those columns exist.
6. **Representative verbatims:** 1 to 3 per code, with ids, redacted.

## Long-item check

For each code with at least 2 items, compare share of text with share of items. If share of text is more than twice the share of items and at least 10% of all text, flag it: "a few long items carry most of the words". A single item is never flagged. This is a heuristic of this plugin.

## Bias note (always)

Public reviews over-represent very happy and very unhappy customers. Tickets over-represent problems. A run of complaints is not a rate. Say which of these applies to the input.

## Churn and switching mentions

List items that mention cancelling or moving to an alternative separately, with ids. Suggest analysing them as churn records for depth.
