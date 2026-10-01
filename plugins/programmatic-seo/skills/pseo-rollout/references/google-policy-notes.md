# Google policy notes

Checked on Google Search Central on 2026-10-01. Recheck the pages before relying on these lines; Google updates them.

| Page (last updated) | What it says, in short |
|---|---|
| Spam policies for Google web search (2026-08-28) | Scaled content abuse: many pages generated mainly to manipulate rankings rather than help users; its examples include generating many pages without adding value and automated rewording of other content. Doorway abuse: pages made to rank for similar queries that lead people to less useful intermediate pages; its examples include pages aimed at specific cities or regions that send users to one page, and substantially similar pages that look more like search results than a browseable hierarchy. Cloaking is listed as a separate policy. |
| Google Search's guidance on using generative AI content (2025-12-10) | Automation and AI are not banned as such; generating many pages without adding value for users may violate the scaled content abuse policy. |
| How to specify a canonical with rel="canonical" and other methods (2026-07-10) | When pages are duplicates, Google picks one version to show. Redirects and rel="canonical" are strong signals for your preferred version; listing a URL in a sitemap is a weak signal. |
| Block search indexing with noindex (2025-12-10) | noindex works as a meta tag or an HTTP header, and only if the page is not blocked by robots.txt and is otherwise crawlable. |
| Build and submit a sitemap (2026-07-08) | One sitemap file is limited to 50,000 URLs or 50 MB uncompressed; larger sets are split into several files, optionally listed in a sitemap index. |
