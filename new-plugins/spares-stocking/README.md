# Spares Stocking

Find spare parts that are short, below reorder point or set with the wrong min/max, and check a critical spare parts list against what is actually in stock. For storeroom and MRO planners and reliability engineers at plants, utilities and equipment service operations. You paste the rows you need (stock on hand, reservations, open purchase orders, usage history, lead times, min/max settings, the critical spares list) into the request; no account or connector is needed. Criticality and service targets come from you.

| Skill | What you get |
|---|---|
| spares-shortage-check | The parts that are short for a dated work order or below reorder point, with the stock position worked out per part, counting only usable stock and firm receipts |
| min-max-review | Current versus indicated min/max or reorder point per part, with the lead-time demand, the coverage each level gives against your target, and the demand assumption used for slow movers |
| critical-spares-check | A register of critical spares that are not stocked, under-stocked, on a stale OEM revision or held under two item numbers, and which slow movers are insurance spares rather than excess |

Try: "Which of these spares are below min? Stock and POs below.", "Will we have enough 6205 bearings for next week's work orders?", "What reorder point does this slow-moving coupling need at 95%?", "Check our critical spares list against this stock list."

## What it adds

The work is in matching the records. Each skill joins stock, reservations, purchase orders, usage and policy rows by part number and storeroom, never links look-alike part numbers on its own, converts units only with a factor you give, and reports duplicates, stale revisions and parts missing from one record. It counts quality-inspection, blocked and awaiting-repair stock separately from usable stock, and treats purchase requisitions and past-due PO lines differently from firm receipts.

It knows how common systems trigger a reorder, because the same reorder point means different things in each: SAP reorder point planning (stock plus firm receipts below the reorder point, safety stock already inside it, reservations netted only with MRP types V1/V2), IBM Maximo (available balance plus on-order at or below the reorder point, ordered up to reorder point + 1 and rounded to the EOQ) and Oracle Fusion min-max (strictly below min, order bounds and lot rounding that can go down). For slow-moving and intermittent demand it uses a Poisson coverage check instead of the normal safety-stock formula, and it treats zero usage during stockouts, and on critical insurance spares, as no evidence of zero need. Dated sources are in [references](references/official-sources.md).

## Limits

It works only from the rows you paste. It does not raise purchase orders, change master data, decide interchangeability or dispose of stock, and it does not set criticality or service targets.

## Network and data

This is a skills-only package: Markdown instructions, a reference file, JSON metadata, a license and an SVG icon. It contains no scripts, servers, connectors or hooks and makes no network requests. The publisher receives no data. See [Privacy](PRIVACY.md).

[Sources](references/official-sources.md) · [Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Support](https://github.com/grayskripko/marketing-skills/discussions)
