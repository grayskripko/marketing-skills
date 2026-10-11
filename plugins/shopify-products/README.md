Write and fix Shopify product titles, descriptions, tags, variants and SEO fields from supplier data, and prepare bulk product CSV files.

# Shopify Products

For store owners and catalog editors. Paste supplier notes, approved facts and an existing listing or product export. No account, keys, installs or paid API are needed for drafting. A Shopify store is needed only when you import the resulting file yourself.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable servers. Development notes and text-only evaluation records are also present in this working folder.

These skills use only task text, attachments, and local files you explicitly supply. They instruct the assistant to use its existing local code tool, when available, to parse CSV, count fields and write a requested local output file without overwriting the source export. The CSV skill also calls for a real CSV reader to check the exact final output; without local parsing it returns a draft requiring validation before import. No code or parser is bundled, and the skills do not instruct software installation. Execution and temporary files are managed by your assistant provider.

The skills prohibit fetching supplier pages or image URLs, account access, API calls and store changes. They do not direct web search, message delivery or automatic publication. Source and support URLs identify references, not retrieval instructions; supply the relevant content instead of expecting a link to be fetched. Supplied image URLs may be included as text in CSV output. If you later import that CSV yourself, Shopify may retrieve those images from the supplied hosts; this is a user-led store action, not a plugin request. The CSV skill explains user-led backup export, import preview, overwrite choices and a representative test before a batch (one product by default for a homogeneous batch). Those actions access your Shopify account and can change store records; the assistant does not perform them.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain your conversation, attachments and tool activity under its own terms. Any requested output file is created by the assistant's existing tools, not a bundled program.

| Job | Skill | Result |
| --- | --- | --- |
| Write product fields | shopify-product-copy | Titles, descriptions, tags and SEO fields with variant-specific facts |
| Fix existing listings | shopify-product-fix | Corrected fields and meaningful changes against supplier evidence |
| Prepare bulk CSV | shopify-product-csv | Product and variant rows mapped to a supplied template or the documented current header subset |

Examples: “Turn these supplier notes into Shopify product copy.” “Fix the care instructions against this supplier sheet.” “Make a draft product CSV from these SKU rows.”

Existing handles, SKU strings and option combinations stay tied to the right product. Missing details stay outside import files. New products default to draft and unpublished. Updates distinguish omitted columns from blank cells that could erase values. When a template or identity is missing, you get mapped draft fields and the minimum necessary questions (one by default for one blocker) instead of an unverified import file.

## CSV use

Export a current product backup and provide its headers before updates. Review the output and the Shopify import preview, then test one representative product before a homogeneous batch by default, or a small set covering distinct mappings and update behavior for a heterogeneous batch. Inspect the resulting records before scaling; a sample does not prove full-batch acceptance. Changing option values can recreate variant identifiers. The package prepares files and explains the import steps; it does not upload, publish, change stock or connect to your store. Local CSV validation does not prove Shopify acceptance. Multi-location inventory and variant metafields need other workflows.

## Data and network

Plugin-directed network requests: none. Local code-tool execution and requested file writes are permitted as described above. User-led Shopify imports are separate account actions and may retrieve supplied image URLs. There is no telemetry or separate storage service. Your assistant provider's conversation and file retention applies. Remove supplier contacts, customer details and secrets before sharing files. See [PRIVACY.md](PRIVACY.md).

## Support and license

https://github.com/grayskripko/marketing-skills/issues

MIT. See [LICENSE](LICENSE).
