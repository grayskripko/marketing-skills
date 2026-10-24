# Skill Checkup

Find why your skill does not activate or fails on a missing file, command or tool.
For skill authors and teams maintaining Claude Code, Codex or agent SDK workflows.
Paste a trace, configuration, SKILL.md, file inventory or upload the relevant package files. No account, API key or installation is required for this artifact review.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The Claude and Codex manifests describe the same package for their respective hosts; neither launches a connector.

The assistant reviews only text, traces, configurations, inventories and files you explicitly supply. It does not run commands or code, install software, search the web, fetch URLs or robots.txt, call APIs or MCP tools, send messages, publish content, write patches to files, or change account settings. Source and support URLs are references, not retrieval instructions; supply the relevant content rather than expecting a URL to be fetched. Proposed patches are returned as text.

The skills also recommend verification that you perform in your own host. The activation check may ask you to invoke a skill, make an ordinary request and inspect the session trace. The dependency check may ask for command help output, recommend corrected command syntax, suggest the OpenAI Agents SDK method `invalidate_tools_cache()` when changed definitions were cached, and ask you to verify a fresh tool list before a read-only lookup. These user-led checks can execute host commands or contact your configured MCP server and lookup service. Their destinations, request data and retention depend on your host and server configuration; the package supplies no endpoint or credentials and does not perform those checks. They are not covered by a blanket “no network” claim.

The publisher receives no task data through this plugin and operates no collection, telemetry or storage service for it. Your assistant provider processes and may retain your conversation and attachments under its own terms. If you independently open a support link or submit an issue, that is a separate action; avoid sharing secrets or private logs.

| Skill | What you supply | What you receive |
|---|---|---|
| skill-activation-check | Skill text, host, locations, settings and invocation trace | Loading or selection diagnosis, minimal proposed patch and host-specific verification |
| skill-dependency-check | Referenced files, command output, tool declaration and error trace | Dependency or call-contract diagnosis, minimal proposed patch and safe verification |

Ask “Why is this skill missing from my session?” or “This skill calls an old tool name; what should I repair?”

The skills use bundled notes from official documentation for checks for discovery, invocation policy, SDK loading and MCP error handling. Sources and retrieval dates are linked from each skill. Uploaded artifacts support a static diagnosis; actual installation and runtime behavior need verification in your host. Proposed patches are returned as text.

## Data and network

The artifact review uses supplied material and bundled references without assistant-directed execution or network access. User-led runtime verification is separate and may execute commands or contact configured services, as described above. Redact secrets before sharing logs. The assistant returns text rather than applying repairs.

## Package and support

Skills-only package with Claude Code and Codex manifests. Host-specific syntax is diagnosed separately rather than advertised as universally portable.
Support: https://github.com/grayskripko/marketing-skills/issues
License: MIT; see [LICENSE](LICENSE).
