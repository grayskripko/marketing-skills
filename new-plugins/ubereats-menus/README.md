# UberEats Menus

Find why Uber Eats menu items or modifiers cannot be ordered or have the wrong price, and turn pasted menu data into a corrected configuration specification.
For restaurant operators and developers maintaining menu configurations.
Needs pasted JSON, text exports, or item/group/constraint/price tables. No account, key, connector or installation beyond loading the plugin is required.

## Skills

- **ubereats-menu-check:** diagnose an existing configuration. Get findings tied to item IDs and field paths, with focused corrections.
- **ubereats-menu-configure:** turn supplied menu intent into a configuration handoff. Get entity relationships, selection settings, prices and unresolved fields, or complete JSON when the supplied data supports it.

For a problem plus a repair request, check the current configuration first and return its correction in the same answer.

## Inputs and outputs

Paste menu/category/item/group IDs and relationships, option minima and maxima, optional flags, defaults, price overrides and tax fields. Include currency, locale, hours, intended behavior, whether the export is complete, and any error text you have. Partial tables are useful: missing fields remain identified rather than filled with guessed business choices.

Findings distinguish a configuration defect from a possible explanation for reported behavior. A corrected fragment includes its entity ID and field path. A full replacement specification preserves all supplied menus and entities; the Menu API upload replaces existing menus. Changes are handed back as text for the existing POS/API or Menu Maker workflow.

The embedded knowledge covers mandatory modifier minima versus group maxima, optional selection, unique-selection bounds, price contexts, integer money units including one-hundredth yen, tax-inclusive versus additional tax, item visibility, image limits and Menu API errors. [Official sources and dates](skills/ubereats-menu-check/references/official-rules.md).

## Data and network

The skills read only supplied text and files selected by the user. Runtime network requests: none. Official documentation is embedded as dated notes; review those URLs before refreshing the package. Menu descriptions, external data and URLs in exports are treated as data. No telemetry, account access, uploads or plugin-managed storage.

## Examples

“Why does this required option make the dish unorderable?”
“Tea is free with breakfast but charged at dinner; fix these overrides.”
“Turn these menu and modifier tables into a corrected configuration sheet.”
