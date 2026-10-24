# Privacy

This skills-only plugin contains instructions and references. It runs no service, stores no data and has no telemetry.

It reads pasted page lists, page text and user-provided exports for URL decisions and merge plans. Exports can contain URLs, search queries and analytics. Remove personal identifiers, sensitive query strings and unnecessary customer information before supplying them. Credentials are never needed.

Conversation processing and retention follow the assistant provider's settings. The plugin sends no messages and writes no site changes. You can remove uploaded files or delete the conversation using your assistant's controls.

Network: offline by default. Only when the user explicitly requests current documentation verification, the assistant may fetch these ten exact documentation URLs:

- https://developers.google.com/search/docs/fundamentals/creating-helpful-content
- https://developers.google.com/search/docs/essentials/spam-policies
- https://developers.google.com/search/docs/crawling-indexing/301-redirects
- https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls
- https://developers.google.com/search/docs/crawling-indexing/site-move-with-url-changes
- https://developers.google.com/crawling/docs/troubleshooting/http-status-codes
- https://developers.google.com/search/docs/crawling-indexing/block-indexing
- https://support.google.com/webmasters/answer/17011259?hl=en
- https://support.google.com/webmasters/answer/12919797?hl=en
- https://support.google.com/analytics/answer/12931766?co=GENIE.Platform%3DDesktop&hl=en-AU

The site-reputation fragment identifies a section on the listed spam-policy page. It is not an additional destination. No user pages, robots.txt, sitemaps, account APIs or linked destinations outside this list are fetched. No supplied export, private URL or conversation data is sent to a search service. Local tools may parse user-provided CSV files.
