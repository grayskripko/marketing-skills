# Acquisition Reporting

Reconcile LinkedIn paid-campaign lead and conversion totals using exported settings and the pasted Attribution Model table; produce a client explanation.
For agencies and freelancers preparing client reports. For reconciliation, supply report rows, conversion settings and a pasted Attribution Model table. For client wording, supply an existing reconciliation and relevant settings. Works from pasted reports and supplied files; no LinkedIn login or API key is required. Load the package’s skills in a supported assistant.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account.

These skills work only from task text, attachments, and local files that you explicitly supply. They do not instruct the assistant to run code, install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. URLs in this package identify sources or support pages; they are not connection endpoints or retrieval instructions. A supplied URL is treated as text: paste the relevant content instead.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

Report preparation: you obtain exports and copy the Attribution Model table yourself in LinkedIn Campaign Manager. The comparison guidance may ask you to clear reporting filters and select a mature date range there; the skills do not access that account or perform those UI actions. Arithmetic and word-count checks are instructions to verify supplied values, not instructions to execute code.

| Skill | Input | Result |
| --- | --- | --- |
| reconcile-linkedin-totals | Campaign exports, settings, pasted Attribution Model table | Comparable totals, calculated gaps, supported explanations and unresolved differences |
| explain-linkedin-attribution | An existing reconciliation, settings and client draft or requested format | Client-ready explanation with correct metric labels and supported claims |

Paste exact headings, totals, date range, timezone, selected filters, reporting level and extraction time. Include the conversion action’s name separately from its category (Lead is a category), associated ad sets, attribution model, click/view windows and dated setting changes when available. Stable campaign IDs help distinguish reused names; lead contact details are unnecessary.

In Campaign Manager, open Advertise, choose the relevant Campaigns, Ad sets or Ads tab, then Columns → Attribution model. Paste the visible headings, rows and total with the selected filters. This table is not exportable. Ordinary performance reports and conversion settings can be supplied as files or text. Fractional credits and blank cells retain their meaning.

Embedded references contain official LinkedIn Help and Microsoft Learn guidance verified on 2026-10-11; using the skills does not refresh those sources.

Sources: [official reporting knowledge](skills/reconcile-linkedin-totals/references/linkedin-reporting.md).

MIT. See [LICENSE](LICENSE). Support: https://github.com/grayskripko/marketing-skills/issues
