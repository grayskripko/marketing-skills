# Zendesk export knowledge register

Verified by live page retrieval; read 2026-10-11. Scope: Zendesk Support account exports and supplied API export responses. Exact article edit dates were not exposed by the retrieved pages; do not replace verification dates with inferred edit dates. Recheck these URLs before the planned 2026-10-21 submission.

## Account exports
https://support.zendesk.com/hc/en-us/articles/4408886165402-Exporting-ticket-user-or-organization-data-from-your-account

Read 2026-10-11; page loaded. Admin Center JSON/CSV selection uses system timestamps and excludes the latest six minutes. JSON is NDJSON; tickets above 1 MB lose comments and have an error companion. CSV omits deleted tickets, descriptions, comments, multiline, multiselect and custom date fields; oversized tickets are absent. CSV timestamps use the account timezone, JSON UTC, Explore user timezone. XML ceiling: 500 MB; unavailable above 200,000 tickets. XML omits custom fields; ticket XML also omits metric sets and comment metadata. User XML excludes tickets. JSON/CSV unavailable in sandboxes; Team plans lack these tools. Owner requests enablement; authorized admins export. AI agent tickets unavailable. Above one million tickets JSON downloads use 31-day increments. File suffixes do not order records.

## NDJSON error meaning
https://support.zendesk.com/hc/en-us/articles/4951317624346-Why-is-my-full-JSON-export-not-valid-JSON

Read 2026-10-11; page loaded. Each line is its own valid JSON object; a whole-file single-document parser can reject a correct export. Array conversion uses brackets and commas between whole objects. Large files can overwhelm editors. Apply local parsing to private content.

## Incremental API exports
https://developer.zendesk.com/documentation/api-basics/working-with-data/using-the-incremental-export-api/

Read 2026-10-11; canonical page loaded directly during the fix verification. API exclusion is one minute, not six. Follow cursor or returned end_time through end_of_stream; counts do not establish completion. Time-based ticket deduplication uses id + updated_at. System-only changes use generated_timestamp. Direct customers retain incremental access; third-party integrations have restrictions. Deleted content is scrubbed after 30 days or immediately on manual permanent deletion. A minimal record remains for 90 days after permanent deletion, then leaves exports. Request prior retained exports when the desired content has already been scrubbed; a present deleted ID cannot recover the original conversation.

## Ticket comment evidence
https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_comments/

Read 2026-10-11; page loaded. GET /api/v2/tickets/{ticket_id}/comments returns up to 100 comments per page; cursor or offset pagination is supported. Attachment content_url and voice recording_url can point outside Zendesk. Metadata is not file bytes. Request supplied pages and attachment files rather than following these URLs or forwarding credentials. Count endpoint is approximate and can be cached; it cannot replace all comment pages.

## Review conventions
Manifest columns and present / absent by format / missing evidence / not requested labels are this package's rule of thumb. Unknown denominators remain unknown. Parsing and archive observations are limited to the actual supplied files. Field definitions and record values are separate evidence. These conventions do not claim a Zendesk feature.
