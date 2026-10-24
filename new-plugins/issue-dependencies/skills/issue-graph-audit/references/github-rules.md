# GitHub issue relationship sources

Verified by live page opens, read 2026-10-11. Scope: current GitHub.com documentation, not a future verification for the planned 2026-10-17 submission or a specific Enterprise Server version. All six canonical URLs loaded. Reopen these sources before submission if the snapshot changes.

| Source and URL | Deciding knowledge and scope |
|---|---|
| [Creating issue dependencies](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/creating-issue-dependencies) | “blocked by” identifies prerequisite work; “blocking” identifies work prevented by the focal issue. UI creation needs at least triage. Available on Free, Pro, Team and Enterprise Cloud. |
| [Adding sub-issues](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/adding-sub-issues) | 100 direct children per parent; eight nested sub-issue levels. Children may come from another repository. UI addition needs at least triage. The text does not specify whether a root is numbered zero or one. Record path nodes and edges at the boundary. |
| [GraphQL Issues](https://docs.github.com/en/graphql/reference/issues) | Issue fields parent, subIssues, subIssuesSummary, blockedBy, blocking and issueDependenciesSummary keep containment separate from blockers. Dependency totals include open and closed. Short count descriptions do not explicitly define an open-only filter. SubIssuesSummary exposes completed, total, percentCompleted; percent is Int, with no rounding rule here. AddBlockedByInput.issueId targets the blocked issue, blockingIssueId its blocker. AddSubIssueInput.replaceParent replaces an existing parent. GraphQL IDs are not REST numeric issue IDs or repository issue numbers. |
| [REST sub-issues](https://docs.github.com/en/rest/issues/sub-issues) | Get parent and list children have Issues/read permission for private resources; public reads can be unauthenticated. List defaults to 30, max 100 per page. Add uses numeric sub_issue_id, same owner as parent; replace_parent moves the current parent. Add needs Issues/write. Add errors include 403,404,410,422; 422 covers validation or spam detection, not a unique hierarchy diagnosis. |
| [REST issue dependencies](https://docs.github.com/en/rest/issues/issue-dependencies) | List blocked_by and blocking are separate directional endpoints. Lists default to 30, max 100 per page, with Issues/read for private resources. Public reads can be unauthenticated. Listed 404 does not establish why a reference is unavailable. These endpoints document data semantics only; the package does not call them. |
| [GraphQL pagination](https://docs.github.com/en/graphql/guides/using-pagination-in-the-graphql-api) | first/last is required on connections and is 1–100. Forward traversal uses hasNextPage and endCursor/after. Full pages alone do not establish completeness. |

## Rule of thumb: analysis conventions

Deduplicate inverse evidence; separate missing coverage from absent edges; report hierarchy and blocking cycles separately. Do not turn a closed parent/open child observation into an automatic closure policy. A count comparison is valid only for matching direction, scope, filters and snapshot. Treat permission gaps, null nodes and missing pages as unresolved. No dependency cap, closure cascade, cycle rejection message, integer rounding policy or root-numbering rule is established by these sources.

## Freshness and error handling

Keep the user's export time independent from this source-read date. API errors need their exact operation, response body and coverage before assigning a cause. Reparenting changes the subtree's location; audit its resulting path and the destination's direct-child count. This is an audit procedure, not an API call.

## Repair verification — read 2026-10-11

All six URLs reopened for bfix. REST path issue_number is the repository-local number; sub_issue_id is the numeric issue object ID. Neither that number nor a GraphQL node ID may be silently substituted for another identifier type. The same-owner requirement applies to REST add-sub-issue, independently of direct-child capacity and nesting. The GraphQL summary still explicitly defines open-and-closed only for total dependency fields; completed child membership needs its own evidence.
