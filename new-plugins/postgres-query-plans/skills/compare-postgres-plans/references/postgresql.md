# PostgreSQL source register

Read 2026-10-11. Each URL loaded in the web reader and identified PostgreSQL 18 as current. These are access dates, not publication dates. Check the server's major version and refresh current before submission around 2026-10-13. Rules below are paraphrases; comparison practices are authored recommendations, not official performance promises.

## Using EXPLAIN

https://www.postgresql.org/docs/current/using-explain.html

Sections 14.1.1–14.1.3: cost units differ from time. Rows are output estimates. Actual rows/time average across loops; totals require multiplication. Parent timings include children, and early termination matters. Rows Removed by Filter are rounded per-loop averages. Section 14.1.3 documents that BitmapAnd/BitmapOr actual row counts always show zero due to implementation limitations; those counters cannot establish empty output or a cardinality-estimate error. External sorts and hash batches describe spill work. Index Searches totals all executions. Shared reads can be served by OS cache; counters are accesses rather than distinct blocks. This prevents treating every sequential scan as an index problem or adding node totals into elapsed time.

## EXPLAIN options

https://www.postgresql.org/docs/current/sql-explain.html

ANALYZE executes statements and side effects. BUFFERS includes descendants and is automatic with ANALYZE in version 18. TIMING OFF keeps statement runtime. SETTINGS exposes nondefault planning settings. GENERIC_PLAN excludes ANALYZE. SERIALIZE requires ANALYZE, measures conversion rather than network transfer; ordinary EXPLAIN omits result serialization. The documented rollback pattern for writes does not establish safety for every external effect.

## Planner statistics

https://www.postgresql.org/docs/current/planner-stats.html

ANALYZE samples; estimates remain approximate. CREATE STATISTICS registers interest; ANALYZE collects values. Dependencies improve constant equalities and constant IN predicates, not range/LIKE or column-to-column comparisons. Multivariate ndistinct targets grouped distinct estimates; MCV captures common combinations. Raising statistics targets adds collection/storage cost. Do not prescribe dependencies to repair arbitrary join estimates.

## Resource consumption

https://www.postgresql.org/docs/current/runtime-config-resource.html

work_mem defaults to 4MB per operation, not per query. Concurrent operations and sessions multiply usage. Hash budget = work_mem × hash_mem_multiplier, whose version-18 default is 2.0. Parallel query workers can increase total allocation. temp_file_limit is per process, excludes explicit temporary tables, defaults to -1 (unlimited), and cancels a transaction exceeding the limit. A spill does not justify raising global memory without workload evidence.

## Multicolumn indexes

https://www.postgresql.org/docs/current/indexes-multicolumn.html

B-tree leading equalities and the first non-equality column's inequality bound the scan range. Later predicates can save heap visits without bounding the entire range. Version 18 skip scan may make later predicates useful when preceding columns have few distinct values. Indexes allow up to 32 total key/INCLUDE columns in a default build; compile-time customization can change that limit. Do not infer index applicability from column order alone.

## Index-only scans

https://www.postgresql.org/docs/current/indexes-index-only-scans.html

An eligible index must store requested data and support index-only access. Visibility-map all-visible bits avoid heap checks; recently changed pages can still require heap access. INCLUDE columns provide payload but enlarge indexes and can exceed tuple-size limits. Index-only naming is not proof of zero heap fetches.

## Prepared statements

https://www.postgresql.org/docs/current/sql-prepare.html

For a statement with parameters under auto plan_cache_mode, five custom executions precede a generic-versus-average-custom-cost decision. A statement without parameters always uses a generic plan. A generic EXPLAIN EXECUTE plan contains parameter symbols; a custom plan substitutes values. DDL/statistics changes can cause replanning. A one-off literal test can miss the application's parameter-sensitive behavior; compare the same execution path.

## Parallel plans

https://www.postgresql.org/docs/current/parallel-plans.html

Partial parallel plans divide work across cooperating participants. The leader can participate; workers can receive unequal work. Gather combines their outputs. EXPLAIN ANALYZE VERBOSE exposes per-worker statistics for assessing skew. Workers Planned is intention, not evidence that those workers launched or that more workers would help. Accumulated participant work can exceed query wall time.

## Parallel worker launch and leader participation

https://www.postgresql.org/docs/current/how-parallel-query-works.html

Read 2026-10-11; page identifies PostgreSQL 18. Gather requests the planned workers, but availability and worker limits can leave fewer or none launched. The leader also executes the parallel portion, while reading worker output can occupy most of its time. Compare launched workers and participant details rather than assuming planned workers all ran.

## Covering-index retention costs

https://www.postgresql.org/docs/18/sql-createindex.html
https://www.postgresql.org/docs/18/storage-hot.html

Read 2026-10-11. INCLUDE payload increases index size and disables B-tree deduplication. Updating included columns can prevent otherwise eligible HOT updates; HOT also depends on page space and other indexes. For a retention decision, measure representative update latency/WAL and HOT-update rate alongside repeatable application-path read benefits. Hold the index fixed when comparing prepared-plan modes, then hold the mode fixed when comparing indexes, so planning improvements are not attributed to INCLUDE.
