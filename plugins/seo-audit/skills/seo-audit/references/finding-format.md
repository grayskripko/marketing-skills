# Finding format

Every skill in this plugin reports findings in the same shape, so results from a site audit, a page audit, an export review and a code review can be merged and handed to the fix plan without rewriting.

## Fields

| Field | What goes in it |
|---|---|
| ID | Short prefix plus number: `IDX-1` (indexing), `CRW-2` (crawl and architecture), `REN-1` (rendering), `ONP-3` (on-page), `CNT-1` (content), `SD-1` (structured data), `PERF-1` (performance), `INTL-1` (international), `DATA-1` (export pattern), `CODE-1` (source code). |
| Area | One of the areas above, in words. |
| Where | A URL, a URL pattern (`/blog/tag/*`), an export row, or `path/to/file.ext:line`. |
| Issue | One sentence describing what is wrong. No advice in this field. |
| Evidence | What was actually seen: the tag or header value, the column values, the code line, or the count of affected URLs with up to 3 examples. |
| Evidence level | Observed, From user data, or Needs verification (see below). |
| Impact | High, Medium or Low, set by the prioritization rules, not by feel. |
| Effort | S (under a day), M (a few days), L (a sprint or more). A rough guess; say so if the team size is unknown. |
| Fix | The concrete change: where, what, and who usually does it (developer, content, SEO). |
| How to verify | The check that proves the fix worked, and when to run it. |
| Might be intentional | Yes or No. Yes only for URL types where the pattern is usually deliberate: internal search, filter and sort parameters, cart, account and checkout pages, staging hosts, pages the owner means to exclude. Then the finding asks the owner to confirm instead of calling it an error. Always No for a noindex, robots.txt block or canonical pointing away on a page the user asked to rank or that is tied to the business goal, and for staging or development directives that reach production. |

## Evidence levels

- **Observed**: seen directly in a fetched page, in HTML or source code the user pasted, or in a file the assistant read. Quote the exact value.
- **From user data**: read from an export or table the user provided. Name the file or report and the columns used.
- **Needs verification**: cannot be confirmed from here. Always name the tool that would confirm it, for example URL Inspection in Search Console (rendered HTML, indexing status, Google-selected canonical), the Rich Results Test, field data from the Chrome UX Report or PageSpeed Insights, a crawler that renders JavaScript, or server logs.

Anything the model assumed rather than saw (the site's business model, which pages matter most, traffic levels) goes into an **Assumptions** list in the report. It is never written as a finding.

## Example row

| ID | Area | Where | Issue | Evidence | Level | Impact | Effort | Fix | Verify | Intentional? |
|---|---|---|---|---|---|---|---|---|---|---|
| IDX-1 | Indexing | `/pricing` | Page carries a noindex directive | `<meta name="robots" content="noindex,follow">` in the initial HTML | Observed | High | S | Remove the directive from the pricing template (developer) | URL Inspection shows "indexing allowed"; page appears in the Page indexing report as indexed within a few weeks | No |

## Rules

- One issue per finding. If the same issue affects many URLs, it is one finding with a count and examples, not many findings.
- A count of excluded or non-indexed URLs is not a finding by itself. It becomes one only when important pages are among them.
- If a check could not be run (no access, cap reached, tool missing), list it under "Not checked" with the way to check it. Do not guess a result.
