# Complaint types

Default: each complaint-coded item gets 1 primary fix type. Use an issue-level type for each explicit distinct complaint when a supplied item needs materially different fixes; retain one record id and state item-level or issue-level classification used.

| Type | Test | Usual owner |
|---|---|---|
| bug | something does not work as designed | engineering |
| confusion | it works, but the person could not find or understand it | design, onboarding, docs |
| missing capability | the product cannot do the job the person needs | product |
| expectation mismatch | the product works as designed, but not as promised or implied | marketing, sales, pricing page |
| price | the cost is the complaint, with or without value named | pricing, packaging |
| service | slow, missing or unhelpful support or account handling | support, customer success |

Default: when the same issue fits 2 types, choose the type its fix depends on and note the other. Use separate issue/type pairs when the text describes distinct failures requiring different fixes; state that issue-level coding was used.
