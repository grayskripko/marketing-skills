# MCP Debugging

Troubleshoot MCP connection, authentication and missing-tool errors in your actual client from pasted traces, logs, configs, transcripts or files. For developers and teams using Claude Code, Codex or agent SDKs. You need redacted material and the client name; reviewing supplied text needs no new account, API key or installation.

| Skill | Give it | You get |
|---|---|---|
| mcp-connect | client name, config and startup output | the cause, a minimal client-specific fix and one safe check with what each result means |
| mcp-tool-check | discovery trace, schemas and call results | missing-tool or failed-call repair and what the actual result proves |

Try "This config works in Claude Code but fails in Codex" or "The server connects, but the search tool is missing." Attach the relevant file or paste the redacted section. Keep secrets out of the conversation.

## What this package runs and connects to

A skills-only package: Markdown instructions, a [dated official source register](references/sources.md), JSON metadata and a static SVG icon. It bundles no scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes, and installing it launches nothing. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not servers.

The skills read only the text and files you provide. They may suggest steps you run yourself: editing local JSON/TOML configuration, `claude mcp get`, `claude mcp remove <name> --scope local`, `claude mcp login <name>`, `codex mcp list`, `codex mcp get`, `codex mcp login <name>`, `/mcp`, checking that an environment variable is set without printing it, or piping one `initialize` message into a server you run yourself. Restarting a client or running a server command launches that server. Suggested checks are chosen to be harmless; the skills do not treat message delivery, purchases, account-data writes or permission broadening as checks, and pasted commands are not run just because they appear in a config.

## Data and network

Default network fetches: none. If you ask for current documentation, the assistant may read official pages on code.claude.com, learn.chatgpt.com, developers.openai.com, modelcontextprotocol.io, openai.github.io, docs.langchain.com or anthropic.com; no trace or config is sent in a search query. If you authorize a live check through a client you already have connected, it contacts only your named server and its authentication provider. The publisher runs no collection, telemetry or storage service for this plugin. Your assistant provider processes your conversation under its own terms. See [PRIVACY.md](PRIVACY.md).

## Support and license

[Report a problem](https://github.com/grayskripko/marketing-skills/issues). MIT; see [LICENSE](LICENSE).
