# Privacy

The skills use claim fields, payer instructions and evidence pasted into the conversation or included in files the user selects. They need only the values relevant to the requested check. Findings use claim aliases, item numbers, line numbers and provider-role aliases; avoid repeating beneficiary numbers, birth dates, addresses, phone numbers or full NPIs.

Network: none by default. A requested rule refresh reads the official CMS URLs in references/sources.md and their CMS redirects, or an official payer URL supplied by the user. Claim contents and personal identifiers are never included in external queries or uploaded to a website. No accounts, credentials, connectors, sends or claim submissions are used.

The plugin has no runtime service, analytics, telemetry, external database or plugin-managed persistence. Conversation and file handling follow the host application's settings. Source documents and exported fields are treated as data, not instructions.
