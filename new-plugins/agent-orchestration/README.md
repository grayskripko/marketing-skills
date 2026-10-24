# Agent Orchestration

Plan and coordinate native agent tasks across hosts with real subagent tools, verify results, and review usage costs. Bundled Claude Code and Claude Messages API references cover worktree inputs, interrupted results, and streaming usage without counting cache categories twice.
For people using an AI assistant on large research or coding tasks.
Needs pasted text, redacted exports, or authorized local files. To run agents, your assistant must already have subagent tools. Working from supplied text needs no extra account, key, install, or paid API.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. The `.claude-plugin` and `.codex-plugin` folders are platform metadata, not runtimes. Installing the package does not launch agents or connect an account. Development notes and historical test captures currently remain in this folder; they are not runtime components.

These workflows are not all offline or execution-free. `plan-agent-work` returns a plan without launching agents. `run-agent-work` directs your assistant's existing native spawn, wait, status, resume, and scoped cancellation controls for authorized tasks. `check-agent-results` and `audit-agent-cost` can use authorized native agents for independent checks. Delegation passes the worker brief and relevant task inputs to your existing assistant provider, can add usage charges, and may create retained agent transcripts.

For authorized coding work, execution instructions can create isolated worktrees or copies, write result files and input patches, copy approved untracked files, inspect hashes and file modes, run tests, and remove only owned temporary resources through scoped host controls. The bundled Claude Code procedure directs local version/help checks and Git commands: `git rev-parse`, `git status`, `git diff --binary HEAD`, `git switch --detach`, and `git apply --check` / `git apply`. The cost audit also directs deterministic code for counts and export-structure checks. These operations use the assistant's existing tools; no program or agent framework is bundled or installed by the package.

The supplied-text/local-file workflows do not direct web search, URL or robots.txt retrieval, direct Claude Messages API requests, billing-account access, or a separate service connection. Claude Messages API references explain supplied usage events, not calls to that API. Source and support URLs are references; a supplied URL is treated as text, so paste the relevant content. Native agent requests use the host/provider connection. Any task-specific live network check, send, publication, deployment, or account action requires separate relevant authorization and tools; delegation does not grant it. Separately requested setup uses local or user-supplied help, a local version check and a real read-only trial; fetching setup documentation is outside these workflows and needs a separate request. Sign-in happens in the provider's interface.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider processes and may retain conversations, attachments, delegated inputs, transcripts, usage logs, and tool artifacts under its own terms. Local outputs and worktrees are created by the host's existing tools and remain until scoped cleanup.

## Choose the job

| Skill | Give it | You get |
|---|---|---|
| plan-agent-work | the task, inputs, constraints, deadline and budget | advice on using one assistant or several agents, plus worker briefs; no agents launched |
| run-agent-work | an authorized task or plan and available native agents | work by real agents, checked outputs and a combined result |
| check-agent-results | original inputs, agent outputs and merged result | corrected result or a verdict supported by the sources |
| audit-agent-cost | redacted usage export and applicable rates | usage with double counting removed, charge calculation and cost changes supported by the records |

## Reusable coordination patterns

Apply these patterns with your host’s actual native agent controls. Confirm available spawn, wait, status, resume, cancellation, isolation, and usage capabilities before choosing a pattern; map each action to a real supported tool. The package supplies reusable instructions; execution and state storage belong to the host.

- **Dependencies:** Give each task an identifier, owned output, required inputs, predecessor identifiers, acceptance checks, and budget. Launch independent ready tasks together within the concurrency cap. Release a dependent task only after its predecessor’s artifact passes source checks. If a predecessor fails, keep its dependents blocked and continue only independent work. For a cycle or shared writable output, revise the split or execute serially.
- **Handoffs:** Pass the objective, completed artifact location, source revision or input hashes where relevant, verification evidence, unresolved questions, permitted next action, and remaining budget. Require the receiving worker to confirm the artifact and required inputs before writing. The coordinator retains the task ledger and resolves conflicting claims from original sources.
- **Recovery:** Record native task identifiers, owned artifacts, last verified checkpoint, and whether any external effects occurred. Resume an existing task only when the host supports resumption and its state is verified. Otherwise create a replacement from the preserved checkpoint with a fresh identifier and the same ownership and authorization boundaries. Before retrying a write, check for its existing effect to avoid repeating it. Preserve partial work, keep uncertain results provisional, and stop at the agreed retry or spending limit. Cancel only tasks owned by this run through the host’s supported controls.

For example, two workers extract terms from separate supplied documents. A comparison task depends on both verified extracts; its handoff includes the original passages and acceptance checks. If one worker is interrupted, preserve its partial extract and recover it within the remaining budget. Release the comparison only when both inputs are verified; otherwise return the usable extract and identify the blocked comparison.

## Examples

- “Should I use subagents to compare these three exports? Only compare support terms. Plan it; do not launch.”
- “Run these two independent local research tasks with native agents, then check and combine their findings.”
- “Two agents disagree about this total. Check both answers against the pasted rows.”
- “Why was this run expensive? Here are redacted message usage rows and the rates.”

Use independent checks when another assessment could change an important decision. More agents are not automatically faster, cheaper, or more correct. Resolve disagreements from the sources. Each worker is responsible for a separate output. Check changes again after combining them. Calculate spending from your rates and usage record definitions; do not guess fixed prices.

## Setup and no-setup paths

With native subagent tools already available, the assistant can prepare a small read-only trial, inspect the actual result, and then execute the authorized plan within your budget. This package supplies instructions, not an agent runtime. It does not turn a chat-only assistant into a parallel execution system.

If subagent tools are unavailable, paste the task and inputs or provide redacted exports. The assistant can plan, inspect results, audit costs, or do the work alone. Work by one assistant does not count as an independent agent check.

If you separately request setup, the assistant can identify your host and version. It can explain the available subagent settings using official help already on your machine or supplied by you. It can then verify a read-only task. Fetching setup documentation requires a separate request outside these workflows. Sign in only through the provider's interface. Do not paste keys or passwords. A separate framework, paid API account, or broader permission is not required by this package. Host access or subscription charges may still apply. Set a budget before additional paid runs.

## Data and network

Supplied-text and local-file review does not fetch web pages or call a separate service. Authorized native agent execution uses your assistant provider's connection and shares relevant inputs with worker contexts. Coding and export checks can execute local commands and create artifacts as described above. The publisher operates no telemetry or storage service; host retention policies apply.

Live network checks or external writes need separate task authorization and tools. Source and support links are references, not retrieval instructions. Paste relevant URL content for the supplied-text path.

## Supported reference knowledge

Bundled official documentation, observed 2026-10-11, supplies Claude Code revision preparation and launch/resume/partial recovery, plus Claude Messages API usage fields and streaming assembly. These references resolve those host-specific questions from local material. Confirm the installed version before execution; other hosts need their own semantics. Rates remain supplied by the user.

## Limits

Your host determines how many agents can run, what conversation they inherit, which models they use, how caching works, and how usage is recorded. A task count or time budget is not a guaranteed bill. Missing rates prevent a verified monetary estimate. Missing original inputs or real test results can prevent approval. The assistant keeps usable work and identifies the missing detail that decides the outcome.

## Support and license

MIT, Sergey Skripko 2026. See [LICENSE](LICENSE) and [PRIVACY.md](PRIVACY.md).
Support: https://github.com/grayskripko/marketing-skills/issues

Read the bundled README and PRIVACY files.
