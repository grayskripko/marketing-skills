---
name: ad-test-readout
description: "Reads ad or creative test results, or plans a creative test: which ad or concept won, whether a CTR or conversion gap is real or noise, whether the comparison was randomised, and how many more impressions or days a clear answer needs. Use when the user asks which ad or creative won, whether a gap between ads is real, or how many impressions or days a creative test needs. Not for website or landing-page A/B tests, attribution, or spend decisions."
---

# Ad test readout

First write the answer exactly as you would without this skill: the same shape, length and judgement. Then check the draft against the list below and change only what fails. Do not add sections about these checks or about metrics the user did not ask for.

## Checks

1. The first line answers the user's main question, and every question they asked is answered in their order.
2. The winner is judged on the user's primary metric (otherwise conversions per impression), never on clicks or whichever metric has the bigger gap.
3. Impossible counts (clicks above impressions, click-based conversions above clicks) mean no winner: the rows are named and the correction is stated.
4. Ads delivered by the platform inside one ad set are called not randomised: a gap is a lead to confirm, not proof. Google asset rows count an impression for every asset in the ad, so they are never summed into totals, and asset CTR, CPC, CPA and ROAS are directional only; full asset statistics start on 5 June 2025. <!-- support.google.com/google-ads/answer/9564897, checked 2026-10-15 -->
5. A Google Demand Gen experiment shows conversion results only after 50 conversions per arm, and its 70% default confidence is labelled directional; only 95% is labelled conclusive, so a winner shown at 70% or 80% is called directional. <!-- support.google.com/google-ads/answer/13719071, checked 2026-10-15 -->
6. Several variants against one control are adjusted for multiple comparisons (Holm on p-values, or Bonferroni-adjusted intervals if the user wants no p-values); skipping p-values is not a reason to call results exploratory.
7. A completed fixed-horizon test with an interval that includes zero is called inconclusive at that horizon, with no advice to keep running it; give the interval as relative lift too, and the smallest lift the test could have detected. If the user named a smallest useful lift, say whether the interval clears it.
8. Every number is recomputed and consistent across the answer (rates, intervals, lift, sample size, days). Compute with a code tool when one is available.
9. Budget and other user constraints are kept; no spend advice.
10. When the user asks to see the calculation, write each formula with their numbers in it, then the result.
11. Unequal arms are not a problem unless the planned split differs; if the plan is unknown, ask it. In a test planned as an even split, arm sizes further apart than chance allows are flagged as a possible sample-ratio mismatch (chi-square on the assigned counts) before any winner is named.
12. A "|" inside a markdown table cell is escaped.
