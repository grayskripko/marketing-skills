# Privacy — Video Summary Notes

This package contains instructions and reference text. It runs no service and ships no executable.

- Data read: your research question, supplied captions, video links and exports; public video metadata and caption text when public research is requested. Material can contain speaker names and personal details. Unnecessary private contact details are not repeated.
- Purpose: find relevant videos and answer or compare their transcript statements in your conversation.
- Recipients: your assistant provider; public search and video hosts for the requests below; PyPI during optional installation; an optional proxy provider only if you choose it. No additional model provider is required or called.
- Retention: the package maintains no storage or telemetry. Your assistant's conversation retention applies. User-authorized retrieval tools may save local transcripts or dependencies; the agent can help locate and remove those task files.
- Controls: use pasted text to avoid public requests, redact private details, decline installation and proxies, and use your assistant's conversation deletion controls. Never paste credentials, cookies or tokens.

## Network scope

Pasted-text work makes no requests. Public research sends topic queries to the assistant's search provider and fetches selected public YouTube watch pages, channel metadata needed for attribution, caption-track listings and caption text on YouTube/Google video hosts, plus relevant robots.txt. Only user-linked or search-selected videos are fetched. No arbitrary linked sites, comments, login, audio/video downloads, telemetry, paid transcript services or extra model APIs. Explicit setup work may fetch PyPI package metadata, distributions and required dependencies and the linked package or platform documentation. An optional user-selected proxy routes video requests through that provider. Direct page fetching respects robots.txt.

Questions: https://github.com/grayskripko/marketing-skills/issues
