# Myths and unverified claims

The skills in this plugin do not report the items below as problems. If the user raises one, answer in one or two sentences in plain words and name the source (Google Search Central, SEO Starter Guide and related documentation). Do not lecture.

The Google pages behind these rows were re-read on 2026-10-08. If more than six months have passed, say the dated rows may be out of date and point to the source.

## Documented by Google as not mattering (or not in the way people think)

| Claim | What Google's documentation says, in short |
|---|---|
| Add a meta keywords tag | Google Search does not use it. |
| Pages need a minimum (or maximum) word count | There is no word-count target for ranking. Length should follow what the topic and reader need. |
| Headings must be in strict order, or there must be exactly one H1 | Heading order and count help accessibility and readability; Google does not rank on heading order. |
| Put the keyword in the domain name or URL | Keywords in the domain have little effect beyond appearing in breadcrumbs and the displayed URL. |
| The top-level domain changes rankings | Only country-code domains matter, and only for targeting that country. |
| Subdomains are worse than subfolders (or the reverse) | Choose by what suits the business and the site's maintenance; both work for search. |
| Duplicate content causes a penalty | Duplicates cause Google to pick one URL to show, which can waste crawling and split signals. It is not a manual penalty unless the copying is deceptive or spammy. |
| E-E-A-T is a ranking factor to optimize | It describes what Google's systems try to reward; it is not a single signal or score. |
| Special files or markup are needed to appear in AI Overviews or AI Mode | Google says its AI features need nothing beyond the normal requirements for Search: no special files and no special markup. |
| robots.txt removes a page from Google | robots.txt blocks crawling. A blocked URL can still be indexed without its content if other pages link to it. To keep a page out of the index, allow crawling and use noindex, or remove the page. |
| Sitemap `priority` and `changefreq` steer crawling | Google ignores both. It uses `lastmod` only when it is consistently accurate. |
| A sitemap makes pages rank, or forces indexing | A sitemap helps discovery. It does not guarantee crawling, indexing or ranking. |
| Add FAQPage markup to get FAQ rich results | FAQ rich results stopped appearing in Google Search from 2026-05-07 (Search Console Help, Data anomalies). |
| A lower CTR at a stable position means the title is bad | AI Overviews and AI Mode appearances are counted inside the Web search type, so CTR can move for reasons unrelated to the title. Check the query's search results before rewriting. |
| `rel=next` / `rel=prev` are needed for pagination | Google no longer uses them as an indexing signal. Each paginated page needs its own crawlable link and, usually, a self-referencing canonical. |

## Lab scores versus field data

A Lighthouse or PageSpeed lab score is a test run on one simulated device. Core Web Vitals assessment in Search uses field data from real Chrome users (the Chrome UX Report), judged at the 75th percentile. Never report a low lab score as a ranking problem by itself. Report field data when the user has it; otherwise mark performance as Needs verification and name the field-data source.

## Unverified practitioner hypotheses

Some widely shared SEO theories are built on readings of Google internal documents that leaked in 2024, on patents, or on single-site experiments. Examples: specific weights for click signals, site-level quality tiers, a numeric site authority score used in ranking, fixed "content freshness" windows.

Rules for these:
- Never use them as the reason for a finding. A finding must stand on evidence from the page, the data or the code.
- If the user asks, say plainly that the theory is not confirmed by Google, and describe what can actually be checked instead.

## Claims about AI search that are often overstated

- "Structured data gets you cited by AI assistants." Google says no special markup is needed for its AI features, and published industry experiments have not shown a reliable citation gain from adding JSON-LD (treat that as a heuristic, not a rule). Recommend structured data for the rich results it supports and for clear entity information, not as an AI-visibility lever.
- "llms.txt is required." Google says its AI features need no new machine-readable files or AI text files. Do not report the absence of llms.txt as an issue.
