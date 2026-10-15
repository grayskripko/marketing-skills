---
name: ab-test-verdict
description: "Reads a finished or running website A/B or A/B/n test from visitors and conversions per variant (or mean, SD and n) and answers whether to ship, hold or keep testing. Covers uneven traffic splits, peeking and early stopping, tool 'chance to beat control' figures, guardrails and several variants or metrics. Use when the user asks whether B won, whether to ship or stop a test, whether a result is noise, why the split looks uneven, or what a tool's probability means. Aggregate counts only; not for ad-level results or channel tests."
---

# A/B test verdict

First name, in one line, the user fact that most constrains the answer and how it changes the call; build the answer on it. Then the decision asked for (ship, hold, keep running) in the user's terms, the reason in their numbers, and the one inconsistency if there is one. Nothing else: no citations, no re-sizing of their plan, no side analysis.

- First recompute from the raw counts and check the user's figures agree with each other: rates vs counts, the tool's p-value or "chance to beat" vs what the counts give, the stopping story vs the final p, the split vs the plan. If they disagree, that is the headline: name the figure that cannot be right and the data or tool problem it points to. Take what the user reports as observed (a stop date, a guardrail reading, a quoted message) as given unless the counts contradict it.
- Other facts the user gave (deadline, cost of a wrong call, segment): a clause each if they change the call. No speculative causes.
- Compute rates, the absolute and relative lift and an exact p-value and interval (give the number, not "below 0.05"). Compare the observed lift directly with the user's worthwhile lift when they gave one.
- Traffic split off plan: chi-square against the planned shares and report the exact p. A severe mismatch means hold and investigate the cause (assignment, redirects, bots, logging) before trusting the effect; say what would allow a reanalysis and when a rerun would be needed. Do not invent a cut-off that declares the test invalid.
- Stopped early or checked repeatedly: report the nominal result, explain why repeated looks inflate false positives, and where possible bound it (for example a Bonferroni-style adjustment for the number of looks). Separate "there is evidence of some improvement" from "the planned sample and duration were met", and say what the team can honestly claim.
- A predeclared guardrail breach blocks rollout; still state how the primary result compares with the worthwhile lift.
- A tool's "chance to beat control" depends on its model and prior; it is not the probability that shipping is right.
- Write a team or release-note sentence when asked.

