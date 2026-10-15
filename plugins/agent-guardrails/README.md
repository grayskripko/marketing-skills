# Agent Guardrails

Define and check agent permissions, human approval and escalation for a real workflow.
For people building or operating agents who need to decide which actions may run and who must approve or take over.
Needs your pasted tool list, workflow, policy, configs, traces, logs, transcripts or authorized files. No account, key, install or paid API is needed for a pasted-input review.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable runtimes.

The normal review uses task text, attachments and files you explicitly authorize, without plugin-directed network requests. This package is not strictly offline: only when you request a source refresh, the skills instruct your assistant's existing web tool to fetch the exact public official-documentation URLs you supply, the sites' robots.txt, and redirects to official documentation hosts. Those requests disclose the requested URLs and ordinary connection metadata to the destination sites and the assistant's tool provider; workflow contents must not be included in requests. The skills follow no unrelated links, perform no web searches, and do not connect accounts or call application APIs. If retrieval is unavailable, supply the relevant documentation as pasted text or an attachment.

The skills return reviewable text rather than executing code, installing software, applying settings or configuration changes, sending messages, publishing, deleting or paying. Controls Review can describe user-led integration steps: identify the runtime version, export redacted effective settings, prepare a change in an isolated application environment and capture scoped traces. Boundaries Check can propose a read-only lookup, a confirmed no-send mode or an explicitly authorized isolated action smoke with cleanup; it does not execute those application checks. Saving supplied logs is permitted only if you request an output file, using your assistant's existing file tools rather than a bundled program.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain your conversation, attachments and tool activity under its own terms. Source links identify documentation; they are retrieved only within the requested source-refresh scope above. Homepage and support links are not automatic connection endpoints.

| Skill | What you receive |
| --- | --- |
| [agent-authority-map](skills/agent-authority-map/SKILL.md) | An action matrix with allowed scope, approval triggers, owners and enforcing surfaces. |
| [agent-controls-review](skills/agent-controls-review/SKILL.md) | A reviewable approval design and configuration findings for the actual host. |
| [agent-boundaries-check](skills/agent-boundaries-check/SKILL.md) | Allowed, blocked and escalated path findings with the evidence supporting each conclusion. |

Start with whatever you have: “Which actions can this agent take, and when must it ask me?” Include the tools, what each changes, your constraints and any settings or trace excerpts. Redact credentials and unnecessary personal data. Missing runtime details become specific questions beside a useful draft.

The embedded control map covers Claude Code, Codex, Claude Agent SDK, OpenAI Agents SDK, MCP authorization and LangGraph interrupts. It checks callback bypass, checks that run too late, repeated effects on resume, approval scope and retrieval access boundaries. It produces planning and evidence artifacts; host settings and application code provide enforcement.

[Sources and control map](references/official-sources.md) · [Privacy](PRIVACY.md) · [License](LICENSE)

## Questions and feedback

If a skill works wrongly for your task, tell me in GitHub Discussions — I read every message: https://github.com/grayskripko/marketing-skills/discussions

Sergey Skripko. I build AI agents and fix poorly working skills.
