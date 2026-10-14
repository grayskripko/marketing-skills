# TierII Inventories

Work out EPCRA Tier II chemical inventory quantities from your own records: the maximum amount on any one day, the average daily amount, days on site, range codes and whether each chemical reaches its threshold. For EHS and environmental coordinators at plants, warehouses and depots, and for consultants who prepare Tier II reports for several sites. You paste stock counts, receipts, usage, SDS extracts and last year's Tier II lines into the conversation; no account or connector is needed.

| Skill | What you get |
|---|---|
| tier2-quantity-register | One row per chemical or mixture: maximum on any one day with its date and formula, threshold, range codes, average daily amount and days on site, with gaps and near-threshold results called out |
| tier2-sds-composition | The components that count for each product, which are extremely hazardous substances, component weights, and mismatched CAS numbers or stale SDS revisions |
| tier2-prior-year-check | A line-by-line comparison with last year's report: dropped and new chemicals, range-code and location changes, basis switches, and which lines can be marked identical |

Try: "Are we over 500 lb of sulfuric acid with the forklift batteries?", "Turn these monthly counts and receipts into Tier II max and average amounts", "Which ingredients in these SDSs count?", "What changed since last year's Tier II?"

## What it knows

The value is in the reconciliation: matching products, CAS numbers (with check-digit validation) and SDS revisions across counts, receipts, SDSs and last year's report, and finding the day of maximum rather than reading a year-end count or annual purchases. The skills carry the federal rules that most often change a result: the any-one-day threshold across the whole facility; 10,000 lb for hazardous chemicals and the lower of 500 lb and the TPQ for extremely hazardous substances, added across every mixture; the 1% and 0.1% carcinogen cut-offs; the mixture-or-component option and its consistency with section 311; retail-station fuel thresholds; why the 0.2 and 0.3 TPQ reduction factors do not apply to Tier II; sulfuric acid in lead-acid batteries; TPQs for common plant chemicals including the 52% qualifier on hydrogen peroxide; range codes; and the change to OSHA hazard categories that starts with the report due 1 March 2028. Each rule has a dated source in [references](references/official-sources.md): 40 CFR parts 355 and 370, EPA's 2026 Tier II rule and instructions, the EPA List of Lists and EPA's lead-acid battery memorandum.

State programs can add chemicals, lower thresholds or require exact amounts; the skills apply those when you paste them. Which facilities and exemptions apply stays with you.

## Network and data

This is a skills-only package: Markdown instructions, a reference file, JSON metadata, a license and an SVG icon. It contains no scripts, servers, connectors or hooks and makes no network requests. It works only on text you provide for the task, pasted or attached. The publisher receives no data. See [Privacy](PRIVACY.md).

[Sources](references/official-sources.md) · [Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Support](https://github.com/grayskripko/marketing-skills/discussions)
