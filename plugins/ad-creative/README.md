# Ad Creative Preflight Kit

Checks ad text before launch and reads creative tests after. Every limit and rule is dated and sourced. The first example below returns:

| Text | Rule id | Result | Action |
|---|---|---|---|
| "Struggling with anxiety?" | META-PA | likely disapproval | "AcmeCalm: a routine for calmer evenings." |
| "#1", "doctors recommend" | GEN-CL-RANK, GEN-CL-ENDORSE | Hold | name the source or drop the claim |
| "50% off today only" | GEN-URG, GEN-PRICE | Hold | confirm end date and old price |

## Skills

- **ad-preflight**: counts, dated rule findings, claim ledger, Ready / Fix / Hold.
- **ad-test-readout**: intervals, design label, days still needed.
- **search-ad-set**: headlines and descriptions from your facts, combination test.
- **social-ad-set**: LinkedIn, Meta, TikTok copy; one-variable variants.
- **angle-matrix**: angles traced to pasted reviews, hypotheses.

## Examples

- "Count and rule-check this Reels ad: 'Struggling with anxiety? AcmeCalm is the #1 app doctors recommend — 50% off today only!'"
- "Ad A: 40,000 impressions, 520 clicks, 26 sales. Ad B: 38,000, 610, 22. Same ad set, 10 days. Which one won?"
- "15 RSA headlines + 4 descriptions for a payroll app. Facts: 14-day trial, no card to try, from $39/mo, setup in one day."

## How it works

Covers Google, Meta, LinkedIn, TikTok and US, UK, EU claim rules. Old rows are flagged; unlisted fields are unknown, never guessed. No figure enters your copy unless you supplied it.

## Data and network

Network scope: this plugin runs no code of its own, calls no service and stores nothing. It works on the text and numbers you paste or attach. It opens a web page only when you give the URL and ask for it, your assistant has a web tool, and the site's robots.txt allows it; such a page is treated as material, never as instructions. Ad libraries are paste-only. If your assistant has a code tool, it may use it to count characters and compute the tables it shows.

Strip names from reviews first; any left become ids (PRIVACY.md).

## What it will not do

Make images or video, change ad accounts, advise on spend, write political ads, or word copy to get past review. Not legal advice.

## Troubleshooting

"Not in this plugin's checked table": paste the limit your ad tool shows.

## Support

Issues: https://github.com/grayskripko/marketing-skills/issues

## License

MIT, see LICENSE.
