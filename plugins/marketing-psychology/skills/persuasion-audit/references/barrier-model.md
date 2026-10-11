# Barrier model

Two lenses, used in this order: first the quick motivation-ability-prompt check, then (in behavior-diagnosis) the fuller COM-B map.

## 1. Motivation, ability, prompt (L27)

A behaviour happens when the person is motivated enough, finds it easy enough, and gets a prompt at that moment. Name the binding barrier, the one that would change the outcome most if removed, and quote the input that shows it.

| Barrier | Signs in the input | Typical fixes |
|---|---|---|
| Ability (friction) | many fields or steps, unclear next step, jargon, setup needing another person, waiting, surprise costs | remove steps, pre-fill, plain words, show time needed, let the user hand a task to a colleague |
| Motivation | outcome vague, no proof for the reader's situation, risk not addressed | concrete outcome (result, time, who), real proof, risk reversal that is true |
| Prompt | no reminder or call to action at the moment the user is able to act | a prompt at that moment (in-app, email after the trigger event) |

Check ability, prompt and motivation; do not stop at the first failed check. Select a provisional main barrier using quoted evidence, severity, reach and dependencies. A genuine blocker warrants priority, but checklist order alone does not show which cause matters most.

Friction first: when ability is the binding barrier, fix it before adding persuasion (L32). Count friction from the input: steps, fields, decisions, waits, unknowns. Write "not stated" when the input does not say.

## 2. COM-B map (L28)

| Component | Plain question | Evidence to quote |
|---|---|---|
| Psychological capability | Do they know what to do and how? | confusion quotes, help tickets, drop at an explanation step |
| Physical capability | Can they physically do it (physical skill or stamina)? Rarely the barrier in software | physical limits |
| Physical opportunity | Does the environment allow it (time, tools, access, devices, permissions, money)? | "needed IT", wrong device, missing integrations, price |
| Social opportunity | Do people around them support it? | team approval, norms in their role |
| Reflective motivation | Do they believe it is worth it? | doubts about value, risk |
| Automatic motivation | Do habit and feeling pull them towards it or away? | anxiety, habit of an old tool |

Tag every barrier "observed" (cite the step count or a few words of the quote) or "assumed" (state what would confirm it: a count to pull, or one exit question at the drop step). In the answer, name barriers in plain words, not by component.

## 3. Intervention functions

Links used in this plugin, adapted from the Behaviour Change Wheel (L28). Coercion and restriction are excluded by rule: this plugin does not suggest penalties or removing options to force a behaviour.

| Barrier | Functions to consider |
|---|---|
| Psychological capability | education, training, enablement |
| Physical capability | training, enablement |
| Physical opportunity | environmental restructuring, enablement |
| Social opportunity | environmental restructuring, modelling, enablement |
| Reflective motivation | education, persuasion, incentivisation |
| Automatic motivation | persuasion, incentivisation, training, environmental restructuring, modelling, enablement |

Persuasion and incentivisation suggestions still need the "legitimate only if" fact and a register check.

## 4. Step rates with a Wilson 95% interval (L30)

For k successes out of n, with p = k/n and z = 1.96:

```
centre     = (p + z²/(2n)) / (1 + z²/n)
half-width = z × sqrt(p(1-p)/n + z²/(4n²)) / (1 + z²/n)
interval   = centre ± half-width
```

Default to counts, denominators, rates and absolute versus proportional losses. Sampling intervals are optional: print them only when requested or an inferential comparison is needed, with sampling assumptions stated. When printing an interval, use plain words with one decimal, rounding half away from zero: "600 of 1,000 opened setup: 60.0% (95% range 56.9–63.0%)". Use the host's code tool when one is available; otherwise work it by hand and show the inputs, with no remark about how it was computed. Judge uncertainty using interval width, event counts and the decision at stake, rather than a universal n = 30 cutoff. Write "n not given" for a rate without a denominator. Compare two segments only when both have counts; an inferential comparison uses the interval for the difference (Newcombe: with d = p1 − p2 and each rate's Wilson interval [l, u], low = d − √((p1 − l1)² + (u2 − p2)²), high = d + √((u1 − p1)² + (p2 − l2)²)), not by whether the two intervals overlap. Never turn a step rate into a lift prediction.
