Check vLLM KV-cache capacity and concurrency from startup logs, or get a minimal engine-argument diff.

For operators sizing vLLM inference replicas. Uses startup allocation lines, effective engine arguments and request lengths/concurrency; GPU inventory helps evaluate memory changes. No account, API key or installation is required.

## Skills

- **capacity-sheet**: return a fit decision and shortfall; reconcile KV allocation, scheduler validation and API admission scopes.
- **configuration-diff**: reconcile argument precedence and installed checks; preserve context and propose the smallest supported edit with restart criteria.

Paste the allocation/concurrency lines and effective arguments that decide your question. Include matching vLLM version, model/revision, topology and errors when their interpretation matters. Include prompt plus maximum generated tokens. Exports can be files you designate. Remove secrets and irrelevant personal data.

Network: none for pasted-text analysis. If you ask for version-specific verification, the agent may fetch official documentation at docs.vllm.ai and vllm-project/vllm source pages at github.com or raw.githubusercontent.com. Private inputs stay out of queries. No telemetry or external log uploads.

Knowledge was verified on 2026-10-11; each skill includes a dated official-source register. GPU inventory alone does not determine cache token capacity. The output is a constraint sheet or proposed diff, depending on the request; server execution is outside this workflow.
