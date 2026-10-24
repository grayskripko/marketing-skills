# Tool Autopsy

Find why an agent's tool call failed and get a repair you can verify. For developers and AI builders using Claude Code, Codex, MCP or agent SDKs. Give it a pasted trace, redacted configuration, tool schema, code excerpt or file you explicitly choose; no observability account, API key, install or paid service is required for analysis.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account.

These skills work only from task text, attachments, and local files that you explicitly supply. They do not instruct the assistant to run code, install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. URLs in this package identify sources or support pages; they are not connection endpoints or retrieval instructions. A supplied URL is treated as text: paste the relevant content instead.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

Verification plans may recommend later checks using your host or service: read-only discovery or lookup, a documented no-send path, or a minimal real write only after authorization for its exact target and side effect. Those checks can run tools, contact the relevant service, or change its state. They remain planned or pending; these skills do not perform them. Destinations and data depend on the supplied host and service contract, not a plugin-owned endpoint.

| Skill | Give it | You get |
|---|---|---|
| tool-trace-diagnose | a failed run and the intended task | earliest supported failure, an event-linked timeline and a proposed fix |
| tool-contract-repair | settings or tool arguments, schema and error | corrected arguments or a minimal configuration patch |
| tool-replay-plan | failed call, proposed repair and runtime details | safe reproduction checklist with expected observations and pass/fail conditions |

Try: "Read this failed run and explain why it keeps repeating the lookup." Or: "Here are my tool schema and arguments; show the smallest correction." Or: "Make a verification plan without sending the message again."

Paste exports directly or attach only the files needed. Redact tokens, cookies, authorization headers, private endpoints and personal data. Keep stable replacement labels for matching requests to responses. If the trace is incomplete, the answer gives the supported finding and asks for the deciding missing detail.

This package contains skills and reference text. It returns reports, patches and plans; it does not apply patches, run commands, connect to an MCP server, collect traces or replay tool calls. A verification plan states what remains pending. Connection success, runtime enforcement and repair success require evidence from the actual host.

Network scope during use: none. No web searches, URL fetches, robots.txt requests, server calls, downloads or telemetry. Files are read only when explicitly supplied for the task. Official documentation is embedded in [references/official-docs.md](references/official-docs.md), with version scopes and source dates. Supplied URLs are treated as text, not opened.

No setup is needed for the supplied-artifact path. If you later want to execute a plan, that is separate work using your host's installed tools, documented interface and existing authentication. Do not paste credentials. A write check needs authorization for its exact target and side effect; existing receipts are inspected before proposing a retry.

[Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Support](https://github.com/grayskripko/marketing-skills/issues)
