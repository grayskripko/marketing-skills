# Webflow source register

Verified/read 2026-10-11. All four official pages loaded. Dates below are displayed publisher revisions, not freshness guarantees for a future release. Reopen before submission around 2026-10-15. No API connection is implemented.

## Import and export

https://help.webflow.com/hc/en-us/articles/33961211526291-Import-export-301-redirects

Displayed revision: 2024-10-01 15:50. Read 2026-10-11. Scope: CSV in Site settings → Publishing → 301 redirects. Deciding claims: full replacement; two mapped columns; 16MB maximum; invalid redirects cause failure with correction guidance downloadable from email/Dashboard; publication activates changes. Exact header spelling, MB units and import ordering guarantees are absent.

## Path matching

https://help.webflow.com/hc/en-us/articles/33961294898835-How-do-I-set-up-redirects-in-Webflow

Displayed revision: 2026-05-19 22:02. Read 2026-10-11. Scope: Webflow redirect pattern syntax and execution. Deciding claims: literal percent escaping; capture targets; query slash handling; creation-order priority (inspect Date created, not the default Last modified sort); localized paths and occupied slugs; paid-plan prerequisite; recommended total rather than hard limit. Preserve deliberate capture syntax and do not generalize ordinary regex semantics. The listed literal escapes are `% - & * ( ) = _ + ?`; the page does not establish `%.` matching behavior. Keeping unknown exported sequences unchanged while withholding semantic equivalence is an authored preparation convention.

## Publishing destinations

https://help.webflow.com/hc/en-us/articles/33961351954579-How-do-I-publish-or-unpublish-a-Webflow-site

Displayed revision: 2026-08-04 00:22. Read 2026-10-11. Publish modal lets users select staging and custom domains separately. Custom-domain ownership must be verified. Site publishing permissions depend on plan and role. Do not imply a successful upload means redirects are active, or that publishing changes only redirects.

## API boundary

https://developers.webflow.com/data/reference/enterprise/site-configuration/301-redirects/get

No publisher revision shown. Read 2026-10-11. GET redirects requires Enterprise Workspace and sites:read; returned data uses redirects with fromUrl/toUrl and pagination. Never offer this as a universal export fallback or request credentials. The supported fallback here is user-provided UI export.

## Preparation conventions, not platform requirements

Graph checks, conservative byte ceiling, UTF-8, deduplication of additions, backup retention and approval of semantic changes are authored preparation conventions. No undocumented error codes, guaranteed rollback, required header spelling, CSV ordering contract or universal regex engine is asserted.
