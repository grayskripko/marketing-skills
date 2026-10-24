# Official runtime sources

Opened 2026-10-11. These sources describe runtime behavior, not a guarantee for every installed version. Recheck the installed version's help and supplied traces before applying flags. Dates here are observation dates, not publication dates.

- Claude Code, [Run Claude Code programmatically](https://code.claude.com/docs/en/headless). JSON and streaming output sections distinguish text `result` from schema `structured_output`; startup metadata documents plugin and MCP load errors. Supports the Claude output/capture rules. Read 2026-10-11.
- OpenAI, [Non-interactive mode](https://developers.openai.com/codex/noninteractive), redirects to [ChatGPT Learn](https://learn.chatgpt.com/docs/non-interactive-mode). Machine-readable and structured-output sections document JSONL events, `--output-schema` and final-message capture. Supports the Codex artifact distinction. Read 2026-10-11.
- MCP, [Tools specification, revision 2025-06-18](https://modelcontextprotocol.io/specification/2025-06-18/server/tools). Error Handling distinguishes protocol errors and `isError` tool results. Structured Content requires schema-conforming structured results when outputSchema is supplied. Apply to the negotiated protocol revision rather than assuming all servers use this revision. Read 2026-10-11.
- OpenAI, [Running agents](https://openai.github.io/openai-agents-python/running_agents/). Agent loop and Exceptions explain final completion and `MaxTurnsExceeded`. Supports incomplete-run classification; does not establish Claude or Codex turn semantics. Read 2026-10-11.

Authored operational conventions: user-owned acceptance contracts, separate artifact paths, evidence-first outcomes, no invented passes, and holding a release on missing required evidence. These are package design choices, not official vendor requirements.
