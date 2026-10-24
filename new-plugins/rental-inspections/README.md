# Rental Inspections

Check an EICR (electrical safety certificate) for a rental property in England: expiry, required work and tenant or council copies. Check a social landlord’s supplied-appliance inventory and safety records.
For landlords, letting agents and social-housing teams reviewing England rental records. Needs pasted report text or selected exports, an equipment list, tenancy dates and any request, delivery or completion evidence. No accounts, keys, installs or paid APIs are required.

For England electrical records; gas safety reports and physical electrical testing are outside these skills.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable connectors. Development notes and evaluation records currently remain in this folder; they are not runtime components.

The skills review pasted text, attachments and local exports that you explicitly select. October 2026 reviews use embedded references and need no network requests. For date-sensitive later cases, including inspections or decisions on or after 30 November 2026, the assistant may use its existing browsing tools to retrieve the listed official sources and additional pages on gov.uk or legislation.gov.uk needed to verify current guidance, the final made instrument, commencement and saving provisions. It also retrieves those sites' robots.txt, respects restrictions and keeps redirects within those domains. Searches use public instrument titles and dates only. You may supply current official text instead.

These optional requests disclose requested public URLs, public search terms and ordinary connection metadata to the visited sites, search service and assistant tool provider. Report content, tenant details and private context must never appear in requests or queries. The skills do not direct code execution, software installation, API integrations, account access, file writes, message sending, publication or account changes. Instructions about notifying tenants, delivering records, arranging work and retaining evidence describe landlord duties and review recommendations; the assistant does not perform them.

The publisher operates no task-data collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain the conversation, attachments and tool activity under its own terms. Source URLs can be retrieval destinations in the verification workflow; the support URL is a reference for users to open themselves.

| Skill | Ask it to do | Result |
|---|---|---|
| rental-electrical-report | Check an EICR, findings and tenancy/delivery dates; use first for a combined packet | Finding-specific actions, dated work and copy deadlines, next inspection and missing evidence |
| rental-equipment-inventory | Match landlord-supplied items to safety records and written requests | Item actions, check dates, unsafe-equipment follow-up and record recipients |

Paste report/export text with property and item aliases. Include landlord sector, tenancy grant and occupation dates, inspection/check dates, findings, next due dates and whether requests were written. Keep C1/C2/FI/C3 exactly as recorded. The review separates fixed installations from supplied equipment and applies the social-tenancy first-check deadline before 1 November 2026.

Examples: “Can I re-let with this C3-only EICR?”; “Which supplied appliances still need records before November?”; “When do these council-request copies and work confirmations fall due?”

## Sources and network

The embedded [source register](references/sources.md) records official guidance and regulations verified on 11 October 2026. A later draft amendment has its own status and date guard. The execution and connection scope above describes the optional current-rule verification workflow; this package is not globally offline.

## Privacy and license

Redact tenant names, full addresses and signatures where aliases suffice. See [PRIVACY.md](PRIVACY.md) and [LICENSE](LICENSE). Support: https://github.com/grayskripko/marketing-skills/issues
