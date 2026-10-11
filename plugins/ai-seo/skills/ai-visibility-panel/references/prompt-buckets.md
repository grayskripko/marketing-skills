# Prompt buckets

Use these buckets as an adjustable commercial buyer-discovery starter. Select relevant intents from the user's objective and seed queries; omit irrelevant buckets. Counts apply to prompt IDs, with phrasing rows counted separately; adapt allocation and panel size to coverage and workload.

| Bucket | What it tests | Typical count | Branded? | Example (fictional brand Acme Invoicing) |
|---|---|---|---|---|
| discovery | Whether the brand appears when a buyer asks for options in the category | 5-7 | no | "What invoicing software works for a 20-person agency?" |
| use-case | Whether the brand appears for a specific need or segment | 4-6 | no | "Which invoicing tool handles multi-currency for EU freelancers?" |
| comparison | How the brand is described next to a named competitor | 3-5 | no, names a competitor only | "Northwind Pay vs other invoicing apps for approvals" |
| alternatives | Whether the brand appears when a buyer leaves a competitor | 2-4 | no | "Alternatives to Globex Billing for small teams" |
| problem | Whether the brand's content is used when a buyer describes a problem, not a product | 4-6 | no | "How do I set up invoice approval with two signers?" |
| brand-direct | Whether answers about the brand itself are accurate | 3-5 | yes | "What does Acme Invoicing cost and who is it for?" |

## Writing rules

- Two phrasings for each prompt in the discovery, use-case, comparison and alternatives buckets: one short and typed, one longer and conversational. Give them the same `prompt_id` and phrasing `a` or `b`.
- Use the buyer's words and the user's market language. Seed queries from the user's own search or sales data are preferable to invented ones.
- Unbranded prompts never contain the brand name and never lead toward it.
- Brand-direct prompts check accuracy (price, audience, features, location). Score them separately.
- Keep the panel fixed between periods. If a prompt must change, retire its ID and add a new one, so old and new results are not mixed.
