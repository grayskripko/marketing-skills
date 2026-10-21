# Plugin Packaging

Plugin troubleshooting for a skills-only Claude plugin that works locally but fails for colleagues: install failures, skills not loading, broken references, a `plugin.json` manifest or plugin dependencies that do not resolve.

Paste the manifest, a file inventory, configs, errors or an install transcript. No account or API key is needed to review what you supply. Local repairs need files you authorize the assistant to edit.

| Skill | Result |
|---|---|
| skills-not-loading-audit | The failing path or declaration and a small list of edits |
| plugin-manifest-repair | Corrected file text or a minimal patch, or authorized local edits followed by `claude plugin validate` |
| plugin-install-check | A receipt of what the supplied install evidence shows, stage by stage |

Ask “It works locally but my colleague sees missing skills,” “Fix these broken references,” or “Does this log prove the plugin loaded?”

## What this package runs and connects to

The package is Markdown instructions, a references file, Claude Code and Codex manifests, a license and a static SVG icon. It bundles no scripts, hooks, MCP or LSP servers, installers or background processes, and installing it runs nothing.

- Reviewing supplied files runs no commands and fetches no URLs. The source links in the skills and in [references](references/sources.md) are for you to open; the skills do not fetch them.
- Authorized local repair reads and writes files inside the package folder you name and runs `claude plugin validate ./<package-directory>`. Validation does not show that skills load or run.
- If you ask for a check to be run, the assistant uses only a harmless skill, does not load a package that has hooks, MCP servers or `bin/`, and lists the commands it actually ran. A local `--plugin-dir` load does not prove a colleague's marketplace install.
- The skills do not install dependencies, run hooks or MCP companions, connect accounts, send messages, publish, or change settings.

The publisher receives no task data and runs no collection, telemetry or storage service. Your assistant's provider processes conversations under its own terms. Leave secrets and private logs out of files you paste and out of public issues.

Support: https://github.com/grayskripko/marketing-skills/issues
License: MIT; see [LICENSE](LICENSE).
