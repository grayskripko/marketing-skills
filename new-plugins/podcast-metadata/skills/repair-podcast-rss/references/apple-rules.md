# Apple metadata decision register

Read 2026-10-11. All seven source URLs loaded with substantive text in the web reader. Pages are undated living support documentation. This is the observed version on the read date, not a claim about future changes. Re-open before relying on these rules for a later submission, or when the user's case conflicts with this snapshot. Each section gives the source scope and a paraphrased supporting passage. Workflow choices such as a field change table, an internal identity ledger and explicit missing-field markers are this package's editorial practices, not Apple requirements.

## RSS technical requirements
https://podcasters.apple.com/support/823-podcast-requirements

Read 2026-10-11. Scope: RSS feeds submitted to Apple Podcasts. Supporting passage: RSS 2.0; public access; UTF-8 declaration and Apple/content namespaces; server HEAD and byte-range support; enclosure URL, length and type; duplicate enclosure URLs ignored; unique unchanging episode GUIDs; case-sensitive tags/categories; RFC 2822 dates; XML entities instead of HTML named entities. Artwork and at least one episode are required. Use UTF-8 for other characters.

## Episode creation and Connect fields
https://podcasters.apple.com/support/825-how-to-create-an-episode

Read 2026-10-11. Scope: episode creation routes. Supporting passage: RSS-created episodes cannot be updated through Connect; edit through the provider. RSS items need title and enclosure. A provider may support Apple subscriptions. In the Connect-created episode form, Name allows 150 characters and Description 10,000; Original Release Date changes sort order only; availability has separate date/time/time-zone settings. Episode numbers are mandatory for serial shows; decimals unsupported. Types: full, bonus, trailer. This passage does not specify RSS field limits; the separate RSS guide below does. No algorithm for counting emoji is specified.

## Metadata authority and refresh
https://podcasters.apple.com/support/832-podcast-metadata

Read 2026-10-11. Scope: metadata updates. Supporting passage: RSS changes go through provider/feed tags, and host dashboard labels may differ. Connect-created shows/episodes are edited in Connect. Apple documents updates within 24 hours. Last Refresh shows the feed refresh time; contact support after more than 24 hours without the change. This is a documented expectation, not a measured refresh for the user's feed.

## Episode order and special placement
https://podcasters.apple.com/support/3143-how-to-set-the-order-of-podcast-episodes

Read 2026-10-11. Scope: Apple Podcasts display and playback organization. Supporting passage: episodic default, newest first; serial sequential, latest season default except Complete Series, which shows first season; no-season serial shows group by year, newest year first. Bonus with season/unique number follows number order; same number follows matching full episode; season alone follows the season; no season follows everything. Tied episodic publish dates should differ. Numbers belong in fields, not titles. A season-based serial episode without season metadata is filed under Unknown Season and misses automatic downloads/Up Next.

## Validation error interpretation
https://podcasters.apple.com/support/829-validate-your-podcast

Read 2026-10-11. Scope: RSS technical validation in Connect. Supporting passage: parse/read failures can involve declaration, tags or casing; no-episode failures require checking enclosure fields and supported available assets. Connection, download, timeout and byte-range messages call for public hosting, HEAD and byte-range support. Missing-category errors can involve category support/casing or escaped ampersands. Channel needs description, language, explicit true/false and title. The source's enclosure example has an unclosed type quote; do not reproduce it. Correctly quote all attributes in generated XML.

## GUID continuity during changes
https://podcasters.apple.com/support/837-change-the-rss-feed-url

Read 2026-10-11. Scope: identity continuity during feed/media/metadata changes. Supporting passage: existing episode GUIDs must remain unchanged even when titles or enclosure URLs change. Changing them may duplicate episodes, misrepresent Analytics or affect show status. This skill preserves existing identifiers rather than rewriting them to a suggested new format. Feed redirect implementation is outside the two repair jobs.

## RSS-specific field limits and byte units
https://help.apple.com/itc/podcasts_connect/en.lproj/itcb54353390.html

Read 2026-10-11. Scope: Apple RSS channel/item tag values, independent of host acceptance or Connect form limits. Supporting passage: tag values default to 255 characters unless otherwise specified. Channel description allows 4000 bytes; item description allows 10,000 characters. Enclosure length is file size in bytes. RSS season and episode numbers are non-zero integers; episode numbers are mandatory for serial shows and optional for episodic shows. HTML within descriptions belongs in CDATA. Count UTF-8 bytes for channel descriptions, not characters; preserve source qualifiers when shortening. A host accepting a longer string does not establish compliance with Apple's RSS limits.

The parent https://help.apple.com/itc/podcasts_connect/ returned only a JavaScript-required shell. The exact English guide URL above loaded the complete tag table. Use the exact guide URL, not the parent shell, to verify field rules.
