# Ramp plan: phases, timing rule and coach hours

Every value below is a default of this plugin that the user can change, printed in the plan so each hours figure can be recomputed.

## Inputs

Role (SDR, AE, AM, sales engineer, or the first seller after a founder); median sales cycle in days; typical deal size (context only); what the person already knows; existing materials; coach hours available per week. A target the user gives is noted as theirs and not used.

## Phases

1. **Learn**: material, product, buyer and process; knowledge checks from rep-certification.
2. **Practice and certify**: role-plays with hidden facts, scored with the shared rubric in certification mode; knowledge-check retests.
3. **Shadow and reverse shadow**: the rep listens to live calls, then leads calls while the coach listens and scores with the same rubric.
4. **Solo with scored calls**: the rep runs calls alone; the coach scores a sample of recorded or noted calls.

## Timing rule (stated, not a benchmark)

The solo phase lasts at least one median sales cycle before a closed deal is expected: solo weeks = ceil(cycle days ÷ 7). Default lengths for the other phases: learn 2 weeks, practice 2 weeks, shadow and reverse shadow 2 weeks. Total weeks = 6 + solo weeks with these defaults. Longer cycles mean a longer plan; that is the point of the rule.

| Phase | Default length | Gate to leave it |
|---|---|---|
| Learn | 2 weeks | knowledge check passed (80% and every critical item) |
| Practice and certify | 2 weeks | discovery role-play passed (16 of 22 or more, no 0 on critical rows) |
| Shadow and reverse shadow | 2 weeks | two reverse-shadow calls meet the discovery pass rule |
| Solo with scored calls | ceil(cycle days ÷ 7) weeks | first closed deal expected at the end of this phase, not before |

## Hour model (coach hours per activity)

| Activity | Hours |
|---|---|
| Weekly 1:1 | 0.5 |
| Review one knowledge check with the rep | 0.25 |
| Run and score one role-play | 0.5 |
| Debrief one shadowed call | 0.25 |
| Reverse-shadow call (0.5 h on the call + 0.25 h debrief) | 0.75 |
| Score one solo call from a recording or notes | 0.75 |

## Default activity counts per week

| Phase | Activities per week | Coach hours per week |
|---|---|---|
| Learn | 1:1 + 1 knowledge-check review | 0.5 + 0.25 = 0.75 |
| Practice | 1:1 + 3 role-plays + 1 knowledge-check review | 0.5 + 1.5 + 0.25 = 2.25 |
| Shadow / reverse | 1:1 + 3 shadow debriefs + 2 reverse-shadow calls | 0.5 + 0.75 + 1.5 = 2.75 |
| Solo | 1:1 + 2 scored calls | 0.5 + 1.5 = 2.0 |

## Coach-time budget

Per week: hours needed − hours available. A positive result is an overload week. Options to print: a peer scorer for role-plays, scoring recorded calls asynchronously, fewer role-plays per week with a longer practice phase (recompute the week count).

## Milestones as checks

Each milestone is something a person can observe, with who checks it and which Kirkpatrick level it gives evidence for (reaction, learning, behaviour, results; Kirkpatrick, 1959; Kirkpatrick & Kirkpatrick, 2016):

| Milestone | Check | Who | Level |
|---|---|---|---|
| Material understood | knowledge check passed (≥80%, critical items correct) | coach | learning |
| Discovery ready | role-play passed in certification mode: no 0 on CS-03, CS-05, CS-12 and ≥16 of 22 | coach or peer | learning |
| Demo ready | demo role-play: no 0 on CS-D02, CS-D08 and ≥12 of 16 | coach or peer | learning |
| Leads live calls | 2 reverse-shadow calls with the discovery pass rule met | coach | behaviour |
| Solo habits hold | scored solo calls meet the pass rule in k of n calls, k and n printed | coach | behaviour |
| First outcomes | the user's own measures (e.g. next steps agreed, first closed deal), named only, no target supplied | user | results |
| Rep's view | short rep feedback after each phase | rep | reaction |

"Training completed" is never a milestone on its own.

## Material checklist

Needed: product and pricing notes (for knowledge checks), at least one role-play brief per call type, a demo plan for the main buyer role, a bank of buyer questions with agreed answers. For each: exists or missing; missing items point to rep-certification, demo-runbook or question-bank.

## Worked example

AE, cycle 45 days, coach 2 hours a week.
- Weeks 1–2, learn: 0.5 + 0.25 = 0.75 h a week, fits.
- Weeks 3–4, practice: 0.5 + 3 × 0.5 + 0.25 = 2.25 h, over by 0.25 h.
- Weeks 5–6, shadow and reverse: 0.5 + 3 × 0.25 + 2 × 0.75 = 2.75 h, over by 0.75 h.
- Solo: ceil(45 ÷ 7) = 7 weeks (49 days ≥ 45), weeks 7–13: 0.5 + 2 × 0.75 = 2.0 h, fits.
- Total 13 weeks; coach hours 2 × 0.75 + 2 × 2.25 + 2 × 2.75 + 7 × 2.0 = 1.5 + 4.5 + 5.5 + 14.0 = 25.5 h.

## Not in this plan

First-day accounts and equipment, general HR goals, quota or attainment schedules, performance reviews.
