# Greenhouse attribution evidence

All pages loaded successfully; read 2026-10-11. Support pages show publisher update 2026-03-02; API docs show no publication date. Scope: Greenhouse Recruiting, pasted evidence analysis.

| Source | URL | Supporting section / decision |
|---|---|---|
| Tracking a candidate’s source | https://support.greenhouse.io/hc/en-us/articles/216902526-Tracking-a-candidate-s-source | Tracking links; integration options; missing-source troubleshooting. Token transport differs for hosted, embedded and API forms. |
| Tracking links overview | https://support.greenhouse.io/hc/en-us/articles/216904366-Tracking-links-overview | Manage your custom sources: create the source before creating its link. |
| Job Board API | https://docs.greenhouse.io/job-board.html#submit-an-application | Request Parameters: optional `mapped_url_token` carries `gh_src`; example form populates its hidden field from the URL. Original https://developers.greenhouse.io/job-board.html redirects here. |
| Add custom source | https://support.greenhouse.io/hc/en-us/articles/200721664-Add-custom-source | Custom source creation requires a sourcing strategy. Permissions: Site Admin or Job Admin who can manage company metadata. |

Additional verified source: [View or edit a candidate’s source](https://support.greenhouse.io/hc/en-us/articles/17286556639259-View-or-edit-a-candidate-s-source), read 2026-10-11; updated 2026-03-02 14:20. The Source & referrer field is under Application details → Source and responsibility.

## Analysis conventions

These are this package’s rules of thumb, not documented platform behavior: do not treat a token as proof of persisted attribution; use supplied mappings; preserve missing source values; separate application/person IDs; inspect repeated query keys as ambiguous; do not infer overwrite priority or cookie persistence. Documentation does not settle token expiry, precedence across visits, or historical source changes. Request relevant history only when it changes the requested result.

## Maintenance

Reopen sources before the planned 2026-10-20 submission and when Greenhouse field definitions change. Retrieval on 2026-10-11 establishes this build’s evidence date only.
