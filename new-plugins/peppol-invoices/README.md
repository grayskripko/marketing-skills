# Peppol Invoices

Review supplied Peppol BIS Billing invoice and credit-note XML, explain rejections, and give my invoicing provider the exact fixes.
For finance teams and invoicing providers using Peppol BIS Billing 3.0. Needs pasted rejection text and invoice XML, exported fields, or a screenshot described in words. No account, key, installation or paid service is required for review.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON platform metadata, and a static SVG icon. It bundles no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not launch a bundled program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata. Development notes and evaluation records are also present in this working folder; they are not runtime components.

The skills review task text and files you explicitly supply and draft corrections or a provider ticket. They also permit the assistant's existing web tool to retrieve public specifications, rule pages, code lists and release tables from `docs.peppol.eu` and `peppol.org`, plus those sites' `robots.txt`. These requests disclose the requested public URL and ordinary connection metadata to those sites and the assistant's tool provider. Off-domain redirects and bypassing a robots disallow are prohibited. Invoice content and identifiers must never enter requests, search queries or remote validators. This optional retrieval makes network requests. Without browsing, the skills use bundled references and supplied evidence, flag relevant freshness uncertainty, and refer unresolved rules to the provider.

The assistant may read supplied local files and use its existing local arithmetic tools; those tools may execute calculations in the host environment, with execution and temporary files managed by the assistant provider. No calculation program or validator is bundled. Output files are created through the assistant's existing file tools only if you explicitly request them. The skills do not install software, connect provider accounts, call provider APIs, upload or transmit invoices, send messages, or change invoices or account settings. You send any drafted ticket; your provider regenerates and validates the full payload and checks delivery separately.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider processes and may retain conversations, attachments and tool activity under its own terms. Source URLs can be retrieved within the limits above; GitHub documentation and support links identify package information and support, not invoice-processing endpoints. See [PRIVACY.md](PRIVACY.md).

| Skill | Your request | Result |
|---|---|---|
| invoice-rejection-diagnosis | “Why did this Peppol export fail?” | Evidence-based field corrections and reconciled amounts |
| invoice-provider-handoff | “Write the exact fixes for our invoice software vendor.” | A support ticket with corrections, unknowns and retest requirements |

Reviews cover identifiers, arithmetic and country-specific rule context against the supplied standard version.

Paste the full error message if available, affected XML or fields, seller/buyer countries, invoice versus credit note, and validation release if known. Keep identifier scheme codes visible; redact personal identifiers, bank details and addresses. If you only have a screenshot, describe its text and the fields visible. A missing field in a cropped screenshot does not prove the export omits it.

The embedded rule reference covers the May 2026 release (3.0.21), mandatory from 17 August 2026, checked 11 October 2026. It includes field mappings, current code choices, VAT categories, arithmetic and changed error severities. It supports targeted review, not complete schema/Schematron validation or guaranteed network acceptance. PINT and self-billing use different specifications. Your provider must validate the regenerated payload and investigate delivery failures.

No provider connection is included. To obtain better evidence, the assistant can walk you through locating your provider's export and validation-report screens once you name the product. It must not guess menu paths or ask for credentials. Pasted fields and described screenshots remain available without setup.

See [the dated rule reference](references/peppol-billing.md). MIT; see [LICENSE](LICENSE). Support: https://github.com/grayskripko/marketing-skills/issues
