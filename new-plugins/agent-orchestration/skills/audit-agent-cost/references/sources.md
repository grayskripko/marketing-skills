# Claude Messages usage and stream assembly

Official sources opened successfully 2026-10-11: [Prompt caching](https://platform.claude.com/docs/en/build-with-claude/prompt-caching), “Tracking cache performance” and “1-hour cache duration”; [Streaming messages](https://platform.claude.com/docs/en/build-with-claude/streaming), “Event types” and “Error events”. Supported schema: raw Claude Messages API responses/events, not arbitrary Claude Code transcripts or other providers.

## Documented field map

| Usage field | Meaning / billing treatment |
|---|---|
| `input_tokens` | Uncached input, separate from cache reads and writes. Never subtract reads from it. |
| `cache_read_input_tokens` | Input retrieved from cache. |
| `cache_creation_input_tokens` | Input written to cache. |
| `cache_creation.ephemeral_5m_input_tokens` / `ephemeral_1h_input_tokens` | Lifetime subdivisions whose sum equals cache creation, not additional input. |
| `output_tokens` | Output token usage; apply supplied output rate. |

Total input = uncached + cache reads + cache creation. When lifetime rates differ, bill the two lifetime subtotals instead of their parent. Missing lifetime breakdown with mixed rates leaves the write charge unresolved.

## Event-to-message procedure

Documented lifecycle: `message_start`, indexed content-block events, one or more `message_delta`, then `message_stop`. Delta usage counters are cumulative. Errors can arrive inside the stream.

Package assembly policy:

1. Preserve stream/request identity from the actual exporter and `message_start.message.id`. Later events need not repeat the ID: associate them through their stream container. Interleaved events with no stream association cannot be reliably reconstructed; request the exporter mapping rather than invent a deduplication key.
2. Initialize message metadata and usage from `message_start`. Accumulate content by block index separately from accounting. For each `message_delta`, replace only supplied usage counters with the latest cumulative values; retain omitted fields. Never sum snapshots or overwrite omitted input/cache fields with zero. Flag inconsistent decreasing counters for inspection rather than silently taking maxima.
3. `message_stop` closes the same message, adding no turn or token charge. Require a clean terminal event for complete-stream status. A disconnect, error or missing stop leaves observed usage provisional; preserve it and reconcile with a final response or billing record. Do not assume a failed request was free or its last observed count was final.
4. A complete stream is not necessarily a completed user task: retain `stop_reason`, and inspect whether the output meets the requirement. Keep retries as separate requests. Do not count an SDK final-message copy again when it represents these same events.
5. Keep coordinator roll-ups outside the API message ledger until their independent overlap semantics are established. Nested usage breakdowns likewise need their own semantics before summing with top-level totals. Unknown fields/events are retained for inspection, not assigned invented prices.

Apply supplied model/date/currency rates: charge = (I×rI + R×rR + W5×rW5 + W1×rW1 + O×rO) / rate unit + nonoverlapping fees. Use aggregate W only if its applicable rate is established. Never include W and W5+W1 together.

Arithmetic illustration with supplied fictional per-million rates: I=50, R=1000, W=200 (W5=150, W1=50), successive output counters 2, 7, 10; rates 2, 0.2, 2.5, 4, 8. Total input=50+1000+200=1250; final output=10; charge=(50×2+1000×0.2+150×2.5+50×4+10×8)/1000000=0.000955 currency units. Start/delta/stop and the creation subtotals do not add extra messages or tokens.
