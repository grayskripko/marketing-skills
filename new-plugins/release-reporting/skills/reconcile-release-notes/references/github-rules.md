# GitHub source register

All URLs loaded and read 2026-10-11. Scope: GitHub.com native generated release notes, not Release Drafter. These are current documentation observations; re-read changing pages before 2026-10-19 submission. The docs do not expose a last-updated date, so the read date records verification rather than publication.

## Configuration

https://docs.github.com/en/repositories/releasing-projects-on-github/automatically-generated-release-notes

Required category fields are `title` and `labels`. Global exclusion lists apply to the generated body; category exclusions affect only that category. Author values are user/bot logins. The wildcard fills unmatched earlier categories. The example reserves dependency PRs by excluding that label from an initial wildcard category. This supports category-local exclusion, not a blanket exclusion. Repository collaborators and writers can customize notes. The page allows an explicit previous tag but does not define the automatic prior-tag algorithm or every overlap tie.

## Generation fields and response

https://docs.github.com/en/rest/releases/releases#generate-release-notes-content-for-a-release

`tag_name` is required. `target_commitish` is needed for a new tag and ignored for an existing tag. `previous_tag_name` sets the start. `configuration_file_path` overrides config lookup; fallback paths are `.github/release.yml` and `.github/release.yaml`, then default settings. The endpoint returns 200 name/body or documented 404 resource-not-found; generated content is not saved. Fine-grained authentication requires Contents write. The example currently uses API version 2026-03-10. This skill reads exported requests and does not execute them.

## Resource-not-found ambiguity

https://docs.github.com/en/rest/using-the-rest-api/troubleshooting-the-rest-api#404-not-found-for-an-existing-resource

Private resources can return 404 when authentication is inadequate. Wrong URL or HTTP method can also produce 404. An exported response alone does not establish a deleted repository. Check redacted request details and access locally through the user's normal GitHub workflow; never request a token in chat.

## Compare export limits

https://docs.github.com/en/rest/commits/commits#compare-two-commits

Unpaged comparisons stop at 250 commits. Paged results are chronological, use up to 100 entries per page, and show the file list only on page one, up to 300 files for the whole comparison. A page's last commit need not be the comparison's last. These limits govern this endpoint's evidence, not the release-note generator.

## PR export fields

https://docs.github.com/en/rest/pulls/pulls#list-pull-requests

List state defaults to open and can be open, closed or all. Page size defaults to 30 and maxes at 100. `closed` is not a merged-only filter; use merge evidence. The get-PR documentation distinguishes pre-merge test `merge_commit_sha` from post-merge values depending on merge method. A SHA field alone is not sufficient merged evidence.

## Authored workflow choices

The per-PR table, minimal proposed correction, and request for matching generation snapshots are this plugin's rule of thumb. They are evidence-handling choices, not GitHub schema guarantees. Quote `"*"` because YAML uses a bare asterisk for aliases; see YAML 1.2.2 section 7.1: https://yaml.org/spec/1.2.2/#71-alias-nodes (read 2026-10-11).
