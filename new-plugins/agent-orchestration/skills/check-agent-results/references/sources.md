# Claude Code interrupted-run recovery

Official source: [Claude Code subagents](https://code.claude.com/docs/en/sub-agents), “Resume subagents” and “Frontmatter reference”; opened successfully 2026-10-11. Record the installed version and native status/transcript records. The documented partial marking for `maxTurns` requires v2.1.246 or later; absence of that marker on older versions proves nothing about completion.

Documented facts: a new invocation creates a new instance. Resumption retains earlier conversation history, including tool calls and results. Reaching `maxTurns` stops the subagent and returns partial output. These host facts do not certify artifact freshness or successful extraction.

## Recovery table — package evidence policy

| State | Coordinator records to inspect | Reuse / next action |
|---|---|---|
| Fresh launch | Actual new instance identity, brief, source versions, tool results and output paths | Supply required evidence explicitly. Prior notes are reusable only after provenance checks, not because the worker has the same name. |
| Resume | Resumed identity linked to the earlier run, earlier and current tool results, original brief, current source versions | Earlier notes may be in conversation without new file reads. Compare source hashes/versions; request a focused reread for changed or unproven passages. |
| Turn-limit partial | Limit, partial/status record, completed operations, missing requirements and artifact contents | Keep supported partial findings. Continue only within remaining allowance; do not raise the limit or approve the entire task merely because a file was returned. |
| Terminal failure / interrupted stream | Native failure/stop record, command exit status, stderr, last successful operation, actual artifact contents | A blank extraction after a failed command is failed evidence, not “no differences”. Repair the extraction or inspect the supplied originals directly. |
| Reported completion | Native terminal record plus required artifacts and deciding evidence | Completion status alone cannot settle disputed claims. Revalidate source versions and the combined conclusion. |

For every reused artifact, record run identity, invocation/resume relationship, source locator and version/hash, generating operation and exit status, output path/hash, and claims still unresolved. This is a suggested provenance record, not a host-provided schema or universal identifier.

For the interrupted policy-comparison request: inspect the failed extraction's exit status and the blank artifact; compare resumed notes' source versions with the supplied originals; decide the disputed passage from those originals. Correct supported statements and withhold approval of unresolved claims. Resume history can explain where a note came from; it cannot prove a current reread or recreate a missing artifact.
