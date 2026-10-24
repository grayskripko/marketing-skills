# Eval Cases

Turn failed agent sessions and support reports into reusable cases with source evidence and clear expected outcomes.
For small agent teams and support engineers preparing cases for an existing evaluation runner.
Needs pasted traces, conversations, configs or selected files, plus supplied requirements; schema-specific exports also need the runner's schema or accepted example. Case preparation needs no additional accounts, paid APIs or package dependencies beyond the assistant host.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, a license, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. BUILD-NOTES.md records development and release evidence; it is not a runtime instruction or executable.

These skills use only task text, attachments, and local files that you explicitly supply. The export skill instructs your assistant to use an available local parser on the actual final JSON, JSONL, or CSV bytes and an available local schema validator for a supplied schema. This can execute local parsing or validation through the assistant's existing tools; no parser or validator is bundled, and the skill forbids dependency installation and remote schema resolution. If a validator is unavailable, the export identifies the exact unverified check. The skills save exports, review collections, and provenance sidecars only when requested, at your chosen local paths; otherwise they return pasteable content.

The skills do not instruct web search, URL or robots.txt retrieval, API calls, account access, message delivery, uploads, publishing, trace collection, agent replay, or evaluation-runner execution. Public source, repository, documentation, privacy, and support URLs are references, not runtime connection endpoints or retrieval instructions. A supplied URL is treated as text; supply the relevant content instead.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider processes and may retain your conversation, attachments, and tool data under its own terms. Local parsing, validation, and any requested output files are handled by your assistant's existing tools, not by a bundled program. Requested exports remain at your selected paths until you remove them.

| Skill | Input | Deliverable |
|---|---|---|
| build-eval-cases | Incident reports, Claude Code/Codex/MCP event exports, SDK traces and relevant configs | Redacted fixtures, provenance, observable expectations and unresolved questions |
| export-eval-cases | Prepared cases and a supplied target contract | Parseable export, a review collection for unresolved cases, and a provenance sidecar when needed |

Try: “Turn these failed sessions into cases with expected outcomes.” Or: “Export these prepared cases using this importer schema.”

Event interpretation accounts for incomplete calls, partial output, protocol errors, requests for further input and omitted sensitive trace data. Expectations come from supplied requirements or approved review decisions. Similar incidents with different conditions stay separate.

This package prepares text and local files. It does not replay an agent, execute a runner, collect traces or upload cases. Neutral JSONL is the no-setup fallback when the target contract is missing; it does not establish runner compatibility. Claude Code and Codex can use supplied local files; a chat assistant can work from pasted or attached exports.

## Data and network
The plugin directs no runtime network requests. Local parsing, schema validation, and requested file writes use the assistant's existing tools as described above. Saved source references supply public format knowledge without sending incident content to their publishers. See [PRIVACY.md](PRIVACY.md).

## Submission status
Prepared as a local skills-only package. Packaging and instruction checks do not establish installed-host routing, runner import, publication or directory acceptance. See [BUILD-NOTES.md](BUILD-NOTES.md) for evidence and remaining release work.
