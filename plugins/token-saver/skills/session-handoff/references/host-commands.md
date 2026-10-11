# Host commands

This is the only file in the plugin that names host-specific commands. Skills refer to actions in general terms ("the host's clear command") and point here. Each entry was checked against the vendor's own source on the date shown. If your host version differs, trust what your host shows.

## Claude Code

Source: Anthropic, "Manage costs effectively", code.claude.com/docs/en/costs, read 2026-09-30.

| Action | Command |
|---|---|
| Start fresh when switching to unrelated work | `/clear` |
| Summarize history, with an optional focus | `/compact` followed by what to keep, for example `/compact keep the failing test and the last error` |
| See what is using context | `/context` |
| See session token usage and plan usage | `/usage` |
| Switch model | `/model` |
| Lower the effort level | `/effort` |
| See configured servers and whether each is on | `/mcp` |

Notes from the same page, stated there, not measured by this plugin:

- The full conversation is sent with every request.
- Claude Code guidance: aim for CLAUDE.md under 200 lines by keeping essentials. Treat 200 as a default target, not a hard limit; preserve distinct always-needed rules even when the shortest complete essentials file exceeds it. Move workflow-specific material on demand only when it is unnecessary for other tasks. State the observed line count and any exception; line count is not a token budget. Do not transfer this target to other hosts.
- Claude Code default cache TTL: 1 hour within included subscription usage; 5 minutes on usage credits, API keys or cloud providers. Use the effective TTL shown by the host or configured for the relevant request bucket when available, including a forced 5-minute or requested 1-hour TTL. State the TTL and evidence used. Compare it with elapsed time since the last eligible model request, not typing. If host, billing mode, request activity or cache reuse is unknown, report expiry unknown; a reminder alone does not establish a cache refresh. Do not infer cost or a cache miss solely from displayed history or a typing break.
- Compaction reads the whole conversation it summarizes, so it is itself a large request. Clearing costs nothing.
- Thinking tokens are billed as output tokens.
- Verbose operations such as test runs and log processing can be delegated to subagents so only a summary returns to the main conversation.

## Codex CLI

Source: OpenAI, openai/codex repository, file codex-rs/tui/src/slash_command.rs (command descriptions), read 2026-09-30. Taken from the open-source repository at that date; the version you have installed may differ.

| Action | Command | Description in the source |
|---|---|---|
| Start a new chat | `/new` | start a new chat during a conversation |
| Clear the screen and start a new chat | `/clear` | clear the terminal and start a new chat |
| Summarize history | `/compact` | summarize conversation to prevent hitting the context limit |
| See configuration and token usage | `/status` | show current session configuration and token usage |
| Choose model and reasoning effort | `/model` | choose what model and reasoning effort to use |

## ChatGPT

No composer commands for context or usage are documented in a source this plugin could check as of 2026-09-30. To start fresh, open a new chat and paste the handoff note.
