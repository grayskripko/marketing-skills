# Fixed procedures and thresholds

The numbers below are written down so that results can be checked: the calculation is always shown, row by row, before the flag lists. Numbers taken from a primary source name it. Everything else is labeled **heuristic**: a reasonable default chosen for reproducibility, which the user may override. Always print the thresholds used.

Search Console "position" is the average topmost position of the site's result across impressions. Treat it as an average, not a rank.

## 1. Striking-distance queries (heuristic)

- Rows: queries with average position from 8.0 to 20.0 inclusive.
- Minimum volume: at least 100 impressions in the export period. If the property has more than 1,000,000 impressions in the period, raise the minimum to 1,000.
- Sort by impressions, descending.
- Output: query, position, impressions, clicks, CTR, and the landing page if the export has it.
- Meaning: pages that already rank near the first page, where on-page work and internal links tend to pay off first.

## 2. CTR outliers by position band (heuristic)

- Bands by average position, so that every value falls in exactly one band: 1.0 to 3.0; above 3.0 to 7.0; above 7.0 to 10.0; above 10.0 to 20.0. Rows above 20.0 are out of scope.
- Only rows with at least 200 impressions.
- Compute the median CTR of the user's own rows in each band.
- Flag rows whose CTR is below half of their band's median.
- If a band has fewer than 3 qualifying rows, still compute it, but say the baseline is thin. A band with one row cannot flag anything.
- Branded queries (containing the site or brand name) usually have much higher CTR; if the user names the brand, compute bands without branded rows and say so.
- Do not use a generic industry CTR curve.
- Caveat to print: AI Overviews and AI Mode results are counted inside the same Web search type, and rich results, ads and other features change clicks at a stable position. A low CTR is a reason to look at the results page for that query, not proof that the title is bad.

## 3. Cannibalization (heuristic)

- Needs a table with query and page together.
- Only queries with at least 50 impressions.
- Flag a query when two or more of the site's URLs each hold at least 20% of the query's clicks. If the query has fewer than 10 clicks in total, use impressions instead of clicks.
- Output: query, each URL with its share, positions.
- Might be intentional: Yes when the URLs serve different intents (for example a product page and a support article), so ask before merging.

## 4. Losing pages or queries (heuristic)

- Needs two periods of equal length. Prefer the same period a year earlier to avoid seasonality; otherwise the immediately preceding period, and say seasonality is not controlled.
- Flag rows where clicks in the previous period were at least 50 and fell by 30% or more.
- Compare clicks, not impressions, if either period touches a reporting anomaly.

## 5. Traffic-drop diagnosis (heuristic mapping)

Read clicks and impressions together for the affected page or query group:

| Pattern | Most likely cause | Next check |
|---|---|---|
| Clicks down, impressions flat | Something on the results page took the click: a feature, an AI answer, ads, a competitor snippet | Look at the results page for top queries; compare CTR by band |
| Clicks and impressions both down, position down | Rankings lost for a set of queries | Which query groups fell; what changed on those pages; competing pages |
| Clicks and impressions both near zero | The page dropped out: 404, noindex, canonical change, robots.txt block, redirect | Check status, robots meta, canonical and robots.txt first; then manual actions, cannibalization, seasonality; only then content quality |
| Impressions down, clicks flat, position up | Measurement or reporting change | Check the data anomalies list for those dates |

Always split by search type, country and device before calling a drop site-wide.

## 6. Page indexing statuses (Search Console Page indexing report)

