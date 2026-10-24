# Indeed Listings

Check an Indeed job posting or explain why it is not showing up.
For employers and recruiting teams reviewing an already approved vacancy. For a posting check, supply the approved text, country and actual role/location details. For missing-job help, start with the exact message or search observation and country; add status, posting-history or budget evidence when it changes the diagnosis. No employer-account connection, credentials or paid API is needed for pasted-text checks.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON platform metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a bundled program or connect an employer account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable servers.

Both skills analyze task text and files you supply and instruct the assistant to refresh the deciding public Indeed policy/help page when browsing is available. The assistant's existing browsing tools may retrieve official Indeed URLs, locale variants and linked policy pages on Indeed domains, including `www.indeed.com`, `ca.indeed.com` and `uk.indeed.com`; legacy official links may redirect through `indeedinc.my.site.com` to `indeed.com`. Public source discovery may use the assistant's web search with public policy terms and locale only. These requests expose requested URLs or search terms and ordinary connection metadata to the destination sites, search service and assistant tool provider. Private posting text, applicant data and account identifiers must not be sent in queries. The bundled ONS postcode link is geography evidence, not an additional runtime retrieval destination; GitHub links identify source/support pages.

This workflow makes public network requests when browsing is available; it is not strictly offline. Without browsing, use the dated bundled references and current policy excerpts you supply, leaving changed or unsupported rules unresolved. The skills do not direct code execution, software installation, API calls, file writes, employer login, publishing, budget/billing changes or message delivery. Corrections and support drafts are returned as text. They may recommend that you correct an existing Indeed or ATS posting, complete account verification directly in Indeed, contact support, reopen an authorized vacancy or review a budget choice; you perform those external actions yourself.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain your conversation and supplied files under its own terms.

- **check-indeed-posting:** returns necessary title, location and description corrections while preserving approved terms.
- **diagnose-indeed-visibility:** explains why a job is not showing up using messages or search observations, account status, posting history, daily spend, grouping and applicable free-post limits.

Add direct-post versus ATS origin, onsite/hybrid/remote arrangement, actual worksite or residency restrictions, posting dates, current status and redacted budget records when relevant. A supplied CSV or text export is also accepted; column labels and timestamps stay attached to their values.

Official knowledge includes location field rules, duplicate/reopened-post handling, daily-limit visibility, grouped jobs and the direct-post free limits. See the skill-local [posting sources](skills/check-indeed-posting/references/indeed-policy.md) and [visibility sources](skills/diagnose-indeed-visibility/references/indeed-policy.md).
