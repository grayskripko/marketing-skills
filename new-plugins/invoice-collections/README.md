# Invoice Collections

Draft a proper overdue-invoice reminder and show whether I can add UK business late-payment charges.
For UK businesses chasing payment for goods or services. Provide the invoice details, agreed terms and payment history you have. Charge calculations also need an as-of or payment date. Paste text or an export, attach a readable screenshot, or describe its fields. No account, key, install or paid API is required beyond a host that supports skills.

## What this package runs and connects to

This package contains Markdown skills and reference text, JSON metadata, a static SVG icon, and development records in Markdown, text and JSON. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account.

The skills analyze invoice details, contract terms and payment history you explicitly supply as task text, attachments or selected local files. Both skills direct the assistant to recheck official guidance and retrieve dated rate history for charge decisions. Retrieval is limited to gov.uk, smallbusinesscommissioner.gov.uk, bankofengland.co.uk, legislation.gov.uk and bills.parliament.uk, including official document redirects to assets.publishing.service.gov.uk. These are actual retrieval destinations, not merely source links. Requests disclose public source URLs and ordinary connection metadata to those sites and the assistant's tool provider. Invoice text, names, amounts and other customer content must not be sent in URLs, search queries or calculator forms. With no browsing, the skills use the bundled dated reference or official extracts you supply and qualify unverified conclusions.

The late-payment-charges skill permits the assistant's existing date/decimal calculation tool, or carefully verified arithmetic, to calculate dates and charges from supplied values. This may involve host code execution; no calculator or executable code is bundled. Tool execution and any temporary calculation files are managed by the assistant provider. The skills do not direct software installation, account access, message delivery, publication, claim filing, payment collection, external invoice edits or output-file creation. Reminder messages and charge notices are returned as text drafts.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain conversations, attachments and calculation-tool inputs under its own terms. Repository and support links identify package information; the skills do not direct retrieval from them.

- **Overdue Reminder:** a friendly or firm reminder, with a separate check of any requested late-payment charges.
- **Late Payment Charges:** contractual/statutory eligibility, overdue dates, interest and one-off recovery compensation, with formulas and dated rate evidence.

For a reminder, provide the invoice reference, balance, due date and relevant payment history. Charge checks also need the debtor type, governing law, VAT-inclusive original debt, contract terms, dated payments, prior compensation and, where relevant, receipt/delivery dates and disputes. Missing details do not prevent a useful draft; charge figures stay conditional until their deciding inputs are known. The agent can walk you through copying these fields from your invoicing system. It does not connect to that system.

Example request: “Draft a friendly reminder for invoice RH-29, £720, due 30 September. My UK business client has not paid. Keep charges outside the email and tell me what you need to check them.”

Works across UK commercial late payments. Consumer charges, disputed legal entitlement, court filings and limitation advice are outside scope. Public-authority transactions require their own contract and timing checks. Messages and charge-invoice wording are drafts; nothing is sent, filed or collected.

For current rules and dated rates, the agent may fetch public guidance on gov.uk, smallbusinesscommissioner.gov.uk, bankofengland.co.uk, legislation.gov.uk and bills.parliament.uk, including official document redirects to assets.publishing.service.gov.uk. It sends no invoice text, names or amounts to those sites and does not submit calculator forms. With no browsing, use the embedded dated reference and a supplied official rate extract; label anything not currently verified.

Source snapshot checked 11 October 2026. The Commercial Payments Bill remains a bill in the Parliamentary stages reviewed; recheck status and commencement before relying on proposed changes.

[Privacy](PRIVACY.md) · [Source register](skills/late-payment-charges/references/uk-commercial-payments.md)
