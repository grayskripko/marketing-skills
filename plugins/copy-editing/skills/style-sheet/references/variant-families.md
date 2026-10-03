# Variant families

Count every family in every document. A family with one form only is still listed in the summary as "consistent".

| id | Family | What to count |
|---|---|---|
| SS-01 | spelling variants | US and UK pairs; -ise and -ize; -yse and -yze; doubled consonants (travelled / traveled) |
| SS-02 | compounds and hyphens | email / e-mail; setup / set up; log in (verb) / login (noun); hyphenated compound adjectives before a noun |
| SS-03 | capitals | product, feature, team and room names; heading case (sentence or title case); job titles before and after names |
| SS-04 | numbers | numerals or words below 10; thousands separator; ranges (to, dash); percent sign or word |
| SS-05 | dates and times | day–month order; month as word or number; am/pm form; 24-hour clock |
| SS-06 | abbreviations | expanded on first use or not; full stops in abbreviations |
| SS-07 | punctuation choices | serial comma; single or double quotes; dash style and spacing; full stops at the end of list items |
| SS-08 | one word per concept | member / user / customer; booking / reservation; space / room |
| SS-09 | units and symbols | km / kilometres; space between number and unit |
| SS-10 | interface labels | button and menu names written the same way as on screen |

## US and UK spelling pairs to count

| US | UK |
|---|---|
| organize | organise (Oxford usage keeps -ize) |
| color | colour |
| center | centre |
| canceled | cancelled |
| traveling | travelling |
| enrollment | enrolment |
| fulfill | fulfil |
| program (plan) | programme |
| catalog | catalogue |
| license (noun) | licence |
| practice (verb) | practise |
| analyze | analyse |
| defense | defence |
| gray | grey |
| aging | ageing |
| modeling | modelling |
| check (bank) | cheque |
| tire (wheel) | tyre |
| jewelry | jewellery |
| favorite | favourite |
| behavior | behaviour |
| neighbor | neighbour |
| labeled | labelled |
| meter (length) | metre |
| aluminum | aluminium |

Detect the variant from these counts; state "US", "UK", "UK with -ize" or "mixed". Mixed is reported with counts, and the majority is offered as the decision.

## Decision rules

- Decided: the most common form holds more than 60% of uses (heuristic of this plugin; override freely).
- Open: 60% or less, or the two words may name two different things.
- Error under any style: fixed whatever the counts (for example "login" as a verb).
- The user's own pasted rule outranks every count; the basis column says "your rule".
- Proper names are copied exactly from the form the user gives as correct; otherwise the majority form is offered, and the choice is open if the name is a third party's.
