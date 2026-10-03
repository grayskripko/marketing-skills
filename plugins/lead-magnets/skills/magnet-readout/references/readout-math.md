# Readout maths

## Rate with interval

Rate = k/n. Interval: Wilson score interval at 95% (z = 1.96), described in the NIST/SEMATECH e-Handbook of Statistical Methods, section 7.2.4.1 (itl.nist.gov, read 2026-10-03).

centre = (p + z²/2n) / (1 + z²/n); half-width = z × √(p(1−p)/n + z²/4n²) / (1 + z²/n), with p = k/n.

## Difference between two rates

Newcombe's hybrid score interval, built from the two Wilson intervals (Newcombe RG, "Interval estimation for the difference between independent proportions: comparison of eleven methods", Statistics in Medicine 1998; 17(8): 873 to 890). With d = p1 − p2 and Wilson limits (l1, u1) and (l2, u2):

lower = d − √((p1 − l1)² + (u2 − p2)²); upper = d + √((u1 − p1)² + (p2 − l2)²).

Always labelled "observed difference, not a significance test". Wording:
- the interval excludes 0 and both numerators are 20 or more → "different in this data";
- the interval excludes 0 but a numerator is below 20 → "different in this data, few events: provisional";
- the interval includes 0 → "not distinguishable yet".

Do not compare by checking whether two separate intervals overlap. Do not compute sample sizes or test lengths. Checking repeatedly and stopping at the first good-looking result inflates false alarms (Evan Miller, "How Not To Run an A/B Test", 2010-04-18); say so when the user reports reading results daily.

## Labels

- "few events (k < 20)": the numerator is below 20. Heuristic of this plugin, used everywhere.
- "too early": fewer than 30 sign-ups, or fewer than 5 sales conversations, for that magnet. No verdict other than "too early" is given.

## Maturity window

Downstream rates (conversations, opportunities, deals per sign-up) use only sign-ups older than the window. Window = the user's figure; otherwise the median days from sign-up to conversation in the data; otherwise "lag not checked" and every verdict is provisional. Print how many sign-ups were left out.

## Projected figures

Projected per 1,000 visits = sign-up rate × mature downstream rate × 1,000. Print the formula, the inputs, and the raw figure beside it (downstream count ÷ visits × 1,000), so a reader can see why they differ.

## Rounding

Compare with thresholds before rounding. Percentages and percentage points to one decimal, ratios to one decimal, money in whole units, halves away from zero. A bound that excludes 0 but rounds to 0.0 prints as "<0.1" (or ">−0.1"), never as 0.0 or with a second decimal.

## Worked example 1 (two views; the flagship)

Checklist: 2,400 visits, 312 sign-ups, 9 sales calls. Calculator: 900 visits, 81 sign-ups, 14 calls. No dates, no source.

| Magnet | Sign-ups / visits | Calls / sign-ups | Calls / visits |
|---|---|---|---|
| Checklist | 312/2,400 = 13.0% (11.7–14.4) | 9/312 = 2.9% (1.5–5.4), few events | 9/2,400 = 0.4% (0.2–0.7), few events |
| Calculator | 81/900 = 9.0% (7.3–11.0) | 14/81 = 17.3% (10.6–26.9), few events | 14/900 = 1.6% (0.9–2.6), few events |
| Observed difference | checklist − calculator: +4.0 pp (1.6 to 6.2), different in this data | calculator − checklist: +14.4 pp (7.2 to 24.2), different in this data, few events: provisional | calculator − checklist: +1.2 pp (0.5 to 2.2), different in this data, few events: provisional |

Calls per visit, calculator ÷ checklist = (14/900) ÷ (9/2,400) = 4.1 (unrounded 4.148). Reading: the checklist grows the list faster (list-growth view); the calculator brings more calls per visit (pipeline view). Lag, traffic source and counting method not checked. Verdicts, provisional, applying the rows of `diagnosis-tree.md` in order: calculator keep (row 3, calls per visit highest; row 2 does not fire); checklist fix bridge (row 4: sign-ups per visit the higher one, calls per sign-up clearly lower). Re-check when each call count reaches 20.

## Worked example 2 (maturity window, projection)

Guide A: 1,840 visits, 312 sign-ups; of 260 sign-ups older than 60 days, 9 became opportunities. Guide B: 610 visits, 128 sign-ups; of 110 mature sign-ups, 2 became opportunities. No traffic source given.

| Measure | Guide A | Guide B | Observed difference |
|---|---|---|---|
| Sign-ups per visit | 312/1,840 = 17.0% (15.3–18.7) | 128/610 = 21.0% (17.9–24.4) | B − A +4.0 pp (0.5 to 7.8), different in this data |
| Opportunities per mature sign-up | 9/260 = 3.5% (1.8–6.4), few events | 2/110 = 1.8% (0.5–6.4), few events | A − B +1.6 pp (−3.2 to 4.9), not distinguishable yet |
| Projected opportunities per 1,000 visits | 0.1696 × 0.0346 × 1,000 = 5.9 (raw 9 ÷ 1,840 × 1,000 = 4.9) | 0.2098 × 0.0182 × 1,000 = 3.8 (raw 2 ÷ 610 × 1,000 = 3.3) | — |

Reading: B's sign-up rate is higher by a small margin (the lower bound is 0.5 pp), and with no source column the gap may come from who arrived rather than from the page. On quality the two cannot be told apart yet. Verdicts: Guide A keep, provisional (traffic source not checked); Guide B too early (2 downstream events, fewer than 5).
