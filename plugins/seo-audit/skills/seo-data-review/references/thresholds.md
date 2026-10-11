# Fixed procedures and thresholds

The numbers below are written down so that results can be checked: numeric screening calculations are shown row by row before the flag lists. For a few named URLs with simple zero-impression or status findings, show the values, period and affected count beside their evidence and actions instead of a duplicate screening table. Numbers taken from a primary source name it. Everything else is labeled **heuristic**: a reasonable default chosen for reproducibility, which the user may override. In the answer, label the defaults once as screening heuristics, show relevant cutoffs with the requested calculations and respect user overrides. Distinguish eligibility under this screen from business priority; retain useful near misses.

Search Console "position" is the average topmost position of the site's result across impressions. Treat it as an average, not a rank.

## 1. Striking-distance queries (heuristic)

- Rows: queries with average position from 8.0 to 20.0 inclusive.
- Select and disclose the minimum volume using period length, relevant segment, evidence sufficiency and business value. The reproducible starting default is 100 impressions; the legacy large-property screen uses 1,000 above 1,000,000 property impressions, but use that only with a stated rationale. A one-impression boundary does not establish a meaningful difference in opportunity.
- Sort the screening table by impressions, descending. Choose recommended work by the business goal, retaining useful near misses; a screen pass is not a business-priority verdict. Consider commercially relevant queries present only in query-by-page data separately, without treating page-level averages as a property-level query position.
- Output: query, position, impressions, clicks, CTR, and the landing page if the export has it.
- Meaning: pages that already rank near the first page, where on-page work and internal links tend to pay off first.

## 2. CTR outliers by position band (heuristic)

- Bands by average position, so that every value falls in exactly one band: 1.0 to 3.0; above 3.0 to 7.0; above 7.0 to 10.0; above 10.0 to 20.0. Rows above 20.0 are out of scope.
- Only rows with at least 200 impressions.
- Compute the median CTR of the user's own rows in each band.
- Flag rows whose CTR is below half of their band's median.
- Build peers from comparable search context before using position bands. With fewer than 3 qualifying peers, show a descriptive comparison and its limitations rather than a categorical outlier verdict; a singleton cannot establish an outlier. The existing bands, 200-impression minimum and half-median cutoff remain disclosed fallback screens, not proof of comparable exposure.
- Branded queries (containing the site or brand name) usually have much higher CTR; if the user names the brand, compute bands without branded rows and say so.
- Do not use a generic industry CTR curve.
- A low CTR is a reason to inspect the query's results page, not proof that the title is bad. Mention particular search features only when evidence or the user's question makes them relevant; do not attribute these rows to unobserved features.

## 3. Cannibalization (heuristic)

- Needs a table with query and page together.
- Only queries with at least 50 impressions.
- For a disclosed starting screen, flag shared-query exposure when two or more URLs each hold at least 20% of the query's clicks; below 10 query clicks, use impressions. Retain the 50-impression eligibility default unless context warrants another evidence minimum. This is not proof of harmful cannibalization: assess intent, temporal switching, canonical relationships and performance loss before recommending consolidation.
- Output: query, each URL with its share, positions.
- Might be intentional: Yes when the URLs serve different intents (for example a product page and a support article), so ask before merging.

## 4. Losing pages or queries (heuristic)

- Needs two periods of equal length. Prefer the same period a year earlier to avoid seasonality; otherwise the immediately preceding period, and say seasonality is not controlled.
- Use 50 prior clicks and a 30% decline as disclosed starting screens, then consider absolute loss, relative loss and business value. Preserve relevant low-volume or smaller-relative-loss cases. Direct questions about named pages require their observed changes without an eligibility gate.
- Compare clicks, not impressions, if either period touches a reporting anomaly that affects impressions but not clicks (`data-anomalies.md`).

## 5. Traffic-drop diagnosis (heuristic mapping)

Read clicks and impressions together for the affected page or query group:

| Pattern | Hypotheses to test, not established causes | Next check |
|---|---|---|
| Clicks down, impressions flat | Query, country, device or position mix changed; alternatively search-result features, ads or competing snippets changed click propensity | Look at the results page for top queries; compare CTR by band |
| Clicks and impressions both down, position down | Rankings lost for a set of queries | Which query groups fell; what changed on those pages; competing pages |
| Clicks and impressions both near zero | The page dropped out: 404, noindex, canonical change, robots.txt block, redirect | Check status, robots meta, canonical and robots.txt first; then manual actions, cannibalization, seasonality; only then content quality |
| Impressions down, clicks flat, position up | Reporting change, demand change or loss of lower-position impressions; aggregate position does not track a fixed query set | Check the data anomalies list for those dates |

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
- Use zero impressions as an investigation screen, choosing the window by publication/change age, seasonal demand and expected exposure. For established pages, 90 days remains a disclosed fallback; use the export's full period if shorter and state coverage. Verify indexing and demand before proposing improve, merge or remove.
- Suggested action per URL: improve, merge into a stronger page, or remove and redirect. Do not recommend mass deletion without the owner's review.

## 8. Days since last crawl (heuristic)

- Needs a last-crawl date per URL (URL Inspection results exported through the API or a tool, or server logs).
- Screen important URLs against their update urgency and expected recrawl cadence; 30 days is a disclosed fallback for established pages, not a universal fault. Logs establish the last observed hit within their coverage, not necessarily the last crawl. Falling crawl frequency can show up before a traffic drop, so treat it as an early warning, not a verdict (heuristic).

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
- Lab results (Lighthouse) are for debugging only. Interpret supplied LCP as loading, CLS as layout stability and TBT as blocking work; TBT is not INP. Label any diagnostic severity as belonging to that lab run, not a field CWV verdict or a cause of non-indexing. If field data is insufficient, say CWV is unknown and name PageSpeed Insights field data, CrUX or Search Console Core Web Vitals as the next evidence, including field INP. Put a necessary rendering check beside the affected page using URL Inspection’s crawled/live rendered view. For an indexing fix, assess later indexed status and impressions after recrawl, and the stated business outcome, without promising a date.
