# Substack Migration

Prepare the subscriber import from my old newsletter export and flag what happens to my paid readers.
For newsletter owners moving subscribers to Substack. Bring pasted rows, a selected export, or screenshots described in text; preparation needs no account, key, install, or paid API. Performing the handoff needs your Substack publication; paid setup may also need your Stripe account, which you manage yourself.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. BUILD-NOTES.md and REVIEW.md are development documentation, not runtime components.

The skills analyze task text, attachments, selected local exports, and screen descriptions you explicitly supply. The import skill directs the assistant to use available local tools to create requested files and a CSV-aware parser for quoted fields. File reading, parsing, calculations, and output creation use the assistant's existing tools; no parser or executable program is bundled. The skills do not instruct software installation, shell commands, or API calls.

This workflow has an explicit network exception: only when you request a rules refresh, both skills permit public Substack help searches and retrieval of official pages on support.substack.com and substack.com, including redirects. Subscriber data, credentials, and private URLs must not be included in those requests. Bundled source links otherwise identify reference material; the GitHub issues link is a support destination, not an automatic connection.

The skills prepare files and native account handoffs. You perform exports/downloads and ZIP extraction, imports/uploads, Stripe setup and Ghost revocation, approved billing/access changes, support requests, and message sending yourself. The assistant does not connect accounts, upload subscriber files, send messages, or execute billing changes.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider processes and may retain conversations, attachments, tool activity, and requested files under its own terms. Local output files are created by your assistant's existing tools, not a bundled program.

- **prepare-substack-import:** map fields, separate exceptions, prepare email-only upload batches and an import checklist, and reconcile supplied results.
- **plan-paid-reader-migration:** separate access from billing, preserve paid-through dates, identify the documented Ghost transfer path, and prepare a cohort handoff.

Start with the source platform, export headers and rows, consent/suppression status, move date, and any paid-through or renewal dates. For a sample, the result covers that sample only. Mask addresses for planning; real import files need the real addresses. Extra fields stay in a local reconciliation file rather than being promised as supported Substack fields.

The agent can walk you through native settings. You log in and confirm imports, payment setup, billing changes, and messages. There is no account connection or automatic move. CSV preparation does not transfer payment authorization. Archive/content and domain migration are outside this package.

Network: ordinary use fetches nothing. If you ask to refresh the documented rules, the assistant may search public Substack help pages and open official pages on support.substack.com and substack.com, including their redirects. No subscriber rows, addresses, payment details, private URLs, or credentials are sent in searches or page requests. There is no telemetry or dependency download.

Sources are in [subscriber import references](skills/prepare-substack-import/references/substack-import.md) and [paid-reader references](skills/plan-paid-reader-migration/references/paid-readers.md), verified on 2026-10-11. Check current native screens before using the handoff, especially if they differ from these sources.

[Privacy](PRIVACY.md) · [MIT license](LICENSE)
