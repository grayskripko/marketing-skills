# Call rubric

One rubric and one scale for every skill in this plugin: call coaching, certification role-plays and ramp gates. A user's own rubric may replace the rows; the quote rule, the n/a rule and the pass rule stay.

## Scale

Each scored row gets 0, 1 or 2, using the anchors below (behavioural anchors in the manner of Smith and Kendall, 1963). Every score carries a verbatim quote of at most 25 words with its turn number or timestamp; the demo rows that link a scene to a pain need two quotes, one for each.

- A 0 also needs a quote: the line where the behaviour was due and did not happen (for example the buyer's stated problem with no sizing question after it, or the closing lines for CS-12).
- "not observed": there is no moment to quote either way. No score is given.
- "n/a": the situation never came up (for example the buyer raised no concern, so CS-09 cannot apply; no product was shown, so CS-10 cannot apply; the seller made no outcome claim, so CS-D06 cannot apply). The row leaves the maximum in every mode.

How "not observed" counts depends on the use:

| Use | "not observed" | Verdict |
|---|---|---|
| Coaching a real call | left out of both points and maximum; listed separately | none; coaching is not pass or fail |
| Certification role-play and ramp gates | counts as 0, because the drill gives the rep every chance to show the row | pass rule below |

## Discovery rows (CS-01 to CS-12)

11 rows are scored. CS-11 is a list, not a score. Maximum = 11 × 2 = 22.

| Row | Behaviour | 2 | 1 | 0 |
|---|---|---|---|---|
| CS-01 | Purpose and agenda agreed | seller states purpose and agenda and the buyer agrees or adjusts it | purpose stated, no agreement sought | seller starts without stating why the call exists |
| CS-02 | Current way of working asked before product talk | at least one open question about how the work is done today, followed up until the buyer describes concrete steps, before the first product turn | asked, but answered only in general terms or only after product talk began | not asked before the product appears |
| CS-03 | Problem in the buyer's own numbers | the buyer gives a figure (hours, money, volume, error count) in reply to a seller question | seller asks for a size but accepts a vague answer | a stated problem is left without any attempt to size it |
| CS-04 | Consequence of leaving it unsolved | seller asks what happens if nothing changes, or who is affected, and the buyer answers | asked, buyer deflects, no follow-up | not asked although a problem was stated |
| CS-05 | Who else decides, and how | both the people involved and the way they will decide are asked | only the people, or only the process | not asked |
| CS-06 | Timing and the reason for acting now | the event or date driving the timing is asked and answered | a date is asked with no reason behind it | not asked |
| CS-07 | Alternatives, including doing nothing | seller asks what else is being considered, including staying as is | asks only about competing vendors | not asked |
| CS-08 | Summary in the buyer's words, confirmed | seller summarises using the buyer's terms and the buyer confirms or corrects | summary given, no confirmation sought | no summary |
| CS-09 | A concern is explored before it is answered | seller asks what is behind the concern before replying | seller acknowledges, then answers without asking | seller answers or argues at once |
| CS-10 | Product shown only after a stated problem was explored | before the first product turn the seller asked at least one follow-up on a stated problem and the problem was sized (CS-03 evidence earlier in the call) | at least one follow-up question on a stated problem, but no size, before the first product turn | product shown while every stated problem was still unexplored |
| CS-11 | Claims made | list only: every number, comparison, customer reference or promise the seller stated, with "proof needed?" | | |
| CS-12 | Specific next step | date, owner and the buyer's agreement are all present | one or two of the three | none, or "let's talk soon" with no agreement |

Integrity (ground rule 8): a false deadline, invented scarcity or made-up reference scores 0 on the row where it occurs (usually CS-06, CS-09 or CS-12), with the quote.

## Demo rows (CS-D01 to CS-D08)

All 8 are scored. Maximum = 8 × 2 = 16.

| Row | Behaviour | 2 | 1 | 0 |
|---|---|---|---|---|
| CS-D01 | Opens with the result the buyer wants | names the result in the buyer's own words before the first scene | mentions a result in general terms | starts with a feature tour |
| CS-D02 | Each scene answers a pain the buyer stated earlier | every scene linked to a quoted buyer pain (quote both) | every scene linked, but one link is the seller's guess | any scene with no stated pain behind it |
| CS-D03 | Pain confirmed before the scene | for every scene | for some scenes | never |
| CS-D04 | Open check-in after the scene | open check-in comparing with how the buyer works today after every scene | open check-in after some scenes | none, or closed ("does that make sense?") |
| CS-D05 | Buyer reaction explored | each notable reaction followed up | one follow-up on a reaction | reactions ignored |
| CS-D06 | Proof for outcome claims | each outcome claim backed by proof from the user's material, or flagged [PROOF NEEDED] | proof for some claims | claims with no proof and no flag |
| CS-D07 | The buyer gets the floor at the end | asks what mattered most to the buyer | "any questions?" only | no closing question |
| CS-D08 | Dated next step | date, owner and buyer agreement quoted | one or two of the three | none or vague |

## Pass rule (certification and ramp gates only)

Heuristic of this plugin, editable. A run passes when both hold:
1. No 0 on any row the user marks critical (default critical rows: discovery CS-03, CS-05, CS-12; demo CS-D02, CS-D08).
2. Points ≥ 70% of the available maximum, compared before rounding up to whole points.

Arithmetic, printed with every verdict:
- Discovery: 0.70 × 22 = 15.4, so 16 points or more.
- Demo: 0.70 × 16 = 11.2, so 12 points or more.
- With n/a rows the maximum shrinks: for example 10 scored discovery rows give 0.70 × 20 = 14.0, so 14 points.

Coaching never prints pass or fail; it prints points over the maximum of the rows that were scored.

## Worked example (coaching a real call)

The buyer says "We lose half a day to it" (06:10); the seller only asks "Who handles that on your side?" (06:30) and shows the product at 07:40. The call ends "Great, let's talk next week" (14:20), "Sounds good" (14:30).

Scored rows: CS-01 = 2, CS-02 = 2, CS-03 = 0 (quote 06:10, no sizing question followed), CS-04 = 0 (same moment), CS-05 = 1, CS-09 = 0, CS-10 = 1 (one follow-up at 06:30, no size, before the product at 07:40), CS-12 = 1 (agreement, but no date and no owner). Points 2 + 2 + 0 + 0 + 1 + 0 + 1 + 1 = 7 of a maximum of 16 over the 8 scored rows. Not observed: CS-06, CS-07, CS-08. In certification the same transcript would be 7 of 22, a fail (7 < 16, and CS-03 is 0).
