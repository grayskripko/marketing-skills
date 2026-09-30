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
- The instruction file is loaded at session start; the page suggests keeping it under 200 lines and moving workflow-specific instructions into skills, which load on demand.
- The prompt cache lifetime is one hour on a subscription, five minutes once you draw on usage credits, and five minutes by default on an API key or cloud provider; the first message after a longer break reprocesses the full context.
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
