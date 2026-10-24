# Release Reporting

Explain missing PRs in GitHub release notes and check the notes against release.yml. Draft supported notes from supplied PRs, labels, authors and tags.
For engineers and release owners reviewing what belongs in a release.
Needs pasted notes or selected exports with confirmed release scope; include generation configuration when diagnosing native notes. No accounts, keys or installs are needed for the pasted-data workflow.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account.

These skills work only from task text, attachments, and local files that you explicitly supply. They do not instruct the assistant to run code, install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. URLs in this package identify sources or support pages; they are not connection endpoints or retrieval instructions. A supplied URL is treated as text: paste the relevant content instead.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

The analysis workflow is offline. One bundled reference (`skills/reconcile-release-notes/references/github-rules.md`, “Resource-not-found ambiguity”) advises you to check request details and access through your normal GitHub workflow. If you follow that advice, your browser or GitHub client connects to GitHub under its normal account and data policies; the assistant does not perform that check or request credentials. Reference-register reminders to refresh documentation before submission are publisher maintenance instructions, not runtime retrieval steps.

## Skills

- **reconcile-release-notes**: explain missing or misplaced PRs and identify the smallest supported correction.
- **draft-release-notes**: draft Markdown notes from the reconciled changes, using your headings or Keep a Changelog sections.

For a combined request, diagnose coverage first, then return the requested notes first in the answer. Generation rules and editorial choices stay distinct: a globally excluded PR can still contain a noteworthy breaking change that you explicitly want in curated notes.

## What to provide

For a draft, provide confirmed release scope and PR titles/descriptions; add links and author logins if you want credits. An explicitly confirmed first release needs no previous tag. For omission diagnosis, also provide the generated body, selected previous tag and target, labels, merge/range evidence, and `.github/release.yml`, `.github/release.yaml`, or the custom configuration used. A partial export is useful; unresolved coverage stays visible.

Ask “Why is #42 missing?” with its labels and the configuration, or “Draft notes for this tag range” with the PR summaries. A generation request/response or compare export can help explain range and coverage issues. Redact tokens, email addresses and private operational details before sharing exports.

## Knowledge included

The skills include configuration field requirements, exclusion scope, catch-all behavior, tag and target rules, generation response meanings, export limits and changelog section meanings. Dated official sources are linked in each skill's references. Source verification was performed on 2026-10-11.

## Data and network

Runtime network fetches: none. The skills read pasted material and only files you select. They include source links for reference and do not retrieve repository data, call GitHub APIs, create tags or publish releases. The package contains instructions, reference text and an SVG icon; it runs no service and collects no telemetry. See [PRIVACY.md](PRIVACY.md).
