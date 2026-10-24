# Contractor Contracts

Check a California home-improvement agreement or initial quote for required fields, deposit arithmetic, payment milestones and applicable bond exceptions.
For homeowners, tenants and contractors reviewing residential improvement paperwork.
Needs pasted text or a readable document export. No accounts, keys, installs or paid APIs are required.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The folder also contains text-only development notes and evaluation records; these are not a runtime.

Normal checks use only task text, attachments, and local files you explicitly supply or select, together with the bundled reference snapshot. Both skills permit an optional network action: when you request current-source verification, your assistant may retrieve the official CSLB and California Legislative Information URLs listed in the skill references, following redirects only within those official domains (`cslb.ca.gov`, including `www.cslb.ca.gov`, and `leginfo.legislature.ca.gov`). The source registers also direct release-time verification of current official text. Retrieval uses your assistant's existing web tools, not a bundled connector. Requests expose the requested public URL and ordinary connection metadata to the official sites and the assistant's tool provider; contract text, personal data and contractor identifiers must not be put in URL queries. If retrieval is unavailable, supply the relevant official text or use the dated snapshot with current verification unresolved. Contractor-specific license and bond checks rely on supplied exports, without automatic registry lookup.

The skills do not direct code execution, software installation, API calls beyond the public-page retrieval described above, account connections, message delivery, publication, or settings changes. Contractor replies and corrected notices are drafts returned in the conversation. Statutory quotations that describe calling, writing, paying or sending cancellation notices are reference text for the user, not assistant actions. No skill directs output-file creation; any file you explicitly request is saved by your assistant's existing file tools, not by a bundled program. The GitHub support link is a support destination, not an automatic connection.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Optional official-source retrieval makes network requests; ordinary supplied-material checks do not.

| Skill | Give it | Get |
|---|---|---|
| contract-check | quote, proposed or signed agreement, attachments, change order | prioritized field and notice corrections, payment calculations, short contractor reply |
| payment-check | price, deposit, milestones, payment request, bond or joint-control evidence | deposit calculation, reconciled schedule, premature-payment findings, exception assessment |

An initial quote gets additions needed before acceptance or signing. Signed terms get proposed amendments. An incomplete export produces findings about supplied pages and requests for omitted material. The checks include January 2026 email, cancellation-help phone and subcontractor disclosures. Payment exceptions depend on the supplied security evidence, not the words “licensed and bonded.”

Paste the project’s California location, document stage and date, contract price, finance charges, all payments and their triggers. Include relevant attachments and any bond text or CSLB record export. Redact homeowner addresses, signatures and account numbers that the check does not need. Preserve labels linking a bond to the same contractor and project.

Examples: “Can I accept this bathroom estimate?”; “They want 20% to order materials; does this bond change the cap?”; “Check the payment total and milestones.”

## Sources and supplied documents

The embedded reference snapshot was checked on 2026-10-11. Sources and their dates: [California rules](skills/contract-check/references/california-rules.md). If an export loses formatting, supply the original page to check type size, boldface and notice placement. Redact unnecessary personal data before supplying documents.

## License and support

MIT; see [LICENSE](LICENSE). Support: https://github.com/grayskripko/marketing-skills/issues
