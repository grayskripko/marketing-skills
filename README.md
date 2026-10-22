# Claude plugins by Sergey Skripko

Free skills-only plugins in the Claude plugin directory. Each plugin lives in its own folder under `plugins/` with its own README, license and privacy note; install them from the Claude plugin directory.

## AI agents and skills

| Plugin | What it does |
|---|---|
| [Agent Debugging](https://github.com/grayskripko/marketing-skills/tree/pl-agent-debugging/plugins/agent-debugging) | Debug a failed AI agent run from traces, logs, configuration, transcripts and output files; find the supported fault and get a repair or reproducible escalation. |
| [Agent Design](https://github.com/grayskripko/marketing-skills/tree/pl-agent-design/plugins/agent-design) | Design an AI agent for one process: decide whether an agent is needed, then write its implementation specification. |
| [Agent Evaluation](https://github.com/grayskripko/marketing-skills/tree/pl-agent-evaluation/plugins/agent-evaluation) | Plan agent evaluation and verify agent output against supplied requirements, artifacts, action receipts and escalation records. |
| [Agent Guardrails](https://github.com/grayskripko/marketing-skills/tree/pl-agent-guardrails/plugins/agent-guardrails) | Define and check agent permissions, human approval and agent escalation for a real workflow. |
| [Agent Recovery](https://github.com/grayskripko/marketing-skills/tree/pl-agent-recovery/plugins/agent-recovery) | Plan recovery of an interrupted AI agent run from checkpoints and action receipts; identify what can resume and which effects need checking before retry. |
| [Instructions Cleanup](https://github.com/grayskripko/marketing-skills/tree/pl-instructions-cleanup/plugins/instructions-cleanup) | Fix conflicting CLAUDE.md and AGENTS.md instructions: map the active scopes, repair stale references and return a minimal patch that preserves approvals. |
| [MCP Debugging](https://github.com/grayskripko/marketing-skills/tree/pl-mcp-debugging/plugins/mcp-debugging) | Troubleshoot MCP connection, authentication and missing-tool errors in my actual client from pasted traces, logs, configs, transcripts or files. |
| [Plugin Packaging](https://github.com/grayskripko/marketing-skills/tree/pl-plugin-packaging/plugins/plugin-packaging) | Repair a skills-only Claude plugin that fails to install, load skills or find its resources. |
| [RAG Evaluation](https://github.com/grayskripko/marketing-skills/tree/pl-rag-evaluation/plugins/rag-evaluation) | Evaluate and debug wrong RAG answers, retrieval quality, missing documents and grounded citations from the question, source documents, retrieved passages and response. |
| [Tool Schemas](https://github.com/grayskripko/marketing-skills/tree/pl-tool-schemas/plugins/tool-schemas) | Fix AI agent tool contracts when connections work but tool choices, arguments or results fail. |

## Sales and marketing

| Plugin | What it does |
|---|---|
| [LinkedIn Warm Leads](https://github.com/grayskripko/marketing-skills/tree/main/plugins/linkedin-warm-leads) | Find warm LinkedIn leads in what you already have: potential clients in your post comments, replies to comments, DM follow-up plans, warm connections in your own export. Drafts only; never sends. Synthetic samples in [samples/linkedin-warm-leads](https://github.com/grayskripko/marketing-skills/tree/main/samples/linkedin-warm-leads). |

## Author

Sergey Skripko. I build AI agents and fix poorly working skills.

If a plugin or a skill of yours works wrongly for your task, write in [GitHub Discussions](https://github.com/grayskripko/marketing-skills/discussions) — I read every message. Bugs: [GitHub Issues](https://github.com/grayskripko/marketing-skills/issues).

## License and privacy

Each plugin folder has its own LICENSE (MIT) and PRIVACY.md. The plugins contain no code and store nothing.
