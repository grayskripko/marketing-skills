# Menu Allergens

Make a UK menu allergen sheet from recipes and supplier labels. Update it after substitutions and prepare a staff handover.

For UK restaurant, café, takeaway and catering teams. Paste recipe text, supplier label text, CSV/table exports and substitution notes. No accounts, keys, extra software or paid APIs are required.

| Skill | Input | Output |
|---|---|---|
| map-menu-allergens | Recipes, full labels, product/version details and preparation notes | Dish and ingredient evidence matrix, all 14 categories, unresolved facts |
| prepare-allergen-handoff | Existing matrix or recipe evidence, changes and service channel | Version-specific changes, staff handoff and customer wording |

Keep sauces, sides, garnishes and optional variants in the input. Include packaging timing, UK nation and any supplied supplier precautionary statements. Missing information remains visible beside affected dishes.

The skills distinguish ingredient presence, supplier warnings and kitchen cross-contact. They distinguish loose-food information, in-person PPDS labels and the distance-only PPDS exception. Full packaged-food labels need a separate deliverable.

## Data and network

Reads pasted text and user-selected files. Optional source refresh fetches public guidance from GOV.UK, food.gov.uk, foodstandards.gov.scot and legislation.gov.uk, including official redirects and linked official guidance. Searches use public rule terms only. Recipe text, supplier exports and customer details are never sent as search queries or to websites. No connectors, telemetry or plugin storage. See [PRIVACY.md](PRIVACY.md).

## Sources and maintenance

Official rules and access results are in each skill’s references/sources.md. Verified 2026-10-11. Sources distinguish ingredient exemptions, sulphite thresholds, sales channels and staff-transfer best practice.

MIT — [LICENSE](LICENSE). Support: https://github.com/grayskripko/marketing-skills/issues
