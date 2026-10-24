# Bookkeeping Cleanup

Check ledger exports for inconsistent categories, possible duplicates, transfers and missing documents or facts. Get a list of proposed corrections, linked to the original rows, for your bookkeeper or accountant to review before posting.

For small-business owners and bookkeepers. Supply readable ledger exports or pasted rows, your approved chart of accounts, the period, account meanings and currencies. No account connection, credentials or paid API is required.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not connectors. This working folder also contains development records in `tests/`, `REVIEW.md` and `BUILD-NOTES.md`; these are not runtime components and should be kept outside the submitted package.

These skills analyze only task text, attachments and local files that you explicitly supply, using bundled reference text. They permit your assistant's existing local calculation tools for exact decimal arithmetic or spreadsheet calculations. Reading CSV/XLSX attachments and scans can also use the assistant's existing file-reading and OCR tools. This is host tool use and may involve code execution and temporary files; no executable code is bundled and no software installation is instructed. If file-reading tools are unavailable, paste a small text table; if OCR is unavailable, supply readable text or CSV.

The skills do not instruct web search, URL or robots.txt retrieval, API calls, account connections, message delivery, publishing or settings changes. Intuit and Reddit URLs identify dated sources; GitHub URLs identify the publisher, repository, documentation or support. They are not retrieval instructions or connection endpoints used by the skills. A supplied URL is treated as text: paste the relevant content instead. QuickBooks Online actions such as undo, match, exclude, void or delete are recommendations for reviewer action, not operations performed by the assistant.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider still processes and may retain your conversation, attachments and tool activity under its own terms; this does not promise that the provider operates on your device. Any output file you explicitly request is created in the chosen workspace by your assistant's existing file tools, not by a bundled program. The plugin does not post bookkeeping corrections or send records elsewhere.

## What it does

| Skill | Give it | You get |
|---|---|---|
| review-categories | Ledger, approved chart, coding policy, prior examples and relevant receipts | Proposed category changes with reasons and questions about missing documents and facts |
| find-duplicates-and-transfers | Ledger and bank/card exports, account ownership and definitions of dates and signs | Duplicate and transfer findings linked to the original rows, including other possible matches that remain unresolved |
| prepare-cleanup-workpaper | Original records, findings and support | List of proposed corrections, table of all original rows, requests for missing documents and facts and checked calculations |

For supplied QuickBooks Online records, bundled dated Intuit guidance adds bank-feed state diagnosis, linked-record checks and reconciliation dependencies. Supply product/edition, feed state, linked record IDs, reconciliation evidence and attachments for those proposals. Sources are bundled; using the skills requires no network fetch.

## Examples

- “Review these expense categories using my chart of accounts. Flag anything you cannot justify.”
- “Find possible duplicate postings and transfers. Keep the source rows so my bookkeeper can check them.”
- “Turn these findings into a correction workpaper. April is closed; show what needs my accountant's decision.”

## What to supply

Include the business, period, currencies, accounting basis and jurisdiction when known; absent values stay unknown. Supply bank/card exports for duplicate and transfer comparisons, and confirmed details of who owns each account and what positive and negative amounts mean. Receipts and approved prior coding support proposals but do not by themselves prove business purpose. To confirm that the records agree with the bank, also supply opening and closing balances and items recorded in the books that have not yet appeared in the bank records. Matching rows alone cannot confirm this.

To read CSV or XLSX files, your assistant needs file-reading tools and local tools for exact decimal or spreadsheet calculations. For scans, it also needs a tool that reads text from images (OCR) and readable originals. If file-reading tools are unavailable, paste a small text table. If only OCR is unavailable, supply readable text or CSV instead of scans. Leave unclear text read from scans unresolved. The plugin supplies instructions, not an extraction engine. It requires no extra plugin runtime; model usage may cost money under your host's plan.

## How to use the output

The workpaper keeps original values and source locations. Suggested corrections remain proposals. Equal amounts alone do not confirm duplicates; repeated export copies are distinct from repeated ledger postings. Transfers need evidence that the accounts belong to the same business. Missing purpose, tax treatment, splits between business and personal use and questions about recording assets stay open unless approved source material resolves them. Each derived figure shows its formula and actual inputs, separately by currency.

Have your bookkeeper/accountant review before posting, especially closed-period changes. This is not an audit, tax advice, professional approval or proof that the books are complete or agree with the bank. It does not post entries, delete transactions, send messages, approve payments, reopen periods or file returns.

## Data and network

Network fetches: none. No web search, URL fetch, API call, account connection or telemetry. Work uses only authorized pasted text, files and exports; a URL alone needs its text pasted. No keys or credentials are needed. Redact personal names, contact details, account/card numbers and tax IDs; keep stable masked source labels.

The plugin runs no service and has no storage of its own. Your AI host processes the conversation and uploads under its own terms. When you request a workpaper file, the assistant writes it in the chosen workspace; manage or delete that file there. See [PRIVACY.md](PRIVACY.md).

## Support and license

[Report an issue](https://github.com/grayskripko/marketing-skills/issues) without financial records or personal data. MIT; see [LICENSE](LICENSE).
