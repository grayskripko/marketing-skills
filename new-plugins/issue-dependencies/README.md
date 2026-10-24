# Issue Dependencies

Audit a GitHub issue graph, distinguishing parent/sub-issue hierarchy from blocking dependencies and checking direction, counts and nesting limits.
For engineers and delivery reviewers using pasted text, CSV or JSON exports. Needs repository-qualified issue IDs, typed relationships, states and export coverage; no account, key or installation is required for analysis.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The Claude and Codex manifests describe the same skills for their respective hosts. This source folder also contains Markdown/JSON development evidence in `tests/`, `REVIEW.md`, and `BUILD-NOTES.md`; those are not executable components and should be excluded from the submitted runtime package.

During issue audits, these skills work only from task text, attachments, and local files that you explicitly supply. They prohibit network requests, connectors, and account changes. They do not instruct the assistant to run code, install software, send messages, publish content, or write files. Counts are presented as formulas and supplied inputs; relationship changes and API payloads are proposals only, not executed operations. Missing pages are requests for additional supplied evidence, not permission to fetch them.

There is one release-maintenance retrieval instruction: both bundled `references/github-rules.md` files say “Reopen these sources before submission if the snapshot changes.” This means opening the six public GitHub documentation URLs listed there: creating issue dependencies, adding sub-issues, GraphQL Issues, REST sub-issues, REST issue dependencies, and GraphQL pagination, all on `docs.github.com`. It is not part of the supplied-data audit and does not authorize repository API calls or account access. Other source, publisher, repository, and support URLs identify references or support pages, not audit connection endpoints. For an audit, supply the relevant content rather than a URL alone.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

| Skill | Give it | Get |
|---|---|---|
| issue-graph-audit | Issues, parent links, blocker links and intended order | Separate hierarchy and blocker findings; a proposed relationship diff |
| issue-count-reconcile | Relationship rows, states, summary fields and pagination | Equations explaining count differences and missing coverage |

Try “Find reversed blockers and conflicting parents in these rows” or “Why does this summary say two blockers when I see three?”

Include export time, repository scope and whether every relationship page is present. Bare issue numbers need their repository. A missing private issue stays unresolved. Corrections are proposed in text.

See [PRIVACY.md](PRIVACY.md), [LICENSE](LICENSE) and [BUILD-NOTES.md](BUILD-NOTES.md). Support: https://github.com/grayskripko/marketing-skills/issues

Documentation and privacy are bundled in this package. Public document links will be added after these exact files are published and verified.
