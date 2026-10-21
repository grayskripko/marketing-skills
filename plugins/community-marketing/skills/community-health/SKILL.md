---
name: "community-health"
description: "Reads the health of a community the user runs from an export or from counts: unanswered questions, time to first human reply, how many newcomers get a reply and come back, and how much staff and a few members carry. Compares the community with its own past, not with outside benchmarks. Members appear only as ids; message text, names and emails are not needed and are not used in the output. Use when the user pastes community numbers or asks whether their own forum, Discord, Slack or user group is healthy, why newcomers don't come back, or how fast questions get answered."
---

# Community health

## A good answer

- Answers the question first, with the numbers worked inline (counts, percentages, differences).
- Checks that the definitions, dates and windows given fit together before relying on them; anything that cannot be true is named and the affected numbers treated as provisional.
- Separates what the counts show from what they cannot (cause, persistence), and, when useful, gives one sentence the user can repeat in a report.
- Intervals or significance tests only when asked; an experiment only when the user asks what to try next.
- Stays inside the scope the user set; members appear only as ids.

## Facts

- "90-9-1" is a rough pattern from a 2006 article that itself shows other splits (about 95-5-0.1 for blogs, 99.8-0.2-0.003 for Wikipedia edits); it is not a law of communities. Nielsen, "Participation Inequality", https://www.nngroup.com/articles/participation-inequality/ (checked 2026-10-03).
- Time to first response, as defined by CHAOSS: time from an item needing attention to the first reply, automated replies excluded. https://chaoss.community/?p=3448 (checked 2026-10-03).
- Contributor absence factor (CHAOSS): the smallest number of contributors who together made half of all contributions; a simple way to show how much a few people carry. https://chaoss.community/kb/metric-contributor-absence-factor/ (checked 2026-10-03).
- No published source supports a universal health threshold (for example "20% DAU/MAU is healthy"); compare the community with its own past.

How to use these facts: cite one only when it decides something in the user's case, in plain words with a short source name ("the FTC's endorsement guidance"). Give the URL only if the user asks where a rule comes from. Never print the check dates; they are for maintainers. Do not add a legal-disclaimer block.
