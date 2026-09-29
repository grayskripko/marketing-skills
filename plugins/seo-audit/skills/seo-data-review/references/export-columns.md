# Recognizing exports by their columns

Column names differ by tool version and interface language. Match on meaning, and ask the user if unsure. Tool names are mentioned only to help recognize files.

## Search Console, Performance (web interface export)

- Delivered as several tables: queries, pages, countries, devices, search appearance, dates, plus a filters table describing what was applied.
- Typical columns: the dimension (for example "Top queries" or "Top pages"), Clicks, Impressions, CTR, Position.
- The interface export does not combine query and page. For cannibalization, ask for a query-by-page table from the Search Console API, the bulk data export, or a report tool connected to Search Console.
- Check the filters table: a search type other than Web, a country filter or a date comparison changes how to read everything else.

## Search Console, Page indexing

- Columns usually include URL and Last crawled, grouped by status (for example "Crawled – currently not indexed", "Excluded by 'noindex' tag", "Page with redirect").
- The interface export for one status is limited to a sample of URLs (up to 1,000 rows); say that counts from the report summary are the totals.

## Search Console, URL Inspection results

- Obtained through the API or third-party tools. Useful columns: URL, coverage or indexing state, Google-selected canonical, user-declared canonical, last crawl time, robots.txt state, page fetch state.

## Bing Webmaster Tools and Yandex Webmaster

- Search performance tables with query or page, clicks, impressions, CTR and average position. Treat them like Search Console tables, but never mix engines in one calculation.

## Crawler exports

Desktop crawlers export an "internal" or "all pages" table. Look for columns meaning:
- address or URL;
- status code and status;
- indexability and the reason (noindex, canonicalized, blocked);
- title, meta description, main heading (often numbered: first title, second title);
- canonical link;
- crawl depth;
- inlinks or unique inlinks;
- word count, size in bytes, response time;
- redirect target or final URL, and number of redirect hops if exported.

Separate exports often exist for redirect chains, sitemap URLs versus crawled URLs, and hreflang. Ask for them if the question needs them.

## PageSpeed Insights and Lighthouse

- JSON or copied text. Field data appears as a separate block (for example "Discover what your real users are experiencing") with percentile values for LCP, INP and CLS. Lab data appears as metric values and a performance score.
- Use only field data for Core Web Vitals verdicts.

## Server logs

- Common log formats: IP, time, request line (method, path), status, bytes, referrer, user agent.
- Ask for a sample filtered to search engine user agents over at least 7 days (heuristic) if the full log is large.
- Remind the user to remove or mask personal data such as IP addresses of human visitors before sharing.
