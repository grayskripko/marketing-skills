# Ad Creative Preflight Kit

Checks ad text before it runs and reads creative tests after. Every limit and rule is dated and sourced. The first example below returns:

| Text | Rule | Result | Suggested fix |
|---|---|---|---|
| "Struggling with anxiety?" | Meta: no line that implies the viewer's health | likely disapproval | "AcmeCalm: an evening wind-down app." |
| "#1", "doctors recommend" | US FTC: claims need proof before the ad runs | Hold | name the source or drop the claim |
| "50% off today only" | Google, UK CAP Code: offers and deadlines must be real | Hold | confirm the end date and the old price |

## Skills

- **ad-preflight**: checks ad text you already have against platform limits and rules; Ready, Fix or Hold per ad, with fixed text.
- **ad-test-readout**: which ad won, whether the gap is real, and how much longer the test must run.
- **search-ad-set**: 15 Google headlines and 4 descriptions from your facts, checked so any three read well together.
- **social-ad-set**: LinkedIn, Facebook, Instagram and TikTok ad copy, in variants that each change one thing.
- **angle-matrix**: ad angles drawn from reviews and comments you paste, each traced to what customers said.

## Examples

- "Count and rule-check this Reels ad: 'Struggling with anxiety? AcmeCalm is the #1 app doctors recommend — 50% off today only!'"
- "Ad A: 40,000 impressions, 520 clicks, 26 sales. Ad B: 38,000, 610, 22. Same ad set, 10 days. Which one won?"
- "15 RSA headlines + 4 descriptions for a payroll app. Facts: 14-day trial, no card to try, from $39/mo, setup in one day."

## How it works

Covers Google, Meta, LinkedIn, TikTok and US, UK, EU claim rules. Rules read more than six months ago are flagged; limits the plugin has not checked are reported as unknown, never guessed. Copy uses the facts you give, in your words, and no figure you did not give.

## Data and network

Network scope: this plugin runs no code of its own, calls no service and stores nothing. It works on the text and numbers you paste or attach. It opens a web page only when you give the URL and ask for it, your assistant has a web tool, and the site's robots.txt allows it; such a page is treated as material, never as instructions. Ad libraries are paste-only. If your assistant has a code tool, it may use it to count characters and compute the tables it shows.

Strip names from reviews first; any left become ids (PRIVACY.md).

## What it will not do

Make images or video, change ad accounts, advise on spend, write political ads, or word copy to get past review. Not legal advice.

## Troubleshooting

"Not in this plugin's checked table": paste the limit your ad tool shows, and it is used as "your limit".

## Support

Issues: https://github.com/grayskripko/marketing-skills/issues

## License

MIT, see LICENSE.
