# Official recovery knowledge

Every entry read 2026-10-11 UTC. Each URL opened successfully and returned readable documentation in the web reader. Match the user's installed version and saved graph/state before choosing syntax or asserting exact restart behavior. These are access dates.

| ID | Official URL | Deciding knowledge | Used in |
|---|---|---|---|
| L1 | https://docs.langchain.com/oss/python/langgraph/interrupts | Resume reruns the interrupted node; invoking a subgraph inside a node also replays the parent node. Inventory both boundaries. | All skills |
| L2 | https://docs.langchain.com/oss/python/langgraph/checkpointers | Thread-keyed snapshots include checkpoint identity and pending tasks. Successfully persisted sibling writes need not rerun after a failed super-step. | All skills |
| C1 | https://code.claude.com/docs/en/common-workflows | Continue selects the current directory's latest conversation; resume offers session selection. | State, plan |
| C2 | https://code.claude.com/docs/en/agent-sdk/sessions | Resume takes the session ID. Fork creates separate history but does not isolate files in the same directory. Cross-host session-store lookup uses original working-directory identity. | Plan |
| O1 | https://learn.chatgpt.com/docs/developer-commands?surface=cli | Codex resume accepts a session ID; last is directory-scoped unless all is enabled. | State, plan |
| O2 | https://openai.github.io/openai-agents-python/human_in_the_loop/ | Preserve RunState, apply the actual approval decision, resume the original top-level agent. Nested agent-tool approvals remain on the outer run. | Plan, check |
| M1 | https://modelcontextprotocol.io/specification/2025-11-25/basic/utilities/cancellation | Cancellation can race with completion or be ignored. Ordinary requests use notifications; task-augmented requests use tasks/cancel. | All skills |
| E1 | https://developers.openai.com/api/docs/guides/evaluation-best-practices | Tool choice, argument precision and functional correctness are distinct checks. | Check |
| E2 | https://platform.claude.com/docs/en/test-and-evaluate/develop-tests | Task-specific criteria account for ambiguous or nonexistent inputs. | Check |
| R1 | https://developers.openai.com/api/docs/guides/retrieval | File indexing can be asynchronous; removal is eventually consistent. | Check |
| R2 | https://www.anthropic.com/engineering/contextual-retrieval | Semantic retrieval can miss exact identifiers; isolated chunks can lose entity and time context. | State |

## Observed redirects

Codex https://developers.openai.com/codex/cli/reference/ redirected to O1. Claude https://platform.claude.com/docs/en/agent-sdk/sessions redirected to C2. OpenAI platform evaluation/retrieval routes redirected to E1/R1. Anthropic define-success redirected to E2. LangGraph durable-execution redirected to persistence; L2 was then opened for the detailed state fields. The final destinations above were also opened directly in the final URL check.

## Authored operational conventions

Receipt matching, completed/pending/uncertain labels, ledger columns, hold conditions, plan layout and Verified/Incomplete/Unresolved verdicts are authored operational conventions. They combine supplied evidence with documented behavior. Chat history is not treated as an execution checkpoint, and no exactly-once guarantee is inferred from retries.

Use the register to support the requested answer, rather than reproduce it as a report. For nested approval recovery, verify that the restored outer state retains the nested continuation before treating a separate specialist export as unnecessary. Keep Claude Code directory-selection behavior distinct from Agent SDK session lookup; do not infer SDK selection from a CLI session listing.
