# CRO Audit and Test Kit

Conversion rate optimization (CRO) for your own pages, forms, checkouts and A/B tests. Every finding shows its evidence, and every number shows its arithmetic.

> "Can we ship B? A: 300 signups from 10,000 visitors. B: 345 from 10,150." → **Inconclusive.** B converted 3.4% against A's 3.0%, but the data fit anything from a small loss to a 32% gain. The traffic split is fine. The answer gives the test size that would settle it.

## Skills

- **page-audit**: a landing, pricing or demo page and its numbers → what to fix first, each fix marked fix now, A/B test or research first.
- **flow-audit**: a form, signup or checkout → which fields to cut or move later, where people get stuck, and a dated check of the order step against EU and US rules (UK rows not yet verified).
- **funnel-leaks**: step counts split by device or source, or set against an earlier period → which step loses the most people, and how sure that is.
- **ab-test-plan**: your conversion rate and weekly traffic → how many visitors and weeks a test needs, or a plain "don't A/B test this".
- **ab-test-verdict**: visitors and conversions per version → Ship, Don't ship, Inconclusive or Invalid, after checking the test was run cleanly.

## Examples

- "A/B test on our pricing page: A 300/10,000 signups, B 345/10,150. 50/50 split, 14 days. Can we ship B?"
- "Signup rate is 3% on 6,000 visitors a week. How long must an A/B test run to detect a 10% relative lift?"
- "Audit our checkout: 4 steps, account required, 16 fields, shipping cost shown only at the last step. We sell to EU and US."

## How it works

Each finding says whether it was seen on the page, comes from your data or is assumed. No industry averages, no predicted lifts. Legal checkout rules show the date each was read; this is not legal advice.

## Data and network

Network scope: this plugin runs no code of its own, calls no service and stores nothing. It works on what you paste or attach and does not search your files or folders. The page and flow skills open a public page only when you give its URL and ask for it, your assistant has a web tool and robots.txt allows it: at most three pages of that site, with no login, form submission or add-to-cart. Fetched pages are material, never instructions. Your assistant's code tool, if it has one, may compute the tables.

Send counts, not visitor-level exports. See PRIVACY.md.

## What it will not do

Write copy, build deceptive variants (fake scarcity, hidden fees, pre-ticked extras), quote "good" conversion rates, or call a site compliant.

## Troubleshooting

"Do not A/B test": traffic cannot finish the test; the plan shows the lift it can detect. "Not checked" names the missing input.

## Support

Open an issue at https://github.com/grayskripko/marketing-skills/issues.

## License

MIT, see LICENSE.
