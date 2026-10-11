# Similarity method

Computed with the host's code tool when available. All thresholds are rules of thumb of this plugin.

## Steps

1. Visible text only. Drop navigation, footer and script text if they were pasted.
2. Split into sentences at `.`, `!` or `?` followed by a space and an upper-case letter, at line breaks, or at the end of the text. Never split between two digits (so "0.8" stays whole) or inside a placeholder such as `{{city}}` or `[DATA NEEDED]`.
3. Lower case. Replace the page's subject (city, tool, product), and any variants the user lists, with `<ITEM>`.
4. Name-swap check before stripping: Default: when one identical masked-text cluster contains at least max(2, ceil(0.80 × n)) pages, report its members as a dominant name-swap cluster and omit only its redundant internal comparisons. Check every remaining page normally and keep separate clusters separate. Say the entire sample is one name-swapped page only when all n pages belong to the same cluster. State membership, count and selected branch.
5. Template strip: Default: strip sentences present in at least ceil(0.80 × n) pages within one supplied template/category group; use n of n when n<5. Preserve repeated sentences that supplied rows identify as decision-relevant facts, even above the threshold. State group size, occurrence threshold and retained fact sentences; list removed sentences.
6. Shared tokenisation for variable share and shingles: split text on whitespace and punctuation and drop empty tokens. Tokenise numerator and denominator identically. Numbers split here ("1.2%" becomes "1", "2"); the separate number-check regex below preserves decimal facts.
7. Variable share: remainder tokens divided by all tokens of the page after step 3 (same tokenisation). Print it per page against the default 40% prose target; use the complete-fact-table test for supplied structured lookup pages with every required field present, and say which was used.
8. Remainder length: default fewer than 50 tokens triggers fact review and exclusion from the prose matrix. Keep complete table-led pages only when every required task field is present and profile eligibility passes; report count and selected check. Never fabricate a Jaccard score for excluded pages.
9. Shingles: sets of five consecutive tokens for prose with at least 50 remainder tokens. For complete table-led pages or text this tokeniser cannot represent, use normalised field comparison, profile eligibility and exact-copy checks; no Jaccard cutoff applies. State the selected method; do not substitute a three-token score.
10. Jaccard similarity for each pair: shared shingles divided by all distinct shingles of the two pages. Default: print 2 decimals; use extra digits or exact shared/union counts when rounding obscures a threshold, and state that unrounded values decided the verdict.

Exact counts: when the host has no code tool, count by hand and say so; default: recount manually computed percentages within 5 percentage points of a threshold (0.05 for Jaccard). Use exact recomputation for every decision-changing figure when a computation tool is available or a one-cell change can flip the verdict; say which values were checked.

## Number check

Extract numbers, decimals and percentages included, from the page text with the pattern `\d+(?:[.,]\d+)?%?` (so "1.2%" stays "1.2%"). Remove thousands separators on both sides ("1,200" and "1200" match), then compare with the values in the user's pasted row for that page. A number that is not in the row is unsupported.

## Flags

| Flag | Rule |
|---|---|
| review | default unrounded five-token Jaccard >=0.60 and <0.80; review facts before action |
| near-duplicate | default unrounded five-token Jaccard >=0.80; apply the fact-review action exception below |
| name-swap copy | the masked text is identical to another page's (step 4) |
| too little own text | below the default 40% prose target (use the complete-fact-table test for structured lookup pages meeting its conditions; state which was used) |
| thin | below the default 50-token prose screen, unless the stated complete-fact-table exception applies |
| missing data | `[DATA NEEDED`, `{{`, `TBD` or similar placeholders remain in the text |
| unsupported number | a number on the page that is not in the user's pasted row for that page (only when rows are pasted) |

## Actions

- No flag: keep.
- Review or too little own text: keep; add missing decision-relevant row data before expansion. For qualifying complete table-led pages or materially different supplied decision facts fully answering the task, keep without padding and state the actual share/facts and selected exception.
- Name-swap copies: merge into the hub, or `noindex, follow` if users need the page. For near-duplicates, keep only when materially different supplied decision facts fully answer the task and profile eligibility passes; otherwise use the same merge/noindex action. For thin pages below 50 tokens, keep a complete table-led page only when all required task fields and profile eligibility pass; otherwise use the same action. Name the deciding facts, count and selected exception; shared wording or length alone does not justify removal.
- Missing data or unsupported number: do not publish until fixed; this hold overrides every keep exception.
