# Roadmap Planning

Compare backlog options. Show how your estimates, dependencies and available capacity change what comes first and what waits.

For product and engineering owners preparing a roadmap decision. Give it a backlog table, goals, your scoring method and estimates, a planning period that matches the estimates and capacity, dependencies, commitments and capacity. Missing estimates remain visible. Pasted text or an export you name is enough; no accounts or paid APIs are required. Your AI app may charge for usage. To read an export or handle larger calculations, it needs file-reading and local calculation tools.

## What this package runs and connects to

This package supplies Markdown skills and reference text, JSON platform metadata, a static SVG icon and a license. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account.

The skills analyze data you provide for this task: backlog rows you paste, or the export you name or attach for this request. All four skills permit your assistant's existing local tools to read that export and bundled references and to calculate; those calculations may execute code in the assistant's tool environment. The decision model also permits available host calculation tools and explains how to interpret CP-SAT results if the host uses that solver. No solver is bundled or required, and the skills do not direct software installation. Tool execution and temporary files are managed by your assistant provider.

Nothing is fetched: the skills do not direct web search, URL or robots.txt retrieval, API calls, account connections, message delivery, tracker updates, roadmap publication, or account-settings changes. Source URLs identify Google OR-Tools and Intercom provenance; GitHub URLs identify documentation, privacy, repository, and support pages. They are references, not retrieval instructions or connection endpoints. For a supplied URL, paste the relevant content instead. Instructions to read linked decision procedures refer to bundled local Markdown files.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider processes and may retain request text, calculation inputs, and tool artifacts under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program. The skills themselves request no file writes or external sends.

| Skill | Give it | You get |
|---|---|---|
| prepare-priority-inputs | backlog, estimate sources, units and periods | comparable input rows and gaps that affect the comparison |
| compare-roadmap-options | alternative choices, dependencies and capacity | included and deferred work, totals and reasons |
| test-priority-assumptions | base case and supplied ranges or scenarios | changed scores, order and displaced work |
| write-roadmap-decision | comparisons and an approved or proposed choice | a short decision note for review |

## Try it

- “Check this backlog export. Are the estimates comparable?”
- “Compare adding the new feature with keeping our current plan. What work is deferred?”
- “Use these effort ranges to show which priorities change.”
- “Turn this approved choice into a note for our roadmap meeting.”

A score is based on your estimates. It is not an objectively correct roadmap. The output separates item scores, dependency-closed packages within each team budget, and calendar feasibility with release gates. A package winner requires an agreed incremental-value objective. Joint range checks test fixed-scope capacity separately from timing and outcome superiority. The shipped [decision model](skills/compare-roadmap-options/references/decision-model.md) includes worked examples and [dated official sources](skills/compare-roadmap-options/references/sources.md). Product and engineering owners review the result before making commitments.

This is for backlog tradeoffs. It does not write general PRDs, conduct discovery, update trackers, publish a roadmap or make customer promises.

## Data and network

No plugin-directed network retrieval or account access is specified. The skills read only the export you name for the task; they do not scan folders or projects, read every attachment, or use memory, chat history, conversation summaries or Claude conversation exports. Local reads of that export and bundled references and calculation execution are permitted as described above. Requested output files are saved by your AI app, not by a plugin service. Minimize customer and employee details; stable item IDs usually suffice. Your AI provider's processing and retention terms apply. See [PRIVACY.md](PRIVACY.md).

## Troubleshooting

Unreadable export: paste the relevant table rows or name a readable text/CSV export. URL input: paste the relevant content. Mixed units or periods: supply comparable inputs; the output does not guess conversions. Missing ranges: you still get the assumptions that need evidence, without invented scenarios.

## Support and license

[Report an issue](https://github.com/grayskripko/marketing-skills/issues). MIT; see [LICENSE](LICENSE).
