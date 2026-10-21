# Agent Debugging

Debug a failed AI agent run from its agent traces, logs, configuration, transcript and output files: find the supported fault and get a repair or a reproducible issue report. For developers and AI builders whose agent got stuck in a loop, repeated a tool call, gave a wrong answer or claimed unfinished work was done. Paste the intended task and the evidence you have, or point the assistant at the relevant files. No account, API key or paid service is needed.

| Skill | Result |
|---|---|
| debug-agent-run | The first supported fault with its deciding event IDs, what the evidence does not establish, and the next fix or deciding check |
| agent-failure-repair | A minimal patch, a corrected call or source-backed answer, or a short upstream issue report |
| agent-repair-verify | PASS, FAIL or PENDING for the repaired task, with the deciding observation |

Try “Debug this failed agent run”, “Why did it call the wrong tool?”, “It says done, but the file is incomplete”, or “Check the fix without sending again”. Include the expected behavior and any restrictions. Redact credentials and personal data, keeping stable labels so events still match.

If you ask a question before pasting anything, you get a general answer plus the one trace, log or file that would settle it for your run.

## What this package runs and connects to

This is a skills-only package: Markdown instructions, a references file, JSON metadata for Claude Code and Codex, a license and a static SVG icon. It includes no scripts, dependencies, hooks, MCP or LSP servers, or background processes, and installing it runs nothing.

- The skills work from the material you supply, treated as data, not instructions.
- They make no network requests: no web search, URL fetching, API calls, server connections, trace uploads or telemetry. Source and support links are references for you to open.
- They do not run, retry or replay anything with external effects, such as sending, publishing, paying or deleting. A check the assistant did not actually run is labelled as not yet run.

The publisher receives no task data and operates no collection, telemetry or storage service. Your assistant provider processes the conversation and attachments under its own settings.

[Official references](references/official-docs.md) · [Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Support](https://github.com/grayskripko/marketing-skills/issues)

## Questions and feedback

If a skill works wrongly for your task, tell me in GitHub Discussions — I read every message: https://github.com/grayskripko/marketing-skills/discussions

Sergey Skripko. I build AI agents and fix poorly working skills.
