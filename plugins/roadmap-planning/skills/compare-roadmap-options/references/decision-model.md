# Portfolio, calendar and uncertainty procedure

Apply only the sections needed for the requested claim: section 1 for package selection, section 2 for deadline or release feasibility, and section 3 plus the applicable feasibility model for all-ranges commitments. For named alternatives, compare those alternatives without requiring an exhaustive search; retain the coverage qualification below. Source facts are in [sources.md](sources.md). The equations and roadmap translations below are explicit adaptations and mathematical derivations, not policies prescribed by Google or Intercom. No solver is bundled or required; enumerate small cases or use the host's available calculation tools.

## 1. Select a dependency-closed portfolio

For indivisible items, default to one binary selection variable x_i per item. Establish from supplied scope whether work is indivisible, staged or divisible. Represent supplied scope variants or stages with their own incremental effort/value, shared prerequisites and exclusion/precedence rules. For divisible allocations, use a model matching the supplied allocation rules rather than forcing binary selection; keep unsupported allocation or multi-window claims unresolved. Never invent reduced-scope estimates. For unfinished task i, supplied remaining effort e_it belongs to team t and budget C_t for the same window. Keep prerequisite effort in its own row when separable. Completed prerequisites are satisfied with zero remaining effort, not additional available capacity.

Constraints:
- Each team: sum_i(e_it x_i) <= C_t. A shared foundation has one x_i, so its effort appears once per team.
- Mandatory item m: x_m = 1.
- Unfinished prerequisite p of i: x_i <= x_p. Take transitive closure. Unresolved cycles block a claim of feasibility; supplied indivisible bundles can be represented explicitly.
- Mutually exclusive alternatives a,b: x_a + x_b <= 1. For a larger exclusion group: sum x_i <= 1.

Separate the feasibility evidence (remaining estimates, dependencies, exclusions and budgets) from the objective evidence (incremental outcome estimates and their combination rule). A knapsack objective maximizes supplied value under capacity; it does not validate the values.

Use max V(S) only after the user agrees what V means. If incremental benefits truly add, V(S)=sum_i(v_i x_i). For activation, v must describe additional activations over the same baseline, population and period, accounting for substitution and interactions. A prerequisite's enabling benefit must not be counted again in its dependents. Customer overlap alone does not prove benefit duplication; different changes for the same customers may interact positively or negatively. Ask for package estimates, incremental evidence or bounds when these interactions decide the choice.

RICE numerators R_i I_i c_i are an optional agreed proxy, not calibrated expected activations. Comparable ordinal impact scales and confidence discounts do not establish additive outcomes. Never default to that sum as the deciding objective. If duplicate benefit is unknown, retain item scores and show conditional alternatives or a frontier using supplied bounds. With no benefit bounds, report the assumption that would select each option and withhold an unconditional activation winner. A frontier retains packages not dominated on the agreed outcome and separate resource dimensions; unknown outcomes remain unresolved rather than silently treated as zero.

Procedure: list the candidate universe and allowed choices; enumerate closed sets for a small universe; reject constraint violations; evaluate feasible sets with the agreed V; retain ties and explain displaced approved scope. If only the named packages are checked, say “best among these options under this objective.” Global optimum requires exhaustive coverage or an optimization certificate for the declared model. A heuristic result is a candidate, not proof.

If the host uses CP-SAT, constraints require integer coefficients. Scale rational estimates exactly and state units; rounding can change feasibility. Report actual status: OPTIMAL proves optimality for the modeled objective; FEASIBLE does not; INFEASIBLE proves that model has no solution; UNKNOWN proves neither; MODEL_INVALID is a modeling failure. No solver status establishes real-world benefit validity.

### Worked portfolio

Fictional remaining efforts (engineering, design): mandatory M=(1,0), foundation P=(2,0), checkout C=(3,2), search S=(2,1), onboarding O=(1,2). S and O require P. Budgets=(6,3); C and S are exclusive. Agreed incremental activation estimates: C=90, S=60, O=50; M and P have no separately counted activation benefit.

Closed feasible sets containing M are: {M}, {M,P}, {M,C}, {M,P,C}, {M,P,S}, {M,P,O}, {M,P,S,O}. {M,C,O} needs P and totals (7,4), so fails. {M,P,S,O} totals (6,3). Checkout alone with M totals (4,2).

If S and O's duplicate activation benefit d is supplied only as [0,50], V(search+onboarding)=110-d versus checkout=90. Search+onboarding wins for d<20, ties at 20, loses for d>20. Neither package dominates over the whole bound; an unconditional activation winner is unsupported. Lead with these conditional choices when asked which to pick. If recommending the stronger worst-case outcome, label worst-case protection as the proposed decision rule; spare capacity is not an additional activation benefit without supplied evidence. This example's d bound is fictional input, not a rule for converting customer overlap into duplicate benefit.

## 2. Prove calendar feasibility separately

