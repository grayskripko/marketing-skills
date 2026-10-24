# Ollama Capacity

Explain Ollama out-of-memory errors, CPU fallback and 503 overload from pasted hardware details, ollama ps, settings and logs; get a memory ledger and the smallest relevant settings proposal.
For AI and agent builders running local Ollama. Works from pasted text or exports; no Ollama connection, account or key is required.

| Skill | Your input | Result |
|---|---|---|
| ollama-memory-ledger | Hardware, loaded models, environment and timestamped logs | Per-memory-pool ledger, pressure signals and decisive missing evidence |
| ollama-config-proposal | The same evidence plus required context and concurrency | Bounded settings diff, staged verification and rollback |

Paste the Ollama version, OS and launch method if known. Include GPU capacity and usage per device, available host RAM, model identity, `ollama ps`, relevant server environment and log timestamps. API `/api/ps` exports are accepted. Remove tokens, usernames and unrelated prompt content. A partial paste still produces a partial ledger with specific unknowns.

The ledger separates capacity pressure from discovery failures, including ROCm driver timeouts and backend visibility. The proposal preserves workload requirements and separates queue overload, context allocation and GPU discovery problems. It does not connect to a server or apply settings. Proposed checks describe what to compare after a change; pasted results can be reviewed in a later message.

Network: none. The skills use bundled official reference summaries and supplied text or exports. They fetch no URLs, call no APIs and download no dependencies. No telemetry. The package runs no service and stores no input; the assistant handles conversation processing and retention.

Sources: dated official Ollama references accompany both skills. Defaults that disagree across pages are resolved through the supplied version and runtime evidence.

Support: https://github.com/grayskripko/marketing-skills/issues

MIT. See [LICENSE](LICENSE).
