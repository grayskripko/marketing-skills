# Agent Guardrails

Define and check agent permissions, human approval and escalation for a real workflow.
For people building or operating agents who need to decide which actions may run and who must approve or take over.
Needs your pasted tool list, workflow, policy, configs, traces, logs, transcripts or authorized files. No account, key, install or paid API is needed for a pasted-input review.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable runtimes.

The normal review uses task text, attachments and files you explicitly authorize, without plugin-directed network requests. This package is not strictly offline: only when you request a source refresh, the skills instruct your assistant's existing web tool to fetch the exact public official-documentation URLs you supply. Those requests disclose the requested URLs and ordinary connection metadata to the destination sites and the assistant's tool provider; workflow contents must not be included in requests. The skills follow no unrelated links, perform no web searches, and do not connect accounts or call application APIs. If retrieval is unavailable, supply the relevant documentation as pasted text or an attachment.

The skills return reviewable text rather than executing code, installing software, applying settings or configuration changes, sending messages, publishing, deleting or paying. Where evidence is missing they say which settings, records or trace excerpt would settle the question.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain your conversation, attachments and tool activity under its own terms. Source links identify documentation; they are retrieved only within the requested source-refresh scope above. Homepage and support links are not automatic connection endpoints.

| Skill | What you receive |
| --- | --- |
| [agent-permissions-map](skills/agent-permissions-map/SKILL.md) | A table of what the agent may do alone, what needs approval and by whom (from your policy), what is blocked and what is undecided. |
| [human-in-the-loop-review](skills/human-in-the-loop-review/SKILL.md) | Whether your settings enforce your approval policy, and the change that would. |
| [agent-boundaries-check](skills/agent-boundaries-check/SKILL.md) | A verdict per logged action (allowed, a violation, or not decidable) and the smallest check that would settle an open one. |

Start with whatever you have: “Which actions can this agent take, and when must it ask me?”, “Review these runtime settings against our human approval requirements.” or “Check these traces for actions taken before approval or after rejection.” Include the tools, what each changes, your constraints and any settings or trace excerpts. Redact credentials and unnecessary personal data. With no material pasted you get a general answer and the one thing to paste next.

Each skill carries short notes on Claude Code, Codex, Claude Agent SDK, OpenAI Agents SDK, MCP authorization and LangGraph interrupts, used only where they change the answer. The skills give advice; host settings and application code provide enforcement.

[Sources and control map](references/official-sources.md) · [Privacy](PRIVACY.md) · [License](LICENSE)
