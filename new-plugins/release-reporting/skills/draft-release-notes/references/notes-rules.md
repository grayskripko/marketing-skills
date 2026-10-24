# Drafting source register

Sources loaded and read 2026-10-11. Dates record actual observation, not a claimed source publication date. Refresh changing GitHub pages before planned 2026-10-19 submission.

## Changelog convention

https://keepachangelog.com/en/1.1.0/

The requested 1.1.0 URL remains live. Its maintained example includes 1.1.2 dated 2024-09-27; do not describe the page as frozen in 2019 or mistake the example's latest entry for a new format URL.

Sections distinguish new features (Added), behavior changes (Changed), pending removals (Deprecated), completed removals (Removed), defects (Fixed), and vulnerabilities (Security). The convention favors newest versions first, visible release dates in YYYY-MM-DD, grouped change types, an Unreleased section, and prominent breaking/deprecation/removal information. Empty sections are noise. Preserve withdrawn versions with `[YANKED]` rather than silently dropping their history. These are changelog conventions, not GitHub release schema requirements.

## Native generation and config

https://docs.github.com/en/repositories/releasing-projects-on-github/automatically-generated-release-notes

Global exclusions and category-local exclusions have different scope. Category `title` and `labels` are required; a wildcard catches PRs unmatched by earlier categories. Generated notes contain merged PRs, contributors and a comparison link, but the supplied evidence decides which claims can be used in a draft. The docs do not decide the user's editorial scope or all multiple-category ties.

https://docs.github.com/en/rest/releases/releases#generate-release-notes-content-for-a-release

An existing tag ignores `target_commitish`. `previous_tag_name` selects the range start. Config override and `.github/release.yml` / `.github/release.yaml` fallback affect reproduction. A 200 name/body response is generated content, not saved release evidence.

https://docs.github.com/en/rest/commits/commits#compare-two-commits

An unpaged compare export can truncate at 250 commits; changed files cap at 300 and are shown only on the first page with pagination. Do not use these export caps as generator limits.

## Authored editorial choices

Reconcile first, draft first in the answer, request an editorial decision for an excluded noteworthy change, and avoid inferring benefits from labels are this plugin's rule of thumb. Supplied security embargoes and explicit omissions stay binding. These choices connect configuration evidence to supported prose; they are not automatic publishing behavior.
