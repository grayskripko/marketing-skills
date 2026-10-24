# Airbnb Claims

Prepare an Airbnb damage-claim evidence packet and separate guest-request/support deadlines using checkout, damage dates, region and documented loss.
For home hosts and property managers. Needs pasted records or user-selected exports and attachments: checkout, damage and discovery dates, listing region, item costs, guest messages and payment history. Preparation needs no account, keys, installs or paid API.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The Claude and Codex manifests describe the same skills for their respective assistant hosts; neither is a connector.

Claim preparation uses task text, attachments, and selected local files that you explicitly supply. The skills do not instruct the assistant to run code, install software, call APIs, send messages, submit claims, or change account settings. They prepare drafts and recommend filing or contacting support yourself through Airbnb's Resolution Center.

There is an optional network workflow: only when you explicitly request a policy refresh, the assistant uses its existing retrieval tools to read official Airbnb policy URLs listed in the skill references or an official Airbnb policy URL you supply, plus the site's robots.txt. It respects robots restrictions and follows only redirects within airbnb.com. Listed sources include help articles 279, 2869, 3591, 1415 and 3344, the Japan insurance summary at /e/jhi-summary (historically redirected from /d/jhi-summary), and the historical terms PDF on assets.airbnb.com. It does not search the web, log in, retrieve reservation/account pages, or include guest records, claim details or identifiers in requests. If retrieval fails, paste the relevant official policy text. The Resolution Center URL is a user filing destination, not an allowed policy-fetch URL; publisher and support links identify reference pages, not plugin connection endpoints.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program; the skills themselves only require drafts and do not direct file writes.

| Skill | Request | Output |
|---|---|---|
| check-claim-deadlines | “How long do I have?” / “They only paid some; now what?” | Guest-request, response and support dates, with next action |
| prepare-damage-packet | “Put my damage claim together” / “Organize these receipts for support” | Itemized loss, evidence index, guest request and support draft |

Uses repair estimates, receipts and supplied photo records without inventing evidence. Separates ordinary checkout cleaning from qualifying extra cleaning, and supported amounts from unresolved amounts. Accounts for payments already received. Japan takes a separate route; Washington uses the insurer review route.

The official help article and terms currently give different support clocks. The skills display both and recommend acting by the earlier date. An unknown damage date remains unknown rather than becoming the discovery date.

## Inputs and use

Paste reservation dates and messages, or supply selected files. Use aliases for guests and listings. Original evidence stays intact; excerpts in the packet identify their source. If only a filename is supplied, the packet does not claim its content was inspected. To file the completed request, use your Airbnb account and its Resolution Center; this package prepares the text and attachment list.

## Data and network

Preparation reads only supplied material. Explicitly requested policy refreshes retrieve public Airbnb policy pages and robots.txt under the limits above. No account connector or claim submission is provided.

Sources and verification dates are in each skill's references/policy-sources.md. Build and test records are in BUILD-NOTES.md and tests/RESULT.md.

MIT. See [LICENSE](LICENSE). [Privacy](PRIVACY.md). [Support](https://github.com/grayskripko/marketing-skills/issues).