Job-shop scheduling uses durations, precedence and resource exclusivity. To adapt it, obtain elapsed durations, eligible resources and available calendars, task release times, deadline, gate timing and whether each gate blocks start, testing or release. Effort person-days cannot become elapsed days without a supplied staffing/productivity assumption. Human teams are not automatically single machines: use exclusive specialist slots only where supplied; pooled teams need time-varying capacity/resource demand, not a blanket no-overlap assumption.

For each selected task use start s_i, duration d_i and end f_i=s_i+d_i. Enforce f_p<=s_i for precedence; s_i>=r_i for release times; and f_i<=s_j OR f_j<=s_i for tasks sharing a supplied exclusive resource. Put task intervals inside available calendar slots; model interruptions/preemption only if allowed. For pooled resources, at every time tau sum active task demands <= available capacity(tau). Retain required maintenance reservations.

For a gate required only before release, release >= max(final task end, approval time). If approval blocks task start instead, s_i>=approval time. Add supplied post-approval work duration and dependencies; never silently assume a zero-duration gate. Require release<=deadline. Unknown approval time prevents an unconditional deadline guarantee. A feasible schedule is a witness; a precedence lower bound past the deadline proves failure even before resource contention. An earliest-finish calculation ignoring calendars is only a lower bound.

### Capacity passes, release fails

Fictional single engineering slot available [0,8), capacity eight person-days; engineering durations equal effort by supplied assumption. Maintenance M=1, P=2, search S=4, export E=3; S and E require P. Keep plan costs 7; replace S with E costs 6. Witness: M [0,1), P [1,3), E [3,6). Security approval is release-only at day 9; deadline day 8. Export fits effort and construction time, but release>=9>8. Search can finish on day 7 if it has no gate.

A fallback trigger must preserve a feasible residual plan. At trigger h, subtract all effort already spent, including abandoned work, and schedule remaining fallback work in actual slots after h. Example: after M and P at day 3, search needs four days and can run [3,7). If export consumes three further days before switching at day 6, search ends day 10 and total spending is 10>8. The fallback is then infeasible. Derive the latest switch from a backward calendar schedule, including supplied switching costs and reservations; deadline minus effort is valid only for the supplied continuous single-slot abstraction. If timing is missing, state the conditional trigger and unresolved cutoff rather than inventing a date. Shared work may proceed before approval only if it remains useful in the fallback and authorization permits it.

## 3. Test joint ranges and commitment scope

Identify whether “survives uncertainty” means item-score order, fixed-scope capacity, deadline, or objective superiority. Define the uncertainty set U before making an all-ranges claim. Separate diagnostic one-input checks from universal guarantees; intervals are not distributions or confidence intervals.

For fixed dependency-closed scope S, nonnegative additive remaining efforts e_it in supplied independent interval bounds [l_it,u_it], U is the Cartesian product of those bounds (all combinations allowed, not statistical independence). Since x_i>=0, sum e_it x_i <= sum u_it x_i for every e in U. Therefore S is effort-feasible throughout U iff sum u_it x_i <= C_t for each fixed team budget. If capacity itself has independent supplied bounds, use its lower bound. Count mandatory repair and prerequisites once. If all-upper effort exceeds capacity, the fixed commitment fails the all-ranges guarantee even if each individual check passes.

Correlated bounds: the box is a conservative outer set if all actual cases lie inside it; passing the box suffices, failing it may use an impossible combination and does not prove actual failure. Use supplied joint scenarios or constraints to maximize each team's effort over the actual U. Unknown correlations, changing scope, nonadditive effort or resource reassignment leave the requested exact guarantee unresolved. Enumerating a few scenarios proves only those scenarios unless they exhaust U.

For timing, check the calendar constraints too. A feasible fixed schedule at upper durations and latest bounded gate times can cover the box if resources/calendars and dependencies are fixed and shorter tasks may wait until reserved starts. Unknown/unbounded approval means no all-ranges deadline guarantee. Adaptive rescheduling needs an explicit policy and evidence that its decisions are available when required; a different schedule for each future outcome is not automatically an executable commitment.

For objective robustness require V(A,u)>=V(B,u) for every relevant feasible competitor B and u in U, using an agreed outcome model. For independent monotone value intervals and disjoint packages, lower V(A)>=upper V(B) is sufficient; shared uncertain terms should cancel in the difference before taking bounds. Unknown overlap/interactions prevents this test. A score crossover holds other inputs fixed and is not a package or deadline crossover.

### Individual checks pass, joint capacity fails

Fictional required repair R=[2,3], foundation P=[1,2], feature F=[3,4], one-team capacity 8. Base all-low total=6. Raising R alone gives 7, P alone 7, F alone 7; all fit. Joint upper total=3+2+4=9>8, so fixed scope is not robust over the box. F must satisfy F<=8-R-P; with repair and foundation at upper bounds, F<=3. A fallback {R,P,G} with G=[2,3] has upper total=8 if G requires P, but gate and calendar feasibility still need checking. Reach ranges cannot repair an effort deficit. No probabilities follow from these bounds.
