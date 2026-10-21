---
name: ab-test-sample-size
description: "Any question about how long or how big a website A/B test needs to be, even a quick one-liner: how many visitors do I need, can I A/B test with 2,000 visitors a month, how long should my test run. Plans a website A/B test before it is built from the user's conversion rate and traffic: visitors per arm, weeks at that traffic, power at the lift they care about, and the smallest lift a fixed time limit can detect, counting conversion windows that delay the readout. Use when the user asks how many visitors or how long a test needs, or whether a change can be A/B tested at their traffic. Not for reading a finished test (ab-test-verdict), or for ad, channel or software tests."
---

# A/B test sample size

First name, in one line, the user fact that most constrains the answer and how it changes the call; build the answer on it. Then answer the question asked, in one or two sentences with their numbers, then the working, short.

- Before sizing, check the inputs agree (traffic vs share reaching the element, baseline vs counts, deadline vs maturity window). If they conflict, say so first; it changes the plan.
- Stay inside the scope and output shape the user set; no side analysis.
- Size from the users who actually reach the changed element, counted as new distinct users per week; say so if only sitewide traffic is given.
- Use the user's alpha, power and worthwhile lift. Give visitors per arm and calendar time, computed exactly: power as a number (41%, not "around half"), sample sizes and weeks as numbers, not ranges. Name the method in one line (two-sided two-proportion z-test unless stated); show the full derivation only if asked.
- When the user has a time limit, say what that limit buys: the smallest lift it can detect, the power it gives at their worthwhile lift, and how much weekly traffic would be needed to meet the deadline. Count conversion and guardrail maturity windows inside the deadline.
- "Detectable" means an 80% (or stated) chance of a significant result if that lift is real; it is not a forecast of the change's effect. Do not predict ceilings or effects the inputs do not give.
- The run-or-don't call is a recommendation with its trade-off ("eight weeks resolves lifts of about 16% or more; smaller real effects will usually come back inconclusive"), not a fixed rule.
- Mention guardrails, stopping rules or allocation checks only as far as the user's setup needs them. Do not add thresholds the user did not set.
- Do not plan fake urgency, invented stock or fake reviews; offer the honest version in one line.
