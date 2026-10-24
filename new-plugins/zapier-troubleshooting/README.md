# Zapier Troubleshooting

Troubleshoot Zapier setup, authentication, mappings, filters and paths, rate limits, and failed or held runs.

For people setting up or maintaining Zapier workflows. Paste run details or an export, or describe a screenshot. Analysis needs no installation, API key, or account connection. Following the recovery steps requires access to the relevant Zapier account; some replay modes require a paid plan.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The Claude and Codex manifests describe the same skills for their respective hosts; neither provides a connector.

The assistant analyzes only task text, attachments, exports, and local files that you explicitly supply, together with bundled references. The skills do not direct the assistant to run code, install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, change account settings, or write files. Pasted links are evidence, not instructions to retrieve them; paste the relevant content instead.

The workflow also gives user-led external steps: checking current official Zapier help in your browser when behavior conflicts, inspecting Zap History and destination records, reconnecting apps, correcting and publishing workflow edits, resolving billing or access restrictions, changing autoreplay settings, cancelling or excluding held runs, and initiating tests or replays and checking their results. Where replay is unavailable, it may recommend manual record creation and notification. You perform these actions in Zapier or the relevant destination app; they can use network connections, incur charges, and create records, send messages, or repeat payments or shipments. The assistant does not perform them. Official help links identify supporting sources, and the support link leads to public GitHub issues; opening them yourself uses those services.

The publisher receives no task data through this plugin and operates no collection, telemetry, or storage service for it. Your assistant provider still processes and may retain your conversation and attachments under its own terms. If you choose to post a public support issue, GitHub and its readers receive what you submit; do not include run payloads or secrets.

## What you get

- **Diagnose Zap runs:** a systematic review of supplied history and audit logs, the likely setup, account, mapping, branching, or rate-limit cause, the smallest fix, and evidence needed to check it.
- **Plan Zap replay:** a run-by-run decision, the appropriate replay mode, duplicate checks, and an estimate of additional tasks where the inputs support one.

Use either skill alone. For “fix these and tell me which to replay,” diagnose first and give one combined recovery table.

## What to provide

For setup issues, include the selected app/event, connection status, permission error, required-field configuration, and observed test result. For branching, include actual condition values and the selected path. Supply relevant audit-log entries with timestamps, timezone, actor, and configuration changes when available.

Run reference, original trigger time and timezone, run status, failed/held step and message, relevant Data In and Data Out, successful earlier actions, downstream actions, current plan and available tasks, and any edits since the failure. Include scheduled retries and whether the destination already contains the record or message. Partial inputs still produce a useful diagnosis; unknowns remain explicit.

In Zapier, open Zap History, choose a run, and inspect the affected step's Data In and Data Out. Copy only the fields needed to diagnose it. Redact personal details and authentication data. The agent can walk you through reading these screens and checking replay choices. Described screenshots are supported; attach an image only if your assistant can read images.

## Boundaries and network

This is advice from supplied evidence, not live monitoring or account control. It supplies no connector, account access, executable script, or replay automation. The user performs reconnects, publishes edits, approves costs, and initiates replays in Zapier. A recommendation cannot guarantee successful delivery or no duplicates.

Assistant analysis uses bundled, dated official-source notes and your supplied material without additional network requests. User-led browser checks and recovery actions use external services as described above. No telemetry or package-owned storage. Assistant-provider conversation and file policies still apply.

Official rules were checked on 2026-10-11, with two sources added on 2026-10-13; see [source register](references/zapier-recovery.md).
