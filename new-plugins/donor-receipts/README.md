# Donor Receipts

Review US donation acknowledgments and Givebutter receipts using gift records, approved benefit values, account status and campaign/account message settings.
For US nonprofit staff and fiscal-sponsor teams reviewing donor documentation.
Needs pasted receipts or gift exports, approved benefit values, beneficiary eligibility and relevant settings. No account, key or installation beyond the plugin is needed.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The Claude and Codex manifests describe the same skills for their respective hosts; neither launches a server.

Reviews use task text, attachments and files you explicitly supply. Both skills permit the assistant to retrieve relevant public www.irs.gov or help.givebutter.com pages and their necessary public source links when current-rule verification is needed, including gift-year benefit limits. These requests use the assistant's existing browsing tools, with no donor identities, gift records or account settings transmitted. This is an optional public-document retrieval workflow, so the plugin is not strictly offline.

The skills do not direct code execution, software installation, API calls, account connections or file writes. They return review text and drafts. Givebutter setting locations, campaign tests, receipt checkbox behavior and resend/retry guidance describe actions for an authorized user to perform in Givebutter; the assistant does not change settings, run account tests or send receipts. Repository, documentation, privacy and support URLs in metadata identify information pages rather than account connectors.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain your conversation and attachments under its own terms. Public-document retrieval contacts the referenced sites through the host's browsing tools.

## Skills

- **review-donation-acknowledgment**: correct a US acknowledgment and identify gift-level substantiation, timing and benefit-disclosure gaps.
- **review-givebutter-receipt**: reconcile an itemized receipt with supplied settings and draft the message repair at the right level.

Paste only the rows needed. Useful fields: gift reference, date, cash or property description, payment amount, goods/services and approved fair market value, fee and tip lines, refund status, acknowledgment received date, organization name and approved eligibility. For Givebutter, add verification/fiscal-sponsor status, account and campaign messages, and the displayed tax-deductible amount. Redacted donor labels work.

Returns review text and drafts. Account changes and receipt delivery are separate actions in Givebutter. Static campaign messages cannot fill donor-specific variables or safely cover mixed benefits with one fixed amount.


Source details: [IRS references](skills/review-donation-acknowledgment/references/sources.md) and [Givebutter references](skills/review-givebutter-receipt/references/sources.md). [Privacy](PRIVACY.md). [License](LICENSE).
