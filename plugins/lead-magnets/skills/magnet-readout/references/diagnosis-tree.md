# Diagnosis tree and verdicts

Read the funnel from the top and stop at the first step that is clearly weak compared with the user's other magnets or the user's own stated goal. "Clearly" means the difference interval excludes 0 (`readout-math.md`); otherwise the step is "not distinguishable yet" and the tree moves on. With no other magnet and no stated goal, describe the shape of the funnel and give no "low" or "high" label.

| Where it drops | Likely cause | Next step |
|---|---|---|
| few sign-ups per visit | the page or the offer: weak promise, too many fields, wrong audience for the source | optin-check on the page; check the source mix first |
| sign-ups, but few confirmations | delivery: the confirmation email is late, filtered as spam or unclear | check sender rules and the confirmation email (optin-check OP-07, OP-18, OP-20) |
| confirmed, but few hand-raises | the bridge from asset to offer, or the follow-up | magnet-plan bridge test; magnet-followup message jobs |
| hand-raises, but few opportunities | reader fit or stage: the asset attracts people who cannot buy | magnet-plan S1 (stage and role) |
| opportunities, but few wins | outside this plugin (sales process) | report it and stop |

## Verdicts

Apply the rows in this order; the first that fires decides, so each magnet gets exactly one verdict: too early, retire, keep, fix bridge, fix page, hold. "Clearly lower" means the observed-difference interval excludes 0.

| Order | Verdict | Rule |
|---|---|---|
| 1 | too early | fewer than 30 sign-ups or fewer than 5 sales conversations for the magnet |
| 2 | retire | clearly lower on both views (sign-ups per visit and conversations per sign-up) than another magnet on the same source, with at least 20 events behind each compared rate |
| 3 | keep | the pipeline view (conversations or opportunities per visit) is the highest or not distinguishable from the highest |
| 4 | fix bridge | sign-ups per visit not clearly lower than any other magnet on the same source, and conversations per sign-up clearly lower than another magnet |
| 5 | fix page | sign-ups per visit clearly lower than another magnet on the same source, and conversations per sign-up not clearly lower |
| 6 | hold | none of the above fired: "not distinguishable yet", re-check with more data |

Each verdict prints the line that decided it. With "few events", "lag not checked" or "source not checked", the verdict is marked provisional.
