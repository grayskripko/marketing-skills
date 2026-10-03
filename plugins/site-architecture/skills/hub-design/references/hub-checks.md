# Hub checks and the merge or split gate

## Merge or split gate

| Situation | Decision | Evidence needed | Source |
|---|---|---|---|
| Two pages with the same primary intent | listed for the user: merge, or rewrite one to a different intent | shared queries in pasted query-by-page rows; without them "Needs verification: query-by-page data" | PR |
| A page that would differ from an existing one only by a wording variant | no new page; extend the existing one | the user's query list | PR |
| A narrower subject: separate child or a section of the hub? | pasted top results are mostly pages dedicated to it → separate child; mostly general pages with a section on it → section of the hub | the top results the user pastes (this skill does not search) | PR, heuristic of this plugin |
| Two hubs that people compare | a comparison page above both, linking down to each hub | the user's statement or query data | PR |

The skill lists the pair and its evidence; the user decides. A merge the user confirms is handed to redirect-map as fate ("merged into"), with the surviving URL.

## HD checks

| Id | Check | Fails when |
|---|---|---|
| HD-01 | One hub per child | a child sits under two hubs |
| HD-02 | Hub links every child | any child missing from the hub's contents block or outline |
| HD-03 | Every child links up | a child without a body or breadcrumb link to its hub |
| HD-04 | No forbidden pair linked | two same-intent pages link to each other instead of being merged or differentiated |
| HD-05 | Distinct intents | two children share a primary intent |
| HD-06 | Contents block present | the hub has no block listing all children |
| HD-07 | Breadcrumb agrees | a child's breadcrumb parent is not the hub (for example still under Blog) |
| HD-08 | URLs checked | a URL not in the input and not marked NEW; print "n of n URLs checked against your data" |
