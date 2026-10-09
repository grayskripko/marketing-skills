# Fix now, A/B test or research first

Every fix card ends with exactly one of three decisions.

## Fix now

No test needed, because there is nothing to learn that would change the call:
- something is broken (an error, a dead link, a field that rejects valid input);
- tracking is broken or the goal event fires twice;
- information the buyer needs is missing (price or price basis, renewal terms, delivery time, what happens after submit). Exception: a price withheld on purpose that no ad promised is a pricing decision, so Research first;
- a rule row came back FIX;
- an accessibility problem blocks the action (target too small to tap, label missing, text unreadable at the given colours).

Watch the result after shipping; that is monitoring, not a test.

## A/B test

Only for a change whose effect is uncertain and only when the test can finish: the ab-test-plan feasibility verdict at the user's traffic must be **Run** (or **Run only with** after the change is made bolder or moved to a busier step). When traffic is unknown, write "A/B test if feasible" and print the n per arm for one example lift so the user can judge.

## Research first

For Assumed findings, or a leak with no visible cause. Name one method:
- a one-question poll on that step ("What, if anything, is stopping you from …?"), read as themes, not percentages, below about 100 answers (heuristic);
- session recordings filtered to that step, where your visitors' consent allows recording;
- a task-based usability round with about five people per user group: it finds problems, it does not measure conversion (Jakob Nielsen, NN/g, 2000-03-18, https://www.nngroup.com/articles/why-you-only-need-to-test-with-5-users/, read 2026-10-03; numbers about rates need far larger samples);
- for a checkout or form step: the errors the server logged at that step, counted by type.

## Top 5 order

1. Seen and Data findings before Assumed ones (Assumed never enters the top 5).
2. Closer to the conversion goal first.
3. Lower effort first.

No invented impact scores, no predicted lift.

## Not now

Up to three tempting changes that should wait, one line each, with the reason (for example "redesign of the hero: no evidence it blocks anyone; research first").
