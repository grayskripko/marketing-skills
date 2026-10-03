# Node types and the link matrix

Node types come from practitioner practice (PR); the next-step order and the counts are heuristics of this plugin.

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

overview → subtopic → comparison → how-to → question. A link between two children is allowed when the target is the natural next step for someone who has just read the source. Product and use-case pages may be linked from any child where the text discusses them.

## Matrix

| Link | Status | Rule |
|---|---|---|
| hub → every child | required | from the contents block and from the outline section that introduces the child |
| child → its hub | required | one upward link, plus the breadcrumb |
| child → child, next step | allowed | in the paragraph where the next step comes up |
| child → child, not a next step | not planned | leave out unless the user asks |
| other hub → child | guest | body links only; the child keeps one parent |
| between pages that share an intent | forbidden | they are merge or differentiate candidates instead |
| comparison page → each compared hub | required when a comparison page exists | the comparison sits above both hubs |

Default counts per child: one link up and at most 4 sibling links (heuristic of this plugin). The hub carries one link per child; a hub with many children groups them by section rather than in one list.
