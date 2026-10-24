# Plugin Packaging

Repair a skills-only Claude plugin that fails to install, load skills or find its resources.
For authors sharing an existing package with colleagues. Paste manifests, configs, traces, logs, transcripts, a file inventory or the relevant files. No account, API key or installation is needed to review supplied artifacts. Applying repairs needs authorized local files; collecting new host evidence needs an existing target host and its provider connection.

## What this package runs and connects to

This skills-only package contains Markdown instructions and reference text, JSON compatibility metadata for Claude Code and Codex, a license and a static SVG icon. It bundles no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing this package does not itself run a bundled program or connect an account.

Supplied-artifact review uses the text, attachments, transcripts and package files you provide, runs no commands and returns corrected text or patches in the conversation. Documentation and support URLs are references, not retrieval instructions; the skills do not fetch those URLs or search the web.

Requested local repair can read and write files inside the authorized package tree and run the existing Claude Code command `claude plugin validate ./<package-directory>`. Supplied-text repair may instead propose that command for you to run. Requested host checks can use the existing named host to inspect inventory and errors, invoke a harmless skill and read a bundled resource. Claude Code local loading uses `--plugin-dir <package-directory>` after inspecting the complete target package for executable components; packages with hooks or MCP companions are not loaded in this workflow. Checks proposed to you are distinguished from commands actually run. Other hosts require an available documented tool or supplied transcripts; an unavailable host yields a partial receipt.

Host checks can make model requests through the host's existing provider connection, sending prompts and file contents read for the check to that provider; the host may also write session logs. This optional mode is not an offline or no-execution workflow. The skills do not install dependencies, run executable hooks or MCP companions, connect new accounts, send messages, publish content, or change account settings. Remote MCP URLs, dependency-installation rules and API/cache methods discussed in the package are diagnostic knowledge, not permission to execute companions or call their APIs.

The publisher receives no task data through this package and operates no collection, telemetry or storage service for it. Your assistant and target-host providers process and may retain conversations, attachments and session data under their own terms and settings. Local repairs and host logs use existing assistant or host tools, not a bundled program. Opening a support link or posting an issue yourself is a separate action; avoid including secrets or private logs.

| Skill | Result |
|---|---|
| plugin-package-audit | Located manifest, path, resource and companion-dependency defects |
| plugin-package-repair | Corrected text or minimal authorized local file edits and validation |
| plugin-install-check | A host-specific receipt from supplied transcripts or requested harmless host checks |

Ask “It works locally but my colleague sees missing skills,” “Fix these broken references,” or “Does this log prove the plugin loaded?”

The audit distinguishes a complete package inventory from an uploaded subset. Repairs preserve skill behavior and package identity. The receipt separates successful installation, enabled state, discovery, invocation and resource access. A valid manifest alone cannot fill those stages.

For requested local repair, the assistant edits the authorized package and runs its available validator. For requested Claude Code checks, it can load the package locally with `--plugin-dir`, inspect discovery and invoke a harmless skill and, when relevant to the requested claim, capture its read of the affected bundled reference. Resource-free skills need no resource-read stage. It records the host version and package revision. Local development loading does not establish a colleague’s marketplace installation. Other hosts need an available documented tool or supplied transcript; an unavailable host produces a partial receipt with the missing evidence.

Network scope: supplied-artifact review fetches no URLs and calls no services. Host-rule summaries and official source links are bundled in [references](references/sources.md). Requested local repairs read and write authorized package files and run validation. Requested host checks use the existing host’s provider connection, which can receive prompts and read file contents and write session logs. Documentation URLs are not fetched during skill use. No accounts are connected, dependencies installed, executable hooks or MCP companions run, or settings changed by these skills. The package adds no telemetry or storage.

The package includes Claude Code and Codex compatibility manifests. Each target host’s loading evidence is assessed separately. Individual-skill behavior repair and organization rollout have separate owners.

Support: https://github.com/grayskripko/marketing-skills/issues
License: MIT; see [LICENSE](LICENSE).
