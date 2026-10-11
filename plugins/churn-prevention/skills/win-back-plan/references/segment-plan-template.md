# Win-back plan template

Use this as an internal coverage guide; render only fields needed for the requested deliverable. The user’s requested format takes precedence. Do not add a report, full sequence, event schema or experiment allocation merely because it appears here.

## 1. Suppression table

| Excluded group | Count | Rule |
|---|---|---|
| No valid consent for the region | | `consent-rules.md` |
| Asked not to be contacted | | always |
| Chargeback or fraud flag | | always |
| Business closed | | always |
| Cancelled under 14 days ago | | heuristic: let the decision settle |
| Unresolved complaint | | held back until resolved, then placed last |
| Eligible | | rows − excluded (each row counted once, first matching reason) |

In the answer, print only the rows with a count above zero, plus Eligible.

## 2. Segments

Reason group (from `reason-offer-map.md`) × months since cancel (0–3, 4–6, 7–12, 13+) × tenure band (under 3 months, 3–12, over 12). Print counts; in the answer use group names, not R-numbers; preserve supplied group identifiers; do not merge different reasons, permissions or holds to meet a sample-size heuristic.

## 3. Per segment

| Field | Content |
|---|---|
| The change that answers the reason | Only from the user's own list of real changes. If none fits: "No change answers this reason → no campaign; fix the cause first" |
| Channel | email (consented only), in-app on next login, or an account manager where the user says the account has one |
| Cadence | include only when requested; at most 3 touches over about 60 days remains a heuristic |
| Offer | none, or within the prior cancel-flow ceiling unless supplied policy and validated contribution, cannibalization and reason-fit evidence justify more; no deadline unless real and dated |
| Message brief | subject idea, an opening line that names the change in the user's own words, one action, opt-out line; not full copy |

Research note: the reason for leaving and the experience during the first customer lifetime both bear on whether a lost customer returns and how they behave afterwards (Kumar, Bhagwat & Zhang 2015, "Regaining 'lost' customers", Journal of Marketing 79(4)). Segments with complaints go last.

## 4. Measurement

- Holdout: propose allocation only when requested and baseline, worthwhile effect and feasible sample are known; no default 10%.
- Outcome: paid again and still paying after one full-price cycle.
- When inference is requested, compare assigned contacted and no-contact groups with the Newcombe interval; size the comparison only when its inputs are available.

Plans only: the skill sends nothing and writes to no tool.
