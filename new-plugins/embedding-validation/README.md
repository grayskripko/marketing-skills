# Embedding Validation

Check embedding dimension mismatches, query/document prompts, input truncation and normalization from pasted settings, vectors and index schemas.
For AI and search builders checking an embedding representation before ingestion.
Needs pasted text or user-selected exports; no accounts, API keys or installs.

- **[Check embedding settings](skills/check-embedding-settings/SKILL.md):** model/revision, query and corpus operations, prompts/tasks, token limits and output settings.
- **[Check vector/index contract](skills/check-vector-index-contract/SKILL.md):** complete arrays, logical dimensions, datatype, model provenance, metric and normalization.

Paste the provider/model ID and revision, library version, query and document requests, effective encoder settings, complete sample arrays, and index field schema. Include tokenizer counts after prompts/special tokens and redacted error bodies when available. Partial evidence produces bounded findings and the precise missing detail.

Skills and reference text only. Network: none for ordinary audits. A requested documentation refresh reads relevant official documentation URLs in [the register](references/official-sources.md) or official URLs supplied by the user, plus robots.txt, with official-site redirects. The plugin makes no requests to embedding providers. The assistant provider processes the conversation. No telemetry. Local tools may calculate over supplied files. Privacy details: [PRIVACY.md](PRIVACY.md).

Technical references were verified on 2026-10-11. Request a documentation refresh when current provider rules are needed. This package returns findings and reviewable corrections from supplied evidence. Full RAG question-to-answer diagnosis belongs to RAG Evaluation.
