# MCP Debugging

Troubleshoot MCP connection, authentication and missing-tool errors in your actual client from pasted traces, logs, configs, transcripts or files. For developers and teams using Claude Code, Codex or agent SDKs. You need redacted material and the client name; reviewing supplied text needs no new account, API key or installation.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It bundles no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing the package does not launch a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not servers. `tests/`, `REVIEW.md`, and `BUILD-NOTES.md` are development records, not runtime components; keep them outside the submitted release folder.

The supplied-material diagnosis reads only task text and files you explicitly provide; it needs no network fetch or code execution. **The complete plugin is not an offline-only workflow:** its skills retain these optional actions and repair instructions:

- At your request, the assistant may fetch relevant official documentation and redirects on code.claude.com, developers.openai.com, learn.chatgpt.com, modelcontextprotocol.io, openai.github.io, docs.langchain.com, and anthropic.com. Your traces, configuration, and secrets are not sent in search queries.
- With your authorization, existing client tools may connect to your named trusted MCP server and its documented authentication provider, discover tools, and make a documented read-only call with harmless approved input. The server receives the call arguments and ordinary connection metadata; authentication is completed locally or through the provider login. Provider charges may apply. Unknown effects and write-capable tools are excluded from smoke checks.
- Optional Inspector setup may download software from the npm registry and package download hosts, then execute Inspector and the reviewed target server. The server's executable origin, arguments, data access, effects, and documented service destinations must be reviewed and explained before launch; no fixed target server or downstream service is bundled. Use a user-selected trusted release. Inspector and the client may store credentials in a keychain or local files.
- Repair guidance can ask you to change local JSON/TOML configuration, set or export credentials locally without printing them, complete login, run `claude mcp list`, `claude mcp get`, `claude mcp remove <name> --scope local`, or `codex mcp list`, inspect `/mcp`, reconnect, refresh discovery, or invalidate an SDK tool cache. Removing a confirmed stale Claude entry changes local configuration; restarting or refreshing a client can launch configured servers and reconnect. Returned snippets and check instructions do not themselves edit files or prove a successful connection.

The skills do not authorize message delivery, purchases, account-data writes, or permission broadening as smoke checks. Pasted commands are not executed just because they appear in a configuration. You can supply redacted traces instead of using live access or installation. Source and support links identify references; relevant official sources may be retrieved in the requested documentation workflow, while the fictional `.example.test` endpoint is illustrative.

The publisher operates no collection, telemetry, or storage service for this plugin and receives no task data through it. Your assistant provider processes and may retain your conversation and attachments under its own terms; optional tools and named services have their own storage and retention. See [PRIVACY.md](PRIVACY.md).

| Skill | Give it | You get |
|---|---|---|
| mcp-connect | client name, config and startup output | a supported diagnosis, minimal client-specific snippet and safe verification step |
| mcp-tool-check | discovery trace, schemas and call results | missing-tool or failed-call repair and a report of what the evidence proves |

Try “This config works in Claude Code but fails in Codex” or “The server connects, but the search tool is missing.” Attach the relevant file or paste the redacted section. Keep secrets out of the conversation. The verification report distinguishes reviewed configuration, discovery and the requested operation.

The skills include source-backed configuration scope, environment, transport, session, discovery, schema and SDK permission guidance. Both skills link a shared [dated official source register](references/sources.md). Use them to restore an existing integration. A callable interface redesign belongs to Tool Contracts; a working knowledge-search call with bad retrieval belongs to RAG Evaluation.

## Optional live checks

If your assistant already has a client connected to the server you name, you can request discovery and a documented read-only call. Live checks need your server's normal access and may involve provider charges. Otherwise the assistant gives a concrete check matched to your client and accepts its redacted output. The package provides instructions, not a connector or execution service.

Inspector is optional. The assistant can explain its current runtime requirements and review a trusted server command before launch. Downloading it can contact the npm registry and package download hosts and execute software. A supplied Inspector trace works without setup. Keep token-bearing browser URLs private; Inspector may retain authentication data in its keychain or local secrets file.

## Data and network

Default network fetches: none. The assistant reads only pasted text and files you supply for the task. If you request current documentation, it may retrieve relevant pages on code.claude.com, developers.openai.com, learn.chatgpt.com, modelcontextprotocol.io, openai.github.io, docs.langchain.com or anthropic.com and their official redirects. No trace or config is sent in a search query. Authorized live checks contact only your named server and its documented authentication provider. Optional installation contacts the npm registry and its package download hosts; the target server may contact its own documented services, which must be reviewed before launch. No telemetry or plugin-managed storage. Host conversation retention and optional client storage still apply. See [PRIVACY.md](PRIVACY.md).

## Support and license

[Report a problem](https://github.com/grayskripko/marketing-skills/issues). MIT; see [LICENSE](LICENSE).
