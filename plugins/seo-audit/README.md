# SEO Audit Kit

## What it does

Audit a website, a single page, Search Console and crawler exports, or a site's source code for technical, on-page and content SEO issues. Every finding shows its evidence and how certain it is, and findings can be turned into a prioritized fix plan with developer tickets.

## Skills

Each skill is chosen by what you give it:

| You give | Skill |
|---|---|
| A domain, a site section or several URLs, or just "why isn't my site on Google?" | `seo-audit`: asks for the domain if needed, then a site audit with a ranked top 5 of changes |
| Exactly one URL or one page's HTML, optionally a target query | `seo-page-audit`: intent match, page checks, title and description options |
| An export: Search Console, crawler CSV, PageSpeed, server logs | `seo-data-review`: fixed thresholds, patterns with counts and examples |
| A local website project | `seo-code-audit`: problems reported as `file:line`, read-only |
| A list of findings | `seo-fix-plan`: tickets with acceptance criteria and verification steps |

## Examples

- "Review this Next.js project for SEO problems and list them as file:line."
- "Here are my Search Console queries and query-by-page exports. Find striking-distance queries, CTR outliers and cannibalization."
- "Run an SEO audit of https://example.com. B2B SaaS; the goal is more demo requests from organic search."
- "Audit https://example.com/pricing for the query 'invoice automation software'."
- "Turn these audit findings into developer tickets with acceptance criteria."

## How it works

The site audit asks only for what it is missing (usually the domain and one business goal), samples one page per template, and diagnoses before it recommends anything. Answers lead with what you asked for; checks and caveats follow. Every finding uses one format and carries an evidence level: **Observed** (seen in the page, HTML or code), **From user data** (read from your export), or **Needs verification** (with the tool that can confirm it, such as URL Inspection or the Rich Results Test). Assumptions are listed separately, never as findings. Export analysis applies fixed, written thresholds and shows the calculation, so results can be checked and repeated. Claims that Google documents as non-issues, such as meta keywords or word-count targets, are not reported as problems.

Sample finding:

| # | Where | Issue | Evidence | Evidence level | Impact |
|---|---|---|---|---|---|
| 1 | `/pricing` | Page carries noindex | `<meta name="robots" content="noindex">` in server HTML | Observed | High |

## Data and network

The plugin contains only instructions and reference text. It runs no code, calls no service of its own and stores nothing. If the assistant you use has a web tool, it fetches public pages on the site you name only: the URLs you give, that site's robots.txt and sitemaps, and other pages on the same site chosen from its sitemap or navigation, at most 10 HTML pages per run. A page audit fetches only that page, up to three competitor URLs you name, and each fetched site's robots.txt. Fetching always respects robots.txt and never logs in or submits forms. The export review may use the assistant's own code or spreadsheet tool, if it has one, to compute the thresholds on your file. Exports and source files you share stay in your conversation. The site audit and the export review do not repeat visitor IP addresses, emails or names found in your files; they use labels such as Visitor 1. The code audit reads project files, does not open files that hold secrets, and changes nothing unless you ask.

## Troubleshooting

- **No web tool available:** paste the page source ("view source"), robots.txt or the sitemap.
- **Page built with JavaScript:** checks that depend on rendering are marked Needs verification, with the tool to use.
- **Export not recognized:** say which tool and report produced it, or paste the header row.
- **Page cap reached:** name the sections or templates to cover next.
- **No file access for the code audit:** paste the files the skill asks for.

## Support

Report problems and requests through GitHub Issues: https://github.com/grayskripko/marketing-skills/issues

## License and privacy

MIT License, see [LICENSE](LICENSE). Privacy policy: [PRIVACY.md](PRIVACY.md).
