---
name: ab-test-verdict
description: "Reads a finished or running website A/B or A/B/n test from visitors and conversions per variant (or mean, SD and n) and answers whether to ship, hold or keep testing. Covers uneven traffic splits, peeking and early stopping, tool 'chance to beat control' figures, guardrails and several variants or metrics. Use when the user asks whether B won, whether to ship or stop a test, whether a result is noise, why the split looks uneven, or what a tool's probability means. Aggregate counts only; not for ad-level results or channel tests."
---

# A/B test verdict

Open with the decision the user asked for (ship, hold, keep running) and the one or two numbers that decide it. Then the working, short.

- Compute rates, the absolute and relative lift and a p-value or interval. Compare the observed lift directly with the user's worthwhile lift when they gave one.
- Traffic split off plan: test it against the planned shares and report how unlikely it is. A severe mismatch means hold and investigate the cause (assignment, redirects, bots, logging) before trusting the effect; say what would allow a reanalysis and when a rerun would be needed. Do not invent a cut-off that declares the test invalid.
- Stopped early or checked repeatedly: report the nominal result, explain why repeated looks inflate false positives, and where possible bound it (for example a Bonferroni-style adjustment for the number of looks). Separate "there is evidence of some improvement" from "the planned sample and duration were met", and say what the team can honestly claim.
- A predeclared guardrail breach blocks rollout; still state how the primary result compares with the worthwhile lift.
- A tool's "chance to beat control" depends on its model and prior; it is not the probability that shipping is right.
- Write a team or release-note sentence when asked. Reuse a confirmation plan the user already has instead of adding new sizing.

Dated facts: use a fact only when it changes the answer; never list them.
- Size of the peeking problem: in Statsig's 50,000 real-data A/A tests (28 days), a z-test checked repeatedly gave 17.3% false positives against 5.0% for one look at the planned end; a sequential method built for repeated looks gave 1.1%. <!-- https://www.statsig.com/blog/sequential-testing-on-statsig ; checked 2026-10-15 -->
- An overall "experiment significant" flag across many correlated metrics can mislead: on 2,300 Microsoft A/A scorecards, Fisher-style aggregation flagged 22.0% at p < 0.05, Benjamini-Hochberg 2.1%, Bonferroni 1.7%. Ask how the tool combines metrics. <!-- https://www.microsoft.com/en-us/research/articles/treatment-effect-assessment-at-scale-accounting-for-correlated-metrics-and-metric-relevance-in-modern-experimentation/ ; checked 2026-10-15 -->