- Group URLs by status and report counts.
- These statuses are usually fine when they apply to the right URLs: "Alternate page with proper canonical tag", "Excluded by 'noindex' tag" (on pages meant to be excluded), "Page with redirect", "Not found (404)" for removed pages, "Blocked by robots.txt" for private areas.
- Always a finding when important URLs are affected: "Server error (5xx)", "Soft 404", "Duplicate, Google chose different canonical than user", "Blocked by robots.txt" or "Excluded by 'noindex' tag" on pages meant to rank, "Indexed, though blocked by robots.txt".
- Triage for "Crawled – currently not indexed" and "Discovered – currently not indexed":
  1. First separate URLs that should stay out of the index: internal search results, filter and sort parameters, deep pagination, tag archives with little content, test pages, feeds. These are not problems; say so.
  2. For important URLs that remain, walk the likely causes: thin or near-duplicate content compared with pages already indexed; main content added by JavaScript; weak discovery (no internal links, deep in the site, only in the sitemap); a burst of new pages on a young site; a recent migration.
  3. For a single important page, a quick test: compare its main topic and phrasing with the pages that rank for its query. If it adds nothing new, the content is the likely cause. If it is comparable, look at internal links and click depth first.
- A count of excluded URLs is never a finding by itself.

## 7. Indexable pages with zero impressions (heuristic)

- A crawler export shows whether a URL is indexable, not whether Google indexed it. Whether Google indexed these URLs needs the Page indexing export or URL Inspection.

- Needs a crawler export (indexable URLs) and a Search Console pages export.
- Flag indexable URLs with 0 impressions over the last 90 days (use the export's full period if shorter, and state it).
- Suggested action per URL: improve, merge into a stronger page, or remove and redirect. Do not recommend mass deletion without the owner's review.

## 8. Days since last crawl (heuristic)

- Needs a last-crawl date per URL (URL Inspection results exported through the API or a tool, or server logs).
- Flag important URLs not crawled for more than 30 days. Falling crawl frequency often shows up before a traffic drop, so treat it as an early warning, not a verdict.

## 9. Crawler export patterns

| Pattern | Rule | Source or label |
|---|---|---|
| Redirect chains | 2 or more redirect hops before a 200 | heuristic; Google follows up to 10 hops (Google Search Central, HTTP status codes) |
| Internal links to redirects | Any internal link whose target answers 3xx | heuristic |
| Errors in the sitemap | Sitemap URLs answering 3xx, 4xx or 5xx | Google sitemap guidelines: list canonical URLs you want indexed |
| Non-indexable URLs in the sitemap | noindex, canonicalized elsewhere, or blocked | Google sitemap guidelines |
| Orphans | URLs in the sitemap with 0 internal inlinks | heuristic |
| Duplicate titles | Exact duplicates among indexable URLs, grouped by template | heuristic |
| Canonical to a bad target | Canonical pointing to a non-200 or noindexed URL | Google canonicalization documentation |
| Deep pages | Crawl depth above 3 for pages the user marks as important | heuristic |
| Heavy HTML | The heaviest 10% of HTML documents by size, listed for review; any HTML over 15 MB is truncated by Googlebot | 10% is heuristic; 15 MB is from Google's Googlebot documentation |
| Key page type missing from sitemap | No URLs of a template the user names as important (for example products) | heuristic |

## 10. Server log sample (only if provided)

- Verify search engine bots by user agent and, if the user can, by reverse DNS; user agents can be faked.
- Share of bot hits by status code and by page class (money pages, content, support, junk such as parameters and internal search).
- Flag: a large share of bot hits on junk URL classes; money pages with few or no bot hits in the period; many 3xx or 4xx hits from bots.
- Image bot rarely requesting images on pages the main bot crawls often: images may be injected by JavaScript.
- Dead ends and loops: sessions where the bot keeps requesting parameter variations of the same page.

## 11. Performance results

- Core Web Vitals "good" thresholds at the 75th percentile of field data (web.dev): Largest Contentful Paint at most 2.5 s, Interaction to Next Paint at most 200 ms, Cumulative Layout Shift at most 0.1.
- Use field data (Search Console Core Web Vitals report, CrUX, the field section of PageSpeed Insights) for verdicts.
- Lab results (Lighthouse) are for debugging only. Report lab issues as things to investigate, not as ranking problems.
