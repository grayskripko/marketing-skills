# Optional pasted evidence

Evaluate or debug a wrong RAG answer using the artifacts already available.
Preserve exact values and redact secrets. Leave unavailable fields marked unknown. No particular logging system is required. Use only the fields needed for the requested conclusion; this is an optional intake format, not an answer template or a requirement to collect every field.

```text
Question and incident time:
Expected source: document ID, version/effective date, tenant, section/page
Deciding source text:
Ingestion: completion/error, indexed version, extracted text and chunk IDs
Search: original/rewritten query, store/corpus, filters, top-k, score threshold
Candidates: rank, document ID, chunk ID, score convention, passage
Reranked results:
Actual passages delivered to generation:
Tool call ID and full result/error:
Response and citation map:
Config/framework/client version:
Changed field and supplied follow-up output, if any:
```

OpenAI Responses: export file-search passages with `include=["file_search_call.results"]` on the next request. Preserve the actual request alongside results. File annotations alone do not contain the full search evidence.

MCP: include `content`, `structuredContent`, `isError` and any tool `outputSchema`. SDK: include complete messages/results with matching call IDs rather than only partial stream fragments. Existing redacted exports are useful; omit credentials and unrelated private content.
