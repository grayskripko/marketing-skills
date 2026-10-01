# Similarity method

Computed with the host's code tool when available. All thresholds are heuristics of this plugin.

## Steps

1. Visible text only. Drop navigation, footer and script text if they were pasted.
2. Split into sentences at `.`, `!` or `?` followed by a space and an upper-case letter, at line breaks, or at the end of the text. Never split between two digits (so "0.8" stays whole) or inside a placeholder such as `{{city}}` or `[DATA NEEDED]`.
3. Lower case. Replace the page's key value, and any variants the user lists, with `<KEY>`.
4. Key-only check, before any stripping: a page whose masked text is identical to another page's masked text is a key-only variation. If at least 80% of the samples are key-only variations of one another, report "the sample is one page with the key swapped" and skip the matrix; the remaining steps would strip everything.
5. Template strip: a normalised sentence that appears in at least 80% of the samples is removed from every page. Print the removed sentences.
6. Tokens for shingles: split the remainder on whitespace and punctuation, drop empty tokens. Numbers become separate tokens here ("1.2%" becomes "1", "2"); this is for shingles only.
7. Variable share: remainder tokens divided by all tokens of the page after step 3 (same tokenisation). Print it per page against the 40% target from the template specification.
8. Remainder length: fewer than 50 tokens means the page is flagged thin and is left out of the matrix.
9. Shingles: every run of five consecutive tokens.
10. Jaccard similarity for each pair: shared shingles divided by all distinct shingles of the two pages. Print with two decimals.

Exact counts: when the host has no code tool, count by hand and say so; recount any figure within 5 points of a threshold.

## Number check

Extract whole numbers from the page text with the pattern `\d+(?:[.,]\d+)?%?` (so "1.2%" stays "1.2%") and compare them with the values in the user's pasted row for that page. A number that is not in the row is unsupported.

## Flags

| Flag | Rule |
|---|---|
| review | highest Jaccard at least 0.60 and below 0.80 |
| near-duplicate | highest Jaccard at least 0.80 |
| key-only variation | the masked text is identical to another page's (step 4) |
| low variable share | variable share below 40% |
| thin | remainder below 50 tokens |
| missing data | `[DATA NEEDED`, `{{`, `TBD` or similar placeholders remain in the text |
| unsupported number | a number on the page that is not in the user's pasted row for that page (only when rows are pasted) |

## Actions

- No flag: keep.
- review or low variable share: keep, and add distinguishing data before the next batch.
- near-duplicate, key-only variation or thin: merge into the hub, or `noindex, follow` if the page must exist for users.
- missing data or unsupported number: do not publish until fixed.
