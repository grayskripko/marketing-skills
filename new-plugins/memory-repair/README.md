# Memory Repair

Repair stale or conflicting AI agent memory using original sources; correct saved facts and check that the existing store retrieves the updated information.
For people maintaining an agent's existing persistent memory. Paste memory files or exports and original sources, plus any traces, logs, configurations or transcripts showing the problem. No account, key or installation is needed for pasted-artifact work.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a bundled program or connect an account. The `.claude-plugin` and `.codex-plugin` folders contain platform metadata, not servers.

Pasted-artifact work analyzes the supplied material and returns an audit, replacement text, patch, or retrieval verdict without setup. The complete plugin is not an offline-only workflow: all three skills permit the assistant's existing web tool to fetch linked official documentation or user-supplied public URLs, following redirects. Those sites, redirect destinations, and the web-tool provider receive the requested URL and ordinary connection metadata; private memory, transcripts, and credentials must not be sent to documentation sites.

For authorized live work, the assistant uses relevant local files or the user's existing connector and its configured store endpoint. Audits may read entries; requested repairs read the current entry, write or delete the selected fact, and read it back. Retrieval checks use the application's normal search route, including bounded ingestion-status polling and repeated reads where needed. The store and connector provider receive the selected queries, entries, and changes. MCP schema inspection uses `tools/list`; no connector or backend is bundled or installed by these skills. Endpoint configuration guidance uses the service's official instructions and the host's credential interface.

Requested file corrections change the named files; patches, companion change notes, and ordinary rollback material may be created through the assistant's existing file tools. Requested forgetting avoids another copy of deleted sensitive content. Startup verification calls for a new Claude Code session or Codex run in the same environment, and application/store checks use the existing host and backend. These are host operations, not a bundled execution harness. The skills do not prescribe shell scripts, package installation, account creation, message delivery, or publication.

The publisher operates no collection, telemetry, or storage service for this plugin and receives no task data through it. Your assistant provider and any connected service process and retain material under their own terms. Development records (`BUILD-NOTES.md` and `REVIEW.md`) are present in this working folder; section 1 of the scanhold packaging guidance recommends keeping them outside the submitted package.

- **memory-facts-audit:** find stale, conflicting, expired or unattributed entries, with source and scope.
- **memory-facts-repair:** return an exact correction in the existing format, or apply a requested change through accessible files or an existing connection.
- **memory-retrieval-check:** distinguish stored contents, retrieved context and the answer after the correction.

Give the target host/store, tenant or namespace, current entry and authoritative correction when available. The result is an audit, an applicable patch or an evidence-backed retrieval verdict. A supplied export produces a prepared repair; an accessible authorized target supports application and readback.

For live store work, the agent can inspect your existing connector's tool schema and help configure the endpoint using that service's official instructions. Keep authentication in the host's credential interface. Pasted exports remain the no-setup path. Startup checks require a new run in the same environment; store checks use the application's normal retrieval route.

This package contains instructions and an icon. It adds no backend, hooks or telemetry. It reads only supplied text and relevant authorized files. Optional network requests fetch linked official documentation or user-supplied public URLs, following redirects; existing store operations contact the endpoint configured in the user's connection. Private memory is not sent to documentation sites.

[Current technical sources](references/current-knowledge.md) cover Claude Code, Codex, MCP, both Agent SDKs, LangGraph and public evaluation/retrieval guidance. [Privacy](PRIVACY.md).
