# Pinterest Trends

When should I publish each topic in my region from these Pinterest Trends values?
For content owners planning seasonal production. Supply pasted values, an export you already have, or a description of a screenshot, plus your region and production lead time. Analyzing supplied data needs no Pinterest account, API key, additional software or paid data service. To collect new values yourself, use Pinterest Trends in a browser; some views require a business account.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable servers.

Ordinary analysis uses task text, attachments, images and local exports you explicitly supply, plus bundled references. The skills instruct the assistant to inspect supplied images, read the bundled source register, and show calculations from supplied values; they do not prescribe code execution, software installation, API calls, file writes, message delivery or account changes. Any local reading, calculation or output file you explicitly request uses your assistant's existing tools, not a bundled program.

This package is not strictly offline: only an explicit documentation-refresh request permits the assistant's existing web tool to fetch the following four official documents, their sites' robots.txt, and redirects serving those documents:

- https://help.pinterest.com/en/business/article/pinterest-trends
- https://help.pinterest.com/en/business/article/schedule-pins
- https://create.pinterest.com/en-in/blog/leverage-seasonal-trends-moments/
- https://business.pinterest.com/en-au/pdf/2026-marketing-moments-guide/

Refresh requests disclose the requested URLs and ordinary connection metadata to help.pinterest.com, create.pinterest.com, business.pinterest.com, any document-serving redirect host (which may be Pinterest's content delivery host), and the assistant's tool provider. Supplied trend data is not uploaded. No web search, login, dashboard scraping, account connection or publishing is directed. If refresh is unavailable, the skills use dated bundled facts and state decision-relevant uncertainty.

The skills can guide you to collect chart values in your own Pinterest browser session and, only when asked, describe how you schedule a Pin yourself. Those user-led actions access Pinterest and may publish content through your account; the assistant does not perform them. Movable event dates must be separately verified or left unknown; the skills specify no additional retrieval destination for that check.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain your conversation, attachments and tool activity under its own terms.

## What you get

- **pinterest-curve-table:** a dated table that keeps search, save and shopping data separate, with missing values and worldwide audience scope marked.
- **pinterest-seasonal-calendar:** publication windows and production deadlines tied to each supplied curve, with formulas and late-start options.

Ask for the calendar directly when your data is already usable. Monthly or approximate inputs produce windows at that precision. Historical curves describe past interest; predicted points remain labelled. Index values do not establish absolute demand or sales.

Example request: “Region: France. Search values for picnic ideas by week: 2026-04-06 10, 2026-04-13 25, 2026-04-20 50, 2026-04-27 100. Production takes 14 calendar days. Publish at the rise. Give me production and publication dates.”

## Getting the values

In your own browser, open Pinterest Trends through your business account's Analyze performance menu. Select the region and Search trends, then the keyword and Date range. Copy visible dates and values, or describe the chart and its labels. Pinterest documents comparison of up to four terms at once; collect more topics in separate groups and retain each group's date range. This package does not require or promise a download button. You can use an export you already possess. A screenshot description is treated as your supplied evidence, not as an image the assistant has seen.

Include the trend view, metric, region label, dates, sampling interval, any filters, and which points are predictions. Add production time and any desired publishing advance, in calendar days or weeks. Business days need your working calendar. Do not paste credentials or customer details.

## Data and network

Analysis uses only supplied content and bundled references. No URLs are fetched during ordinary analysis. If you explicitly request a documentation refresh, the assistant may fetch the four exact official URLs listed in [references/pinterest-knowledge.md](references/pinterest-knowledge.md) and each site's robots.txt, following only redirects serving those documents. No search, account access, dashboard scraping, connector, telemetry or source-data upload is part of this package. If a document cannot be fetched, use the dated bundled facts and state the uncertainty when it changes the answer.

The output is a plan. Native scheduling steps can be described when requested; the assistant does not create, schedule or publish Pins. A seasonal calendar may extend beyond Pinterest's native scheduling horizon.

[Privacy](PRIVACY.md) · [License](LICENSE)
