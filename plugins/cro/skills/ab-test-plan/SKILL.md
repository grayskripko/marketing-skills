---
name: ab-test-plan
description: "Plans a website A/B or A/B/n test before it is built: visitors per arm, weeks at the user's traffic, power at the lift they care about, and the lift a fixed time limit can detect. Covers uneven splits, ship-if-not-worse tests, revenue per visitor and conversion windows that delay the readout. Use when the user asks how many visitors or how long a test needs, or whether a change can be A/B tested at their traffic. Not for ad, channel or software tests."
---

# A/B test plan

Answer the user's actual question first, in one or two sentences with their own numbers, then the working.

- Size from the users who actually reach the changed element, counted as new distinct users per week; say so if only sitewide traffic is given.
- Use the user's alpha, power and worthwhile lift. Give visitors per arm and calendar time. Name the method in one line (two-sided two-proportion z-test unless stated); show the full derivation only if asked.
- When the user has a time limit, say what that limit buys: the smallest lift it can detect, the power it gives at their worthwhile lift, and how much weekly traffic would be needed to meet the deadline. Count conversion and guardrail maturity windows inside the deadline.
- "Detectable" means an 80% (or stated) chance of a significant result if that lift is real; it is not a forecast of the change's effect.
- The run-or-don't call is a recommendation with its trade-off ("eight weeks resolves lifts of about 16% or more; smaller real effects will usually come back inconclusive"), not a fixed rule.
- Mention guardrails, stopping rules or allocation checks only as far as the user's setup needs them. Do not add thresholds the user did not set.
- Do not plan fake urgency, invented stock or fake reviews; offer the honest version in one line.
