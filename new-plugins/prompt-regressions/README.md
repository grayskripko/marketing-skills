# Prompt Regressions

Check whether a prompt change broke the behavior you need before you ship it.
For developers and skill authors reviewing an existing agent workflow.
Needs your previous and changed prompts, existing acceptance requests, and either runner configuration or exported results. Pasted files work without an account or installation.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON platform metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. The `.claude-plugin` and `.codex-plugin` directories are platform metadata, not runtimes. Installing the package does not run a program or connect an account.

Preparation from supplied prompts and review of exported results need no installation or network retrieval. The skills can also propose commands or a patch for your supplied runner and create explicitly requested output artifacts through your assistant's existing file tools. This package is not limited to offline use: requested documentation verification retrieves the linked official pages on code.claude.com, developers.openai.com (including its learn.chatgpt.com redirect), modelcontextprotocol.io and openai.github.io. Those sites and the assistant's web-tool provider receive the requested URL and ordinary connection metadata.

For explicitly requested execution, the assistant may inspect local CLI help, use the runner's supported login/status flow, prepare its configuration, and run your existing Claude Code, Codex or OpenAI Agents SDK workflow. Installation is a prerequisite, not an automatic action; separately authorized dependency installation contacts the selected package registries. Execution can send prompts, inputs and tool arguments to your configured model provider and MCP endpoints, incur provider charges, write run artifacts and cause the configured tools' side effects, including external writes or sends where authorized. The actual destinations and actions depend on your supplied runner configuration; the skills require authorization for its reads, writes, network calls and paid usage and forbid bypassing permissions.

The publisher operates no collection, telemetry or storage service and receives no task data through this package. The skills prohibit uploading supplied traces to other services. Your assistant provider processes and may retain conversations and attachments under its own terms; an authorized runner's providers, endpoints and logs have their own processing and retention rules. No credentials should be pasted into the conversation.

## Skills

- **prepare-release-check** turns supplied requests and expectations into a case contract and capture plan for your existing runner.
- **inspect-run-results** turns supplied outputs and traces into a release report separating behavior failures, execution errors and missing evidence.

Examples: “Prepare a release check for these prompt versions and our JSON contract.” “Read these exported runs and tell me which required behavior broke.”

The skills include documented Claude Code, Codex, MCP and OpenAI Agents SDK distinctions. They integrate with the runner you supply; they ship no runner, hosted service, hooks or MCP server. They do not rewrite prompts automatically or promise model-wide reliability. Export review is the no-setup path; it does not execute or monitor an agent.

Sources and observation dates are in each skill's references/official-sources.md. See PRIVACY.md for processing and BUILD-NOTES.md for build validation and release status.
