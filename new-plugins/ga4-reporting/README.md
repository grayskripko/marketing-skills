# GA4 Reporting

Reconcile GA4 acquisition and exploration exports into a monthly client report using supplied scopes, attribution settings and quality indicators.
For agencies and freelancers reporting to clients. Supply pasted tables or exported files plus the date range, field names, settings and quality indicators. No account connection, key, paid API or installation is needed to analyze supplied data.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON platform metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable servers. Build notes, reviews and test records are development documentation, not runtime instructions.

These skills analyze only task text, attachments and local exports that you explicitly supply, plus bundled reference text. They do not instruct web searches, URL or robots.txt fetches, API calls, account connections, message delivery, publishing or settings changes. Google Help URLs record source research; support URLs identify support pages. These are not retrieval instructions or connection endpoints. Paste relevant content rather than supplying a URL for retrieval. Re-export requests describe the fields and settings you must export yourself from GA4 and supply; the assistant does not access GA4 or perform the export.

Both skills permit “calculate locally if available.” Your assistant may use its existing local calculation, code or spreadsheet tools on supplied values; this is not a strict no-execution workflow. No calculation program or software installation is bundled. Tool execution and temporary files are managed by your assistant provider. Any report file you explicitly request is created by your assistant's existing file tools at your selected destination, not by a bundled program. Drafting a report does not send it.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider still processes and may retain your conversation, attachments and tool activity under its own terms. These boundaries concern additional plugin-directed activity, not the assistant provider's inference connection.

| Skill | Ask for | Result |
|---|---|---|
| reconcile-ga4-exports | Explain why acquisition and Explore numbers disagree | Comparison table, usable figures and specific re-export instructions |
| write-ga4-monthly-report | Turn exports or a reconciliation into a monthly client report | Client copy, comparable month changes and the quality notes that affect the figures |

## Inputs

Paste CSV or table text, or provide local CSV, spreadsheet or PDF exports that your assistant can read. Include full column headers and totals; say whether rows are complete or just the top rows. Add property time zone, currency, included streams, filters, comparisons or segments, reporting identity, selected key event and counting method. Include the reporting attribution model, relevant lookback windows and any changes between periods.

Copy the data-quality indicator text: percentage used, thresholding and grouped (other) rows. A CSV alone may not carry those details. If they are missing, the report marks the affected comparison and still uses the figures it can support. Passwords, tokens, user IDs and individual event records are not needed.

## Examples

- “Why does Traffic acquisition disagree with this Explore export? Here are both headers and quality indicators.”
- “Write September for my client from these two monthly exports. Keep event-scoped purchase credit separate from session acquisition.”
- “Turn this reconciliation into client copy and show how each monthly percentage was calculated.”

## Documentation and support

Read [PRIVACY.md](PRIVACY.md) for data handling and [BUILD-NOTES.md](BUILD-NOTES.md) for source checks and validation. Support: https://github.com/grayskripko/marketing-skills/issues

MIT. See [LICENSE](LICENSE).
