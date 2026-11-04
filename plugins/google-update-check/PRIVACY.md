# Privacy policy: Google Algorithm Update & Traffic Drop Check

Effective date: 2026-11-04.

Google Algorithm Update & Traffic Drop Check is a set of instructions and reference documents for an AI assistant, plus the address of one read-only data server. It contains no code that runs on your computer. The server is https://black-vector.com/mcp/search-updates, run by the plugin author; it holds public Google Search event dates and nothing about you.

## What is sent, and when

- **Only when a skill needs Google's dates.** The assistant calls one of the server's three tools: `updates_in_range`, `search_status_now` or `list_updates`.
- **Only dates and an update kind.** Each call carries the tool name and its inputs: dates and, optionally, an update kind such as «core». The skills tell the assistant never to send your site address, URLs, numbers or text. `search_status_now` takes no input at all.
- The connection is made by your assistant app (from your computer in Claude Code, from the assistant provider's servers on claude.ai), under that provider's privacy terms. As with any connection, the app also sends its own technical details, such as its name and version.
- Data you paste into the chat (for example a Search Console export) stays in your conversation with the assistant; the skills do not send it to the server.
- No skill runs web searches or calls any other service on its own. The server needs no account or sign-in.

## What the server keeps

- The server is run by the plugin author on a rented server (Hetzner), with no CDN or proxy service in front of it. Like any web server, it receives the IP address of the connection in order to answer.
- For this address, the web server (nginx) keeps neither an access log nor an error log: both are turned off for `/mcp/search-updates`, on https and on plain http (which only redirects to https). The service itself writes no request log.
- For each tool call, the service writes one counter line with the UTC date and the tool name, for example `2026-11-04 agent-updates_in_range`. It is used to count how often each tool is used.
- The service does not store IP addresses, the dates or kind you asked about, the app's name or version, or anything you type.
- One exception, common to every nginx server: if a connection fails before nginx has read which address it asks for (for example a broken TLS handshake), nginx can write a line with the connecting IP address to the server's general error log. Such a line does not show the address asked for or any request content; that log is kept for about two weeks, then deleted.
- No cookies, no scripts, no account.

Apart from that exception, nothing that identifies you is retained.

## Where the data comes from

The server's data comes from Google's public pages: the Google Search Status Dashboard (status.search.google.com) and the «Data anomalies in Search Console» help page (support.google.com/webmasters/answer/6211453). A daily job reads them; no AI model is involved.

## Contact

Questions about this policy: open an issue at https://github.com/grayskripko/marketing-skills/issues

## Changes

If this policy changes, the new version will be published in this file with a new effective date.
