# Node types and the link matrix

The node types are a convention of this plugin; the next-step order and the counts are heuristics of this plugin — apply user-supplied overrides; otherwise adapt only when task evidence justifies the change, stating any material change to the recommendation.

| Node type | Answers | Example |
|---|---|---|
| overview (hub) | the broad subject | "SOC 2 for software companies" |
| subtopic | one part of the subject | "SOC 2 trust services criteria" |
| comparison | choosing between two or more options | "SOC 2 vs ISO 27001" |
| question | one narrow question | "How long does a SOC 2 audit take?" |
| how-to | carrying out a task | "Preparing evidence for a SOC 2 audit" |
| use case | the subject for one role or industry | "SOC 2 for healthtech" |
| product or entity | a specific product, tool or organisation | "Our SOC 2 readiness module" |
| support | help for existing users | "Exporting the SOC 2 evidence report" |

## Next-step order

A link between members is allowed when it supports the intended website visitor's task: prerequisite, definition, reference, comparison, alternative or next action. Use supplied workflows to choose direction. Overview → subtopic → comparison → how-to → question is one educational example, not a universal order. Product and use-case links require relevant source content.

## Matrix

| Link | Status | Rule |
|---|---|---|
| hub → every child | required | from the contents block and from the outline section that introduces the child |
| structural child → its hub | required | upward link and, where present, the approved structural breadcrumb; curated members keep their structural chain and use a relevant body link to the topic hub |
| child → child, next step | allowed | in the paragraph where the next step comes up |
| member → member, prerequisite/reference/alternative | allowed when useful | place where the reader needs it; next-step status is not required |
| other hub → child | guest | body links only; the child keeps one parent |
| between pages that share an intent | review | preserve useful existing links; overlap alone neither forbids a link nor authorizes removal |
| comparison page → each compared hub | required when comparison exists | link to each subject; comparison does not automatically become their structural parent |

Structural children link upward; curated members retain their structural home and link contextually to the hub. Choose sibling links by reader need; four is only a review starting point. The hub links every member and groups large collections by useful sections.
