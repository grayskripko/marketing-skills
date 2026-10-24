# GitHub issue-form source register

Verified live and read 2026-10-11. Scope: current GitHub Cloud documentation. Server installations need their version's documentation. Planned submission: approximately 2026-10-17; re-open these sources then for any changed schema. All listed pages loaded substantive documentation. The organization URL under configuring-issues redirects to the using-issues URL below. Rules are paraphrased; no future verification date is claimed.

| Source URL | Deciding knowledge |
| --- | --- |
| https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-issue-forms | Required name/description/body; optional title/labels/assignees/type/projects. Existing repository labels only. Organization issue type. Project OWNER/NUMBER and opener write permission. Unique template names. |
| https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/common-validation-errors-when-creating-issue-forms | Zero-based body error indexes. ID character restrictions and collisions. Similar labels can generate identical references. Explicit IDs distinguish duplicates; nested checkbox options have no IDs. Boolean-looking strings need quotes; forbidden key spellings remain prohibited. Input/textarea labels prohibit certain credential-related words; the documented example changes the label. |
| https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-githubs-form-schema | IDs exclude Markdown elements. Current upload and min_length support. Per-element attribute and validation table. Required is public-only. Dropdown default is indexed; default excludes None/n/a. Render prevents textarea attachment/Markdown editing. |
| https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository | Forms live in .github/ISSUE_TEMPLATE on default branch. config.yml controls blank issues and contact links, not individual form body fields. |
| https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/managing-issue-types-in-an-organization | Organization owners modify types. Maximum 25. Defaults Task/Bug/Feature are editable, disableable and deletable; inspect actual enabled inventory. |
| https://docs.github.com/en/issues/planning-and-tracking-with-projects/automating-your-project/adding-items-automatically | Per-project auto-add limits: Free 1, Pro 5, Team 5, Enterprise Cloud/Server 20. Select the repository separately from the filter. No automatic backfill on enabling. Matching created/updated items; supported filters is/label/reason/assignee/no, negation except no. |

## Upload extensions

From the form-schema page: archives .zip/.gz/.tar.gz, documents .pdf/.docx/.xlsx/.pptx and text .json/.py/.js/.ts/.log/.txt/.csv: 25 MB. Images .png/.jpg/.jpeg/.gif/.svg/.webp: 10 MB. Videos .mp4/.mov/.webm: 100 MB. accept belongs under validations and contains comma-separated extensions.

## Repair choices

Removing credential collection rather than disguising its label is this plugin’s safety rule of thumb, not GitHub’s documented repair requirement. Keeping valid questions, preferring narrow patches and offering native auto-add rather than more reporter access are editorial workflow choices. They are not extra GitHub schema requirements. A settings export establishes supplied state at its date, not live state today. Recheck only the platform rule or inventory that decides an unresolved change.

Additional source, read 2026-10-11: https://docs.github.com/en/issues/planning-and-tracking-with-projects/managing-your-project/managing-access-to-your-projects — project roles are separate from repository access; read allows viewing, write allows editing. Asking an admin to configure the replacement workflow is an editorial ownership choice, not a sourced minimum-role claim.

## Repair verification — 2026-10-11

Re-opened the schema, validation-errors and auto-add pages above on 2026-10-11. Confirmed the Markdown ID exception, credential-label example and all five plan limits directly. Publication URLs are tracked separately in BUILD-NOTES.md.

## Separate Actions routing — verified 2026-10-12

https://docs.github.com/en/issues/planning-and-tracking-with-projects/automating-your-project/automating-projects-using-actions — Actions can add issues to Projects through the API, independently of native auto-add configuration. The repository-scoped GITHUB_TOKEN cannot access Projects. GitHub recommends a GitHub App for organization projects, with organization Projects read/write permissions and repository issue read permissions for issue intake, installed for the relevant repositories; store the private key as an Actions secret. Matching current intake scope, handling later labels/state changes and backfilling supplied issues are rollout choices, not additional form-schema rules.
