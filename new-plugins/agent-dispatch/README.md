# Agent Dispatch

Split agent work into clear owners, recover blocked jobs and reconcile the results.
For developers and technical leads coordinating coding or research agents.
Give it pasted task briefs, traces, configs, diffs or test output, or authorize access to specific local files. Pasted-input use needs no setup, accounts, keys or paid APIs beyond your existing assistant.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a bundled program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable runtimes.

Pasted-material planning, recovery and reconciliation use only the supplied records. This package also supports requested execution: through your assistant's existing native delegation tools, it may start workers, send them selected task material or inherited context, collect results, and resume or interrupt workers when authorized. With requested workspace access, it may inspect local files and Git checkout state, run local acceptance tests, and apply integration edits when requested. Requested output files use the assistant's existing file tools at your authorized destination. These are host tool operations, not a bundled launcher; this is not a strictly offline, no-execution plugin.

The skills prohibit web search, page or robots.txt retrieval, external connector/API calls, software installation, permission changes, shell-based substitute agents, publication and messages to people. Source, repository and support URLs are references, not retrieval instructions. The README's setup fallback asks you to install or enable a chosen host separately using its official instructions; the plugin does not perform that setup. Native delegation uses your host's existing model service, so delegated task material and permitted inherited history are processed by the host and its selected model providers and may consume your existing allowance. Local tests run in the authorized workspace under the same worker restrictions.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider controls conversation, attachment and worker-transcript retention; requested local artifacts remain in the authorized workspace. Check inherited-context sharing before delegation: redacting a brief alone does not redact the worker's inherited history.

| Skill | Give it | You get |
|---|---|---|
| dispatch-plan | Task, constraints, paths and available runtime | Dependencies, file owners and worker briefs |
| dispatch-recover | Worker status, wait relationships and pending operations | Revised assignments and safe unblock actions |
| dispatch-reconcile | Briefs, reports, diffs and check output | Integration decision and missing evidence |

Example requests:

- “Split this migration between workers. Only the coordinator can edit the schema.”
- “These workers are waiting for each other's field names. Reorganize the jobs from this trace.”
- “Combine these results. The UI worker tested against an older contract.”

The instructions include host-specific checks for Claude Code worktree bases, Claude SDK resume/trace evidence, Codex native controls, OpenAI SDK handoff history and MCP cancellation races. Public documentation and actual read dates are in [runtime sources](skills/dispatch-plan/references/runtime-sources.md).

Plans work from supplied material. Live dispatch is conditional: ask for execution in an assistant that exposes native delegation and grants access to the needed local workspace. The agent checks available tools and permissions, starts ready jobs, and collects actual results. It does not install an orchestration runtime or launch substitute agents through shell commands. If delegation is unavailable, you still get briefs and an integration order for sequential work. Planning alone does not enforce file locks or prove a worker ran.

If you want live work but delegation is unavailable, the agent can help identify the host and its supported setup from your pasted version/config. Install or enable your chosen host through its official instructions outside this package, then request a harmless read-only worker check before allowing edits. Do not paste credentials or widen permissions to get around a blocked launch. Native workers use your host's model service and may consume your existing allowance; no cost or speed outcome is promised.

Execution and connection scope is described above; worker briefs carry the same restrictions. See [PRIVACY.md](PRIVACY.md).

Local build evidence and pending release checks are in [BUILD-NOTES.md](BUILD-NOTES.md). This package's host-specific operational paths require verification in your installed host before relying on live execution.

Support: https://github.com/grayskripko/marketing-skills/issues

MIT. See [LICENSE](LICENSE).
