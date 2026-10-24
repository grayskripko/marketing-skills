# Shopify Shipping

Explain this unexpected checkout shipping charge from my settings and this cart.
For Shopify merchants and staff reviewing shipping profiles or shipping options by market. Needs the cart, destination region and relevant shipping settings. For charge explanations, include the observed amount. For a missing option, describe the checkout result. Paste text, provide exports, attach screenshots or describe what they show. No API keys, Shopify app installation or account connection are required.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The .claude-plugin and .codex-plugin directories contain platform metadata, not executable servers.

The two skills analyze task text, attachments, screenshots and local files that you explicitly supply, plus bundled references. They do not direct code execution, software installation, API calls, message delivery, publishing or account changes. Reading a bundled reference means reading local text, not fetching its source links. Missing carrier or app quotes must be supplied by you; the assistant does not request them from a carrier or app. Neither skill directs writing output files; any file you separately request is created by your assistant's existing file tools.

There are two external paths to distinguish from supplied-material analysis. If you separately request current documentation, your assistant may use its existing browsing tool to retrieve public pages at help.shopify.com; the bundled registers also call for a publisher documentation recheck before submission. Those requests disclose the requested public URL and ordinary connection metadata to Shopify and the browsing-tool provider; do not include cart or customer details in requests. The settings-check skill recommends that you inspect your Shopify settings and run a new storefront checkout with the same cart, destination, discounts and methods, stopping before payment. You perform that check and supply the observed rates; it contacts your store's checkout and can involve configured carrier/app rate services. The assistant does not log in, operate checkout, change settings, place orders or buy labels. If updated documentation or checkout evidence is unavailable, paste the relevant text or result and leave the affected conclusion conditional.

The publisher operates no collection, telemetry, or storage service for this plugin and receives no task data through it. Your assistant provider processes and may retain your conversation and attachments under its own terms. GitHub source, documentation and support links identify package information; they are not runtime connection instructions.

| Skill | Request | Result |
|---|---|---|
| explain-shipping-charge | Why is checkout charging this amount? | A rate-by-rate explanation, calculation and the remaining evidence needed |
| check-shipping-settings | Will these settings cover this cart, or why is an option missing? | Specific settings defects and a checkout verification checklist |

Include currency, quantities, discounts, item weights, package weight, product/profile assignments, stock by location, location groups, rate names/types/conditions and selected shipment methods where relevant. Redact customer names, full addresses, order identifiers and credentials. A destination country and province/state usually suffice for manual rates; use a redacted quote for carrier questions.

The instructions distinguish existing profiles from stores upgraded to shipping options by market. They explain additions across profiles, the same-group flat-rate exception, highest matching flat/order amount rates within a market option, mixed methods, and missing-rate conditions. Supplied settings alone cannot prove which carrier response checkout received.

For settings collection, the assistant can walk you through Settings > Shipping and delivery. On upgraded stores, shipping options are managed under Markets > the relevant market > Shipping. You retain account control. The assistant does not connect a Shopify account, change settings, place orders or buy labels.

## Sources and support

Official Shopify Help Center sources were opened on 2026-10-11. Each skill links its dated source register. Shipping options by market are in early access; verify your store's actual system before applying that branch. Sources and their read dates are in the bundled registers.

Support: https://github.com/grayskripko/marketing-skills/issues

MIT. See [LICENSE](LICENSE).
