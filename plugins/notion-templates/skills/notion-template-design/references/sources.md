# Source notes

Primary Notion documentation, read 2026-10-10. Runtime does not fetch these pages. These notes support platform behavior, not proof of account access or a completed import. Procedure choices, minimal schema design, acceptance checks and response shape are this package's rules of thumb. Consult only the platform details relevant to the requested deliverable; these notes do not prescribe answer sections or establish that an unnamed app is Notion. Parser or workspace validation requires actual execution evidence.

- [CSV import](https://www.notion.com/help/import-data-into-notion): new CSV creates pages/properties, not new formulas, rollups or relations. Existing relation mapping is available. Import/merge appends rows rather than updating them. Help specifies MM/DD/YYYY dates and UTF-8 for character recovery.
- [Formula syntax](https://www.notion.com/help/formula-syntax): property types govern expression types; relations are page lists. `empty(0)` is true. `if` chooses a branch; dateBetween takes two dates and a unit.
- [Relations and rollups](https://www.notion.com/help/relations-and-rollups): a relation connects database records; a rollup aggregates a property through a relation.
- [Database templates](https://www.notion.com/help/database-templates): create through New's dropdown; preset relation values are reused on new pages.
- [Views, filters and sorts](https://www.notion.com/help/views-filters-and-sorts): databases support distinct presentations and per-view filtering, sorting and grouping.

CSV quoting and round-trip parsing are file-format handling conventions. Retaining IDs as text, keeping a separate relation-key map and using a scratch import are this package's rules of thumb. Never infer permissions from a filter.
