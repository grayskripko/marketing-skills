# Navigation spec fields

Fill the fields the site needs; leave out the rest.

| Field | What to write | Source |
|---|---|---|
| Header items | Label → target URL, in display order, plus one primary action if the site has one | — |
| Dropdown or mega menu | For each header item: groups, labels, targets. A mega menu only when one item holds several distinct groups | NN-FD |
| Section navigation | Side or in-page menu inside large sections (docs, help, catalogue): which sections get one and what it lists | — |
| Footer groups | The utility and trust layer: about, contact, legal, security, careers, plus links to the main hubs under the same section names as the header (L-07) | convention of this plugin |
| Breadcrumb format | Home › parent › current page, built from the single parent chain in the page table: one path even where a page could live in two places, the first crumb links home, the current page is last and not a link; none for a site only one or two levels deep; breadcrumbs support the main menu and never replace it | NN-BC guidelines 1, 3, 4, 5, 7, 8 |
| Hub entry points | Which header item or section index links to each hub | convention of this plugin |
| Link markup | Every menu, breadcrumb and pagination link is an `<a href="...">` element, whether in the HTML or inserted by JavaScript; items with no `href`, such as onclick-only links, cannot be followed reliably | G-links |
| Mobile | Which header items collapse, and that the breadcrumb does not wrap onto several lines | NN-BC guideline 9 |

Two layers, kept apart:
- Topical layer: header items, hubs, section menus and body links. Every topical link follows the tree.
- Utility layer: about, contact, legal, account, careers. Sitewide in the header corner or footer; outside the topical tree (convention of this plugin).

Do not grade the header by its number of items. Judge whether each item is distinct, recognisable and leads to a page whose heading matches the label (L-01 to L-08).
