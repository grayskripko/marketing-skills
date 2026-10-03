# URL rules sheet

Print this sheet as an editable list. Each line shows its source id (see `sources.md`) or the label "convention of this plugin". When a current URL breaks a line, list it with the line number.

| # | Rule | Why | Source |
|---|---|---|---|
| U-01 | Lowercase paths only | Servers and crawlers treat `/Pricing` and `/pricing` as two URLs; if the server answers both the same way, pick one case | G-url |
| U-02 | Hyphens between words, not underscores or run-together words | Hyphens let people and crawlers see word breaks | G-url |
| U-03 | Readable words, not internal ids, where the CMS allows | People can tell what the page is from its URL | G-url |
| U-04 | Parameters only for state that does not change what the page is about, written `key=value` and joined with `&` | Keeps one content page at one URL | G-url, G-facet |
| U-05 | No fragments (`#...`) to load different content | Google Search generally ignores fragments, so content behind one is not a separate page | G-url |
| U-06 | Words in the path are written for readers | Google says they have hardly any ranking effect beyond breadcrumbs | G-start |
| U-07 | A page's folder is its parent section in the tree | Consistency between URL, breadcrumb and upward link; Google's own reason for folders is learning how often sections change | convention of this plugin, supported by G-start |
| U-08 | No dates in evergreen paths (`/blog/2023/05/slug` → `/blog/slug`) | Avoids a URL change each time a post is refreshed; a maintenance cost, not a ranking claim | convention of this plugin |
| U-09 | One trailing-slash policy, and the other form redirects to it | One URL per page | convention of this plugin |
| U-10 | One URL pattern per page type (all features under one folder) | Predictable URLs; SA-03 checks it | convention of this plugin |
| U-11 | Paths no longer than they need to be: drop folder levels that add no meaning | Shorter URLs are easier to read and share | convention of this plugin |
| U-12 | Session ids and tracking parameters never in internal links | They create many URLs for one page | G-url |
