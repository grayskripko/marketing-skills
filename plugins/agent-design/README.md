# Agent Design

Design an AI agent for one process: decide whether an agent is needed, then write its implementation specification.
For process owners and developers planning one business workflow. Paste process notes, traces, logs, configs, transcripts or files; no account connection, API key or install beyond the plugin is required.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not servers.

The design workflow uses task text, attachments, and files you explicitly supply or identify, plus the bundled source notes. It does not direct code execution, software installation, business API calls, message delivery, deployment, or account changes. When requested, it outlines the chosen SDK/runtime installation, scoped service access, secret storage, and persistence as implementation dependencies; those are planning details, not actions performed by this skill. Output files are saved only when you request them, using your assistant's existing file tools.

This package is offline by default, with an optional network workflow: only if you ask to refresh platform guidance, the assistant may fetch official documentation URLs in [references/sources.md](references/sources.md) and their official redirects, or exact public documentation URLs you supply for the chosen stack, using its existing browsing tool. Registered destinations are `www.anthropic.com`, `docs.cloud.google.com`, `code.claude.com`, `learn.chatgpt.com`, `openai.github.io`, `modelcontextprotocol.io`, `developers.openai.com`, `docs.langchain.com`, and `developers.llamaindex.ai`. These requests disclose the requested URL and ordinary connection metadata to the documentation sites and the assistant's tool provider. They do not upload your process notes, logs, configs, transcripts, or files. No web search or login is directed. Paste the relevant documentation instead when browsing is unavailable or unwanted. Repository and support links identify project pages, not automatic retrieval or message-delivery instructions.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider processes and may retain your conversation, attachments, and tool activity under its own terms. Requested output files are managed by your assistant and host, not by a bundled program.

| Skill | Your input | Your result |
|---|---|---|
| agent-process-scope | Steps, transcripts, logs and available data | A process map with decisions, action boundaries and human ownership |
| agent-architecture-decide | A process and constraints | An agent vs workflow decision, including single-call and code-only options |
| agent-build-spec | A process, chosen architecture and tool/config details | An agent specification with interfaces, retrieval, review, stopping conditions and acceptance checks |

Ask for the whole design or just one stage. Each skill works on its own. A full request gets one combined specification rather than three repeated reports.

The implementation brief checks the chosen stack's approval behavior, MCP error and continuation results, and persistence after interrupted review. Process mapping and the agent vs workflow decision keep that brief tied to the actual work.

Current official guidance is embedded in the skills and dated in [references/sources.md](references/sources.md): Claude Code settings, Codex permissions, MCP tool results, OpenAI and Claude Agent SDK controls, public evaluation and retrieval guidance, LangGraph persistence, LlamaIndex and Google's architecture patterns.

## Examples

- “Map our equipment-return process from this staff transcript before we choose AI.”
- “Should this fixed approval process use an agent or a workflow? Here are its steps.”
- “Write the build specification for a read-only investigator using these MCP schemas and SDK settings.”

## Inputs and access

Pasted text and supplied exports are the default path. The assistant reads only files you supply or identify for this design; large artifacts can be narrowed to relevant sections. The specification records missing live access as an implementation dependency. If you request setup guidance, the brief outlines the chosen SDK/runtime installation, scoped service access and secret storage that an implementer needs; use redacted configuration, never credentials in chat. Proposed paid services or extra infrastructure require a reason tied to this process.

The optional documentation-refresh workflow and its destinations are described above. Pasted documentation supports the same design path without additional network requests.

Deliverables are designs and implementation briefs. Application building, deployment, live monitoring, incident repair, detailed tool implementation and worker coordination belong to their respective workflows.

Support: https://github.com/grayskripko/marketing-skills/issues

MIT. See [LICENSE](LICENSE).
