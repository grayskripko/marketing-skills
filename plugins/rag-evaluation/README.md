# RAG Evaluation

Evaluate and debug wrong RAG answers, retrieval quality, missing documents and grounded citations from your question, sources, retrieved passages and response.
For developers and knowledge-base owners investigating AI answers. Paste traces, logs, configs, transcripts or source files; no account, API key or installation is required for the pasted-evidence workflow.

The result follows one question from source availability through retrieval and passage delivery to a supported answer. It identifies the observed failing stage, prepares a concrete correction and checks the evidence from a supplied rerun.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The two plugin manifests provide Claude and Codex metadata, not connectors.

Analysis uses only task text, attachments, and relevant local files that you explicitly supply. The skills do not direct the assistant to run code, install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. Source and support URLs are references, not retrieval instructions; supply the relevant content instead. The assistant may read supplied local artifacts and, only when you explicitly request an edit and name the file, write that local configuration file using its existing file tools. Otherwise corrections are returned as text or diffs.

The skills can recommend that **you rerun your existing RAG pipeline** and paste its output. For OpenAI Responses file search, they recommend adding `include=["file_search_call.results"]` to your next request while retaining your existing store, filters, and result limit. That user-run request can call OpenAI's API and access your configured vector store; reruns on other stacks use your existing pipeline's services. The plugin does not execute those requests, connect to MCP servers, run SDKs or evaluators, mutate indexes, or deploy changes. Its MCP and SDK guidance interprets supplied logs and results.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation, attachments, and tool activity under its own terms. Any local edit or output file you explicitly request is handled by your assistant's existing file tools, not by a bundled program. User-run pipeline requests remain subject to the services and data handling you already configured.

| Skill | Ask it to do |
| --- | --- |
| `rag-retrieval-check` | Find why the right document or passage did not reach the answer. |
| `rag-answer-check` | Correct unsupported claims and citations against the actual evidence. |
| `rag-incident-repair` | Prepare a stage-specific fix and inspect the corrected run. |

Start with what you have. Source IDs and versions, metadata filters, ranked passages, tool call IDs and citation maps help distinguish the failure. [Evidence template](references/evidence-template.md) provides an optional paste format. Missing artifacts remain specific unanswered boundaries rather than invented results.

The skills embed current official checks for OpenAI file-search result exports, MCP execution errors and structured content, Codex tool filters, Claude Code file-backed results, SDK trace completeness and retrieval-versus-response evaluation. [Dated technical sources](references/official-sources.md) explain the fields and their scope.

See [PRIVACY.md](PRIVACY.md) for local file access, user-run requests, and provider retention.
