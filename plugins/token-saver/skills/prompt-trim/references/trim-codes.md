# Trim codes

Every change in the change table carries one code. A change without a code is not allowed.

| Code | Name | Use when | Never use for |
|---|---|---|---|
| T1 | Duplicate | the same instruction appears twice, in the same or different words | two rules that only look alike but differ in scope, such as "run tests" and "run tests before commit" |
| T2 | Filler | a sentence changes nothing the assistant does: greetings, praise, "please", "it is important that", restated headings | a sentence that sets tone when the user relies on that tone |
| T3 | Repeated example | an example shows a rule already stated clearly | the only example of a format that has no other description |
| T4 | Obsolete | the user said the rule no longer applies | anything the user did not mark |
| T5 | Move out | a block describes one workflow and could live in a file read only when that workflow runs | rules that apply to every task |

## Merging

Two rules may become one sentence when the merged sentence keeps every condition of both. Example (fictional):

- R1 "Always run tests." and R2 "ALWAYS run tests before commit." → "Always run the tests, including before every commit." The merged line keeps every condition of both, so no question is needed.

When scopes differ, keep both conditions in the merged line, as above, or keep both rules. Never narrow a rule. Ask only when the two rules conflict.

## Locked tokens

Inside any rule, these never change: numbers, names, paths, commands, flags, package names, quoted strings, and words in capitals that the author uses for emphasis on a prohibition ("never", "must not").
