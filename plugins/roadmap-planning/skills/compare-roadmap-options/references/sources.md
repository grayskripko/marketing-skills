# Official sources — checked 2026-10-11

All four URLs were opened as readable web pages on 2026-10-11 and independently checked by HTTP GET. This is the verification date, not a claim of a new publication. Runtime use remains offline; these references ship with the skills.

| Official source | Publication/update date shown | Deciding knowledge and boundary |
|---|---|---|
| Google OR-Tools, [The Knapsack Problem](https://developers.google.com/optimization/pack/knapsack) | Last updated 2024-08-28 UTC | Maximize supplied total value subject to capacity. Integer data requirement. Does not establish activation values or benefit additivity. |
| Google OR-Tools, [CP-SAT Solver](https://developers.google.com/optimization/cp/cp_solver) | Last updated 2024-08-28 UTC | Integer constraints; OPTIMAL versus FEASIBLE; INFEASIBLE, UNKNOWN and MODEL_INVALID boundaries. A time-limited unknown result does not prove infeasibility. |
| Google OR-Tools, [The Job Shop Problem](https://developers.google.com/optimization/scheduling/job_shop) | Last updated 2024-08-28 UTC | Start times, processing durations, precedence, exclusive-resource non-overlap and makespan. Human team calendars and release gates must be separately supplied. |
| Intercom, [RICE: Simple prioritization for product managers](https://www.intercom.com/blog/rice-simple-prioritization-for-product-managers) | Publication date not relied on; checked 2026-10-11 | Item scoring with reach, impact, confidence and effort; dependency and table-stakes exceptions. Does not validate a portfolio sum or calibrate confidence as outcome probability. |

## Adaptation and derivation

The [decision model](decision-model.md) adapts knapsack selection to prerequisite closure, mandatory work, mutual exclusions and separate team budgets. Its benefit-validation rules are an authored roadmap adaptation. Its upper-effort box guarantee is explicitly derived from nonnegative additive capacity inequalities. Calendar slots, pooled resource demand, approval timing and fallback residual capacity are explicit roadmap extensions to job-shop constraints. They are not external product policies or invented security requirements. Security and partner approval are enforced only as supplied by the user.

No company-specific policy, staffing calendar, historical productivity, probability distribution or measured activation effect is supplied. Conditional alternatives remain necessary where those facts decide the answer. Other answer-format and input-handling conventions are authored guidance. Source definitions do not prove this package outperforms another agent.
