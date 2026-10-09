# Finding format

Every skill in this plugin reports findings in the same shape, so results from a site audit, a page audit, an export review and a code review can be merged and handed to the fix plan without rewriting.

## Fields

| Field | What goes in it |
|---|---|
| # | A number, 1, 2, 3, in impact order. |
| Area | In words: indexing, crawl and architecture, rendering, on-page, content, structured data, performance, international, export pattern, or source code. |
| Where | A URL, a URL pattern (`/blog/tag/*`), an export row, or `path/to/file.ext:line`. |
| Issue | One sentence describing what is wrong. No advice in this field. |
| Evidence | What was actually seen: the tag or header value, the column values, the code line, or the count of affected URLs with up to 3 examples. |
| Evidence level | Observed, From user data, or Needs verification (see below). |
| Impact | High, Medium or Low, set by the prioritization rules, not by feel. |
| Effort | Under a day, a few days, or a sprint or more (S, M, L in the prioritization rules). A rough guess; say so if the team size is unknown. |
| Fix | The concrete change: where, what, and who usually does it (developer, content, SEO). |
| How to verify | The check that shows the change is live, and the report to look at again later. Whether Google indexes the page or accepts its canonical is something to check on a date, never a promised result. |
| Might be intentional | Yes or No. Yes only for URL types where the pattern is usually deliberate: internal search, filter and sort parameters, cart, account and checkout pages, staging hosts, pages the owner means to exclude. Then the finding asks the owner to confirm instead of calling it an error. Always No for a noindex, robots.txt block or canonical pointing away on a page the user asked to rank or that is tied to the business goal, and for staging or development directives that reach production. |

## Evidence levels

- **Observed**: seen directly in a fetched page, in HTML or source code the user pasted, or in a file the assistant read. Quote the exact value.
- **From user data**: read from an export or table the user provided. Name the file or report and the columns used.
- **Needs verification**: cannot be confirmed from here. Always name the tool that would confirm it, for example URL Inspection in Search Console (rendered HTML, indexing status, Google-selected canonical), the Rich Results Test, field data from the Chrome UX Report or PageSpeed Insights, a crawler that renders JavaScript, or server logs.

Anything the model assumed rather than saw (the site's business model, which pages matter most, traffic levels) goes into an **Assumptions** list in the report. It is never written as a finding.

## Example row

| # | Area | Where | Issue | Evidence | Evidence level | Impact | Effort | Fix | How to verify | Might be intentional |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | Indexing | `/pricing` | Page carries a noindex directive | `<meta name="robots" content="noindex,follow">` in the initial HTML | Observed | High | Under a day | Remove the directive from the pricing template (developer) | Live test in URL Inspection shows "indexing allowed"; check the page's status in the Page indexing report again after 1–4 weeks | No |

## Rules

- One issue per finding. If the same issue affects many URLs, it is one finding with a count and examples, not many findings.
- A count of excluded or non-indexed URLs is not a finding by itself. It becomes one only when important pages are among them.
- If a check could not be run (no access, cap reached, tool missing), list it under "Not checked" with the way to check it. Do not guess a result.
- In the answer, leave out a column whose value is the same in every row and say it once above the table (for example "All seen in the HTML you pasted; none looks intentional"). Keep Fix and How to verify: they are the developer hand-off.
- With three findings or fewer, a numbered list (issue, evidence, fix, who) is usually clearer than a table.
- In sentences, name a finding by what it is ("the noindex tag on /pricing"), not by its number.
