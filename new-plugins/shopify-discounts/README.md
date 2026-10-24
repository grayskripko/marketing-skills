# Shopify Discounts

Why won’t my codes and automatic discounts combine, and what will this cart actually pay?
For Shopify merchants and support teams. Give pasted discount settings, cart exports, checkout messages, or screenshots described in text. Analysis needs no account, API key, installation, or paid service.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The Claude and Codex manifests are platform metadata, not executable connectors.

These skills analyze discount settings, cart details, exports and checkout text that you explicitly supply, and read their bundled source notes. They do not instruct the assistant to run code or shell commands, install software, call store APIs, write files, send messages, publish content or change account settings. A support reply is returned as copy-ready text for you to send.

This is not a strictly offline workflow: when current documentation is needed, both skills permit the assistant's existing web tools to fetch public pages on `help.shopify.com` or `shopify.dev`, following redirects only within those domains. The six official source URLs in the bundled notes identify these documentation destinations, including the Discount Function API documentation; that link does not authorize an API call. No supplied cart or customer data is sent to those sites. Ordinary supplied-material analysis fetches nothing. GitHub source and support links are references, not runtime connection endpoints. Web-tool requests are handled by your assistant provider under its own terms.

The skills can guide you to inspect Shopify admin > Discounts, Orders and payment status, consult Shopify Support, or reproduce a cart and enter codes to compare visible discounts, shipping and tax/duties. You perform these account and checkout checks yourself and stop before payment. Proposed setting changes or replacement codes are guidance for the merchant; the assistant does not log in, access a store, change discounts or complete checkout.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider processes your conversation, attachments and tool activity and controls their retention under its own terms. Redact unnecessary customer information and never supply credentials or payment details.

| Skill | Input | Result |
|---|---|---|
| shopify-discount-diagnose | Codes, automatic discounts, settings and checkout message | Specific conflict, supported reason and the setting to inspect |
| shopify-cart-calculate | Item prices and quantities, all discount settings, shipping and tax | Eligible savings and a calculation showing the total or missing inputs |

Coverage includes automatic discounts alongside codes, customer and item eligibility, active dates and timezone, usage limits, combination precedence and worked cart calculations.

Include the checkout surface (Online Store, Storefront API, POS Lite/Pro, draft invoice or external checkout) and whether any adjustment is manual. Start with the discount class, value, Combinations selections, products/variants, purchase type, customer eligibility, minimum, usage limits and active dates. Include the store plan for same-item product stacking. Describe screenshot fields exactly; cropped or missing fields stay unknown. Customer names, emails, addresses and order IDs can be redacted. A destination country or market may be needed; a full address is usually unnecessary.

The agent can walk you through Shopify admin > Discounts to copy settings. You can compare its result with checkout before payment. It provides guidance and calculations; it does not connect to your store or change discounts. App-defined logic needs its actual conditions or observed checkout values.

Example: an eligible automatic product discount reduces USD 100 of merchandise by USD 20. An eligible 10% order code, with both offers permitting the combination, then saves (100 − 20) × 10% = USD 8. Merchandise totals USD 72; adding USD 5 shipping gives USD 77 before tax. Check both offers’ dates, eligibility, minimums and usage limits before applying those savings.

Calculations distinguish merchandise subtotal, shipping, tax and payment credits. A pre-tax subtotal is never presented as the final charge when tax or duties are unknown.

Official rules were read 2026-10-11. Sources and qualifications are in each skill's references. Recheck changing rules before relying on them after that date.

MIT; see LICENSE. Support: https://github.com/grayskripko/marketing-skills/issues
