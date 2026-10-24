# Shopify Inventory

Prepare my Shopify inventory CSV correction from a stock count and later movements.
For Shopify merchants correcting inventory quantities. Needs an inventory export, count or correction evidence, and their times; accepts pasted text, exports, legible screenshots, or screenshots described by you.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account.

These skills work only from task text, attachments, and local files that you explicitly supply. They do not instruct the assistant to run code, install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. URLs in this package identify sources or support pages; they are not connection endpoints or retrieval instructions. A supplied URL is treated as text: paste the relevant content instead.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

The assistant may read supplied files and create requested correction or retry CSV copies with its existing file tools. The user separately exports inventory, views history/reports, uploads a reviewed CSV, starts the import, and checks the outcome in their own Shopify account; those user actions connect to Shopify and imports change store inventory. These skills do not perform them. The bundled reference’s “Recheck before submission” note is publisher maintenance guidance, not a runtime retrieval step. Both platform manifest directories contain metadata, not executable servers.

No account access is needed to prepare a draft. Exporting and importing in Shopify needs your own store access and permission. No keys, paid APIs, installations, or connection are required. These skills prepare files and handoffs; you import in Shopify yourself.

- **Prepare stock correction:** reconcile the count with later stock movements and return reviewed rows with current-stock validation intact.
- **Repair stock import:** explain rejected rows and prepare a retry containing only unresolved corrections.

For a protected export, open Products > Inventory > Export and choose All states. Available-only exports lack the current/new comparison. An agent can walk you through these native steps. Paste relevant rows and times for the no-setup path; missing fields stay marked rather than guessed.

On-hand validation checks a quantity, not every order or stock state. A sale that is still committed may leave on hand unchanged. Reconciliation needs the count's meaning and subsequent stock movements, not simply the number of new orders.

At runtime no URLs are fetched and no network requests are required. Official knowledge is bundled in dated references. There is no telemetry or automatic store write. See [PRIVACY.md](PRIVACY.md).
