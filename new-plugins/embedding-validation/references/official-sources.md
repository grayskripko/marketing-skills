# Official source register

Verified by live reads on 2026-10-11. Dates below are read dates; publication/update dates are recorded only where displayed. Reopen changing model/SDK rules before the planned 2026-10-21 submission. Sources supply technical rules; sampling boundaries and output format are authored workflow decisions.

| Source and URL | Freshness and scope | Rules used |
|---|---|---|
| [SentenceTransformer API](https://www.sbert.net/docs/package_reference/sentence_transformer/model.html) | read 2026-10-11; loads, current public API, installed library version still controls | Explicit prompt takes precedence; document fallback order document/passage/corpus; query/document tasks can route modules. max_seq_length limits tokens, truncate_dim reduces vector dimensions, normalize_embeddings defaults false. |
| [SentenceTransformer modules](https://www.sbert.net/docs/package_reference/sentence_transformer/modules.html) | read 2026-10-11; canonical modules.html URL; loads, current module reference | Normalize module normalizes embeddings to unit length independently of the encode option; inspect complete output vectors after later transformations. |
| [Voyage embeddings API](https://docs.voyageai.com/reference/embeddings-api-1) | read 2026-10-11; loads, displays updated 11 months ago; lists 3-series models | input_type null/query/document; role prompts preserve compatibility. truncation defaults true; false rejects excess context. Binary arrays pack eight dimensions per integer. encoding_format base64 preserves dtype-specific NumPy representation. |
| [Gemini embeddings guide](https://ai.google.dev/gemini-api/docs/embeddings) | read 2026-10-11; loads, last updated 2026-10-09 | 001: 2048 tokens, task_type, manually normalize reduced output. 2: 8192 tokens, text task instructions, automatic reduced-output normalization. Both support 128–3072 dimensions, recommendations 768/1536/3072. Spaces incompatible, re-embed on change. Multiple parts can aggregate. |
| [Voyage current model guide](https://docs.voyageai.com/docs/embeddings) | read 2026-10-11; loads, includes 4 series omitted by API reference | General-purpose 4-series models share a space; code-4 is separately listed. voyage-3.5: 32000 per input, 320K total request tokens, up to 1000 inputs; output sizes 256/512/1024/2048, default 1024. Model tables differ; use exact row. |
| [Gemini API fields](https://ai.google.dev/api/embeddings) | read 2026-10-11; loads, last updated 2026-08-28 | embedContentConfig supersedes deprecated top-level taskType/title/outputDimensionality; title for RETRIEVAL_DOCUMENT. Model-specific guide decides task support, even though generic schema exposes taskType. autoTruncate permits silent over-length input truncation; no default is documented in this field schema. |
| [Voyage error codes](https://docs.voyageai.com/docs/error-codes) | read 2026-10-11; loads | 400 malformed request; 401 authentication; 403 forbidden client IP; 429 rate limit; 500/502/503/504 server/availability problems. Diagnose the supplied body before assigning a field cause. |
| [Qdrant collections](https://qdrant.tech/documentation/manage-data/collections/) | read 2026-10-11; official concepts URL redirects here; loads | Within a vector field size/metric must match; named vectors allow separate contracts. Cosine automatically normalizes uploaded vectors. |
| [Sentence Transformers Matryoshka](https://www.sbert.net/examples/sentence_transformer/training/matryoshka/README.html) | read 2026-10-11; loads | Training optimizes nested reduced vectors; truncation support is not a universal quality guarantee. Renormalize manually truncated vectors when unit norm is required. |
| [Sentence Transformers semantic search](https://www.sbert.net/examples/sentence_transformer/applications/semantic-search/README.html) | read 2026-10-11; loads | Retrieval distinguishes query/document paths; normalized embeddings allow dot-product scoring corresponding to cosine. |

## Conflicts and applicability

Voyage's API reference remains useful for field semantics but is behind the model guide's catalog. Do not treat its recommended-model list as exhaustive. Gemini generic REST fields remain broader than Embedding 2 task support; the current model guide explicitly says Embedding 2 cannot use task_type. Validate installed SDK field spelling against supplied version, rather than converting snake_case to camelCase mechanically.

## Authored calculation and evidence conventions

For dense floating-point arrays use Euclidean norm sqrt(sum(x_i²)). Cosine divides dot product by both nonzero norms. Keep rounding/tolerance explicit. A short sample or a rounded export cannot certify the remaining corpus or original precision. These are mathematical definitions and evidence boundaries, not provider limits.

## Fix-pass verification — read 2026-10-11

The fix pass independently reopened every documentation row above. The canonical modules.html destination replaces the redirecting models.html link. Gemini guide/API and Voyage guide/API continue to support the migration, reduced-normalization, task-field, model-limit and packed-representation decisions. The inline skill lookup tables make those sourced contracts visible before generic sample arithmetic. Provider-specific worked examples replace the arithmetic-only examples; these are teaching examples, not evaluation requests.
