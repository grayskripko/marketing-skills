# Blog Content Strategy, Content Calendar & Content Audit

Plan what content to write next, what to fix or retire, and how to fit topics, writer briefs and lead magnets into your team's available hours. Covers content audits, pruning, topic maps, briefs, lead magnets and a plan that fits real capacity. It plans; it does not write the content or build campaigns.

## What it does

- **content-audit:** keep, update, merge, redirect, retire or leave alone for each existing page, with the reason and the numbers behind it.
- **content-planning-topic-map:** topics by buyer stage and search intent, each tied to evidence only your company has; generic topics are set aside.
- **content-calendar:** a week-by-week plan that fits your team's hours, with a planning score for each idea and a not-now list.
- **content-brief:** a brief a writer can work from, built on your evidence, with a success metric.
- **lead-magnet-plan:** one lead magnet for a topic cluster or a slot in your plan, with the reason to ask or not ask for an email.

## Examples

- Keep, update, merge or cut: /blog/ap-tips-2021 (40 visits), /blog/ap-automation-guide (2,100), /blog/ap-tips-2023 (35).
- Demo goal, 1 writer 6h/wk. Topics: ROI guide (own data), customer story (own data), AP glossary (no own data). What fits this quarter?
- Topic map for Northwind Ledger: AP automation for 50-500 staff firms, goal demo requests, we have 40 customer interviews.

## How it works

Example decision: /blog/ap-tips-2023 (35 visits) answers the same question as /blog/ap-tips-2021 (40 visits), so it merges into the stronger page; a small job. Example plan line: month-end close checklist, 4 hours, planning score 11 of 12, first in the plan. A publish date alone never decides a page's fate, and scores are planning judgements, not traffic forecasts.

## Data and network

The plugin makes at most two kinds of fetch, both through the assistant's own web tool.

1. **Your own site, when you give it (content-audit only).** When you give a sitemap URL, content-audit reads at most 3 sitemap files as lists of URLs without visiting those URLs, and fetches at most 10 public pages that you name on the same site, after checking that site's robots.txt and skipping disallowed paths. It never logs in, submits forms or follows links.
2. **The author's page at https://black-vector.com/content-strategy/myths, only after you say yes.** Some advice relies on dated Google guidance positions (for example, that a page's age alone is no reason to retire it). The bundled copy is dated 2026-10-08 and may be out of date, so an answer may end with a short sources line: the Google pages it relied on, their date, and an offer to check them against the plugin's changelog of these positions, `https://black-vector.com/content-strategy/myths`, a page kept by the plugin author on a domain he owns. It fetches that page only if you say yes or ask for it, quotes what changed, and you decide whether to revise anything. If you never say yes, nothing is fetched.

No skill runs web searches or calls any other service on its own. If the assistant has a code tool, it may use it to compute the tables and totals from what you pasted; the plugin ships no code and stores nothing. Remove names and emails of customers or interviewees before pasting notes; the skills refer to people as Customer A, Customer B.

What the author's page at https://black-vector.com/content-strategy/myths keeps: see the [privacy policy](PRIVACY.md).

## Troubleshooting

- A check was skipped: add the column named under Not checked.
- The plan looks small: it matches the hours you gave; change the hours or the reserved share.
- A fetch failed: paste the list instead.

## Related plugins

Where this plugin stops and another one of mine continues:

- [Lead Magnets](https://github.com/grayskripko/marketing-skills/blob/storm/plugins/lead-magnets/README.md): lead-magnet-plan only plans the asset; Lead Magnets drafts it with proof checks, checks the opt-in for consent rules and reads sign-up-to-deal results.
- [Site Architecture & Faceted Navigation](https://github.com/grayskripko/marketing-skills/blob/storm/plugins/site-architecture/README.md): Redirect and retire decisions from content-audit need a checked redirect map, and a topic cluster needs a hub and child-page link spec, both of which Site Architecture builds.
- [Customer Research Kit](https://github.com/grayskripko/marketing-skills/blob/wind/plugins/customer-research/README.md): content-planning-topic-map labels topics without a source of new information as commodity; interview synthesis and feedback analysis are how a team gets that first-hand information.

## Questions and feedback

If a skill works wrongly for your task, tell me in GitHub Discussions — I read every message: https://github.com/grayskripko/marketing-skills/discussions

Bug reports also work in GitHub Issues: https://github.com/grayskripko/marketing-skills/issues

Sergey Skripko. I build AI agents.

## License

MIT. See LICENSE.
