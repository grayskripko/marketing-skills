# Prompt buckets

Default full panel: 25 prompt IDs: discovery 5, use-case 4, comparison 4, alternatives 3, problem 5, brand-direct 4 (21 unbranded, 4 branded). The 20-30 full-panel range and bucket ranges below are coverage guides, not simultaneous quotas. If the stated sustainable budget cannot cover the full panel, use a 10-unbranded-ID starter: discovery 2, use-case 2, comparison 2, alternatives 1, problem 3, each with one phrasing and 3 repetitions per selected engine. Brand-direct accuracy questions may be added separately and never enter unbranded denominators. Use fewer real IDs when supplied buyer evidence supports fewer; do not invent questions to meet a quota. Omit unsupported competitor buckets and redistribute only to distinct evidenced intents. Add evidenced uncovered intents up to 30 IDs when the budget permits; for a larger explicitly requested inventory, group questions into bounded panels and state their coverage separately. State IDs, bucket allocation, phrasing count, repetitions, selected engines and calculated workload; keep IDs and wording fixed between periods. These counts are workload conventions, not researched optima.

| Bucket | What it tests | Typical count | Branded? | Example (fictional brand Acme Invoicing) |
|---|---|---|---|---|
| discovery | Whether the brand appears when a buyer asks for options in the category | 5-7 | no | "What invoicing software works for a 20-person agency?" |
| use-case | Whether the brand appears for a specific need or segment | 4-6 | no | "Which invoicing tool handles multi-currency for EU freelancers?" |
| comparison | How the brand is described next to a named competitor | 3-5 | no, names a competitor only | "Northwind Pay vs other invoicing apps for approvals" |
| alternatives | Whether the brand appears when a buyer leaves a competitor | 2-4 | no | "Alternatives to Globex Billing for small teams" |
| problem | Whether the brand's content is used when a buyer describes a problem, not a product | 4-6 | no | "How do I set up invoice approval with two signers?" |
| brand-direct | Whether answers about the brand itself are accurate | 3-5 | yes | "What does Acme Invoicing cost and who is it for?" |

## Writing rules

- Default: two phrasings for discovery, use-case, comparison and alternatives, one for problem and brand-direct. Use one for the constrained starter or where the supplied seed has no distinct wording variant; use two for other buckets when logged wording variants give materially different answers. State the allocation used, share the ID, and keep both periods balanced.
- Use the buyer's words and the user's market language. Seed queries from the user's own search or sales data are preferable to invented ones.
- Unbranded prompts never contain the brand name and never lead toward it.
- Brand-direct prompts check accuracy (price, audience, features, location). Score them separately.
- Keep the panel fixed between periods. If a prompt must change, retire its ID and add a new one, so old and new results are not mixed.
