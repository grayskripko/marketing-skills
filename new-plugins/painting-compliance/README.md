# Painting Compliance

Screen a US renovation/painting scope against EPA RRP paperwork triggers using property age, disturbed area, work type and supplied test evidence.
For painters, renovation estimators and rental property managers preparing a job or checking its paperwork.
Works from pasted scope text or exports. Property year/use, state, work dates, painted areas, methods and existing test or document evidence help; missing facts stay visible. No account, API key or installation beyond the plugin is required.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata. This working folder also contains development notes and text/JSON evaluation records; these are not a runtime and should be kept outside the submitted release folder.

The skills analyze scope text, pasted checklists, measurements, certificate details, test reports and document exports that you supply. They are not strictly offline: for current-rule questions or work after the embedded verification date, they instruct your assistant's existing browsing tools to retrieve relevant public EPA (`www.epa.gov`) and eCFR (`www.ecfr.gov`) pages, linked official state/Tribal administering-authority pages, and relevant `robots.txt`, following official redirects. The paperwork skill also opens the current linked clearance provision for dust-level disputes. The source registers call for rechecking deciding sections and applicable authority requirements for later work. These requests disclose the requested URL and ordinary connection metadata to the destination sites and browsing-tool provider; the skills prohibit sending project details in queries or requests. A public source URL can therefore be a retrieval target, not merely a citation. Private report links are not fetched.

No skill instructs code execution, shell commands, software installation, API calls, account connections, certification filing, message delivery or external writes. Calculations show formulas and supplied values. Blank forms are drafted only if requested; signatures, performance dates and results must come from the person who performed the work. Delivery, notification, recordkeeping and certification steps in the findings describe actions for the responsible people, not actions executed by the plugin. No skill directs output-file creation.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain your conversation, attachments and tool activity under its own terms. Pasted/exported inputs can be analyzed with embedded references without retrieval when no current-rule, later-work, local-requirements or dust-level verification is needed. If current verification cannot be obtained, supply the relevant official text and keep the affected conclusion conditional.

Two skills:

- **rrp-scope-screen:** room/exterior decisions, same-room 30-day aggregation, window/demolition exceptions, component-specific tests and the paperwork triggered.
- **rrp-paperwork-review:** document gaps, recipient-specific pamphlet delivery, certificate validity, completion information deadlines and retention dates.

Paste an estimate, work order, room measurements, test-report text or document checklist. The answer starts with your scope decision or gap table. Unknown facts stay visible. A mixed request screens the scope first and then reviews the packet.

The embedded references were checked on October 11, 2026. They include EPA guidance and current regulatory sections, recognized kit/substrate combinations, the zero-bedroom child exception and authorized program routing. Each skill keeps its deciding rules inline. For current-rule questions or later work dates, the assistant reads the relevant public EPA/eCFR pages and linked administering-authority pages, plus relevant robots.txt, following official redirects. It sends no job details in those requests. Pasted text and exports are the no-setup path.

The package contains instructions, references and an SVG icon. It has no connector, background service, account access or telemetry. Data handling: [PRIVACY.md](PRIVACY.md). Build decisions and checks: [BUILD-NOTES.md](BUILD-NOTES.md).
