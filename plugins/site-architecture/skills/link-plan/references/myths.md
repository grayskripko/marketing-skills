# Claims this plugin does not use as rules

Answer in one or two sentences from this table when the user raises one.

| Claim | What the sources say | Source |
|---|---|---|
| Every page must be reachable within 3 clicks | No published study supports the rule; a test of it found people did not give up more often when a task took more than three clicks. Report depth, and judge it by how clear each step is. | NN-3click |
| A menu should have at most 7 items | The same article names this as a second myth with no data behind it. Judge categories by how distinct and recognisable they are, not by a count. | NN-3click, NN-FD |
| A flat hierarchy always beats a deep one | Both shapes fail at the extremes: flat works when categories are distinct and recognisable; deep ones need shortcuts to key pages. | NN-FD |
| Keywords in the URL path lift rankings | Google says words in the path have hardly any effect beyond showing in breadcrumbs. Readable paths are for people. | G-start |
| `rel=next` and `rel=prev` are needed for paginated series | Google no longer uses them. Each page of a series needs its own URL, a normal crawlable link and its own canonical. | G-page |
| Page 1 should be the canonical for every page of a series | Google says not to do this; each page in the series is its own canonical. | G-page |
| Blocking a URL in robots.txt and adding noindex makes sure it drops out | A crawler that may not fetch the page never sees the noindex, so the URL can stay indexed. Use one or the other on purpose. | G-noindex |
| Redirect every removed page to the homepage | Many old URLs pointed at one unrelated page can be treated as soft 404s and confuse visitors. Removed pages with no replacement should answer 404 or 410; Google currently treats the two the same. | G-move, G-404 |
| There is an ideal number of links per page, or per 1,000 words | Google gives no number. It asks for links that help the reader and says that if a page looks like it has too many, it probably does. | G-links |
| Internal nofollow channels link value to money pages | Not a documented mechanism. This plugin never plans internal nofollow to steer value (rule 8). | rule 8 |
| Moving content to a subdomain or a new domain escapes a quality problem | This plugin treats a move as a structural change, not a fix for content quality; improve the content itself. | convention of this plugin |
| More near-duplicate pages bring more traffic | This plugin gives each page one intent and plans no new URL for a wording variant of an existing page; a new URL needs its own decision point, use case or data. | convention of this plugin |
| Folders are a ranking signal of hierarchy | Google's stated reason for grouping pages in directories is that it can learn how often each section changes. Folder = parent section is a convention of this plugin, chosen for consistency. | G-start |
