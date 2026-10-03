# Call statistics: counting rules

All figures are recomputable from the transcript. Print the rule with the figure. Use the host's code tool when available; otherwise label each figure "counted by hand — check".

## Gate (before any count)

| Check | If it fails |
|---|---|
| Speaker labels on each line | stats "not computed"; the rubric still runs on quotes |
| Which label is the seller | ask once; until answered, stats are "not computed" |
| Timestamps | time-based figures and thirds by time are skipped; thirds use word position instead |
| Language | non-English: say question detection may be less reliable |
| Length | under about 300 words: stats are printed with "short excerpt" |

## Definitions

- **Word**: a whitespace-separated token in the spoken text, after removing the speaker label and timestamp.
- **Turn**: consecutive lines by the same speaker, merged into one. Turn numbers count merged turns from 1.
- **Seller word share** = seller words ÷ all words, one decimal. With several seller-side speakers, their words are added up and the speakers named. If timestamps allow, also report time share = seller speaking seconds ÷ call seconds, where a line lasts until the next line's timestamp.
- **Seller question**: a seller sentence ending in "?".
- **Open or closed** by the first word of the question, after dropping any initial "so", "and", "but", "ok", "okay", "right", "well", "um", "uh" and commas:
  - open: what, how, why, which, who, where, when, tell, walk, describe, talk, help;
  - closed: do, does, did, is, are, was, were, can, could, would, will, should, have, has, had, shall, may, might, any, isn't, aren't, don't, doesn't, didn't, won't, wouldn't, can't, couldn't;
  - anything else: unclassified.
  Print the full list of seller questions with their label so the user can correct misses (e.g. "what about Tuesday?" is open by the rule but works as closed).
- **Thirds**: split the call into three equal time spans from the first to the last timestamp (or three equal spans of total word position when there are no timestamps); count seller questions in each.
- **Longest seller turn** and **longest buyer turn**: words in the longest merged turn, with its turn number.
- **Next-step test**: date ✓/✗, owner ✓/✗, buyer agreement quoted ✓/✗, taken from the last third of the call.

## Targets

None by default. If the user gives a target (e.g. "seller share under 50%"), print the target, the figure and met or missed, compared before rounding. Never supply a target from outside the user's data.

## Several calls (2 to 5)

Report stats per call side by side. No averages when there are fewer than 3 calls; with 3 or more, print the median and the range, not a mean.

## Worked example

A discovery call of 31 lines (28 turns after merging).
- Words: 413 in total, Seller-1 253; share 253 ÷ 413 = 61.3%.
- Seller questions: 9; open 5 ("How does your team handle incoming tickets today?", "Who handles that on your side?" and three more), closed 3, unclassified 1 ("Anything else on your mind…?"); by thirds 5 / 2 / 2.
- Longest seller turn: 109 words, turn 17 at 07:40 (four seller lines merged). Longest buyer turn: 29 words, turn 4 at 00:55.
- Next-step test: date no, owner no, buyer agreement yes ("Sounds good.").
