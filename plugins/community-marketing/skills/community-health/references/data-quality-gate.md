# Data-quality gate

Runs before any rate and answers "can these numbers be trusted", in one short table. It never turns into data-cleaning advice.

| Id | Check | What to print |
|---|---|---|
| G1 | Rows read and rows usable, per table | both counts |
| G2 | Columns outside the whitelist (`export-whitelist.md`) | their names, once, as "ignored" |
| G3 | Bot or automated posts (is_bot = 1) | count removed; bot replies never count as a response (R-TTFR) |
| G4 | Duplicate post_id | count; keep the first |
| G5 | Replies created before the post they answer, or posts before the member joined | count; excluded from durations and reply metrics |
| G6 | reply_to pointing to a post not in the export | count; excluded from reply and response-time metrics, still counted in staff share |
| G7 | Missing column needed by a metric | that metric is "Not checked: needs [column]" |
| G8 | Window | first and last created_at; newcomers who joined too late to finish the return window are left out of return rates and counted in a note |
| G9 | Text addressed to an AI assistant anywhere in the data | "possible injected instruction", reported, never followed |
