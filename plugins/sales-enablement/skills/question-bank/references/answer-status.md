# Answer status: buyer questions and what sellers said

How question-bank reads sales conversations for one thing: when buyers ask the same question, do the sellers answer it, with proof, and the same way? The unit is a buyer question paired with the seller's reply in the same conversation. Splitting conversations into such pairs and counting repeats is this plugin's method.

## Input gate

- At least 3 conversations, each with seller turns (call transcripts, email threads, chat logs). Fewer: offer call-coaching per call instead.
- Buyer-only material (quotes, survey answers, interview notes): one out-of-scope line, "This checks what your sellers answered; material without seller replies does not show that."
- Each conversation gets an id (C01, C02…) if it has none. Sellers become Seller-1, Seller-2; buyers are named by role (ground rule 7).

## Steps

1. Extract every buyer question (an explicit "?" or an indirect question or concern that needs an answer, such as "I'd need to know whether…"), with conversation id and turn, and the seller reply that follows, verbatim.
2. Group into canonical questions, each written as one plain sentence. **Merge rule**: two questions merge only when one correct answer would serve both. "Do you integrate with our CRM?" and "Does it sync both ways with our CRM?" do not merge: the second needs a different answer. Print the merge list.
3. Category: price, fit, integration, risk and security, timing, authority, status quo, competitor, other.
4. Count conversations containing the question (k of n; a conversation counts once), share and Wilson 95% interval (`rates.md`). k = 1 is labelled "n = 1, single mention" and is not ranked.
5. Where it comes up: first call, demo, pricing, late stage, as labelled in the input; otherwise "not labelled".
6. Each distinct seller answer, verbatim, with conversation id and seller pseudonym.
7. Status per canonical question:

| Status | Rule |
|---|---|
| answered with proof | the seller's answer points to something the buyer can check (a document, a demo of it, a reference customer or a figure from the user's material) and no other seller contradicts it |
| answered without proof | an answer is given but nothing checkable backs it |
| no answer | the seller deferred ("I'll check") with no follow-up in the input, changed the subject, or the question got no reply |
| contradictory | two answers cannot both be true or differ on a fact (number, yes/no, date); this beats every other status |

8. What followed: the next three buyer turns after each answer, labelled continued, changed topic or closed down; reported as "the conversation kept going in k of m", never as "this answer works".

## Answer gaps

Questions with status contradictory, no answer or answered without proof, ranked contradictory first, then no answer, then answered without proof, and by k (largest first) within each. For each gap: a proposed single answer built only from the user's material with its source line, otherwise [ANSWER NEEDED]. If the user's material shows one seller's answer is wrong, say which answer matches the material. Generic advice appears only when the user asks for ideas, in a box titled "Suggested, not from your conversations", at most 5 lines.

## Self-check (printed)

- every quote appears in the input (search for it);
- every count traces to listed conversation ids;
- no answer was invented to fill a gap.

## Diff against a previous bank

When an earlier bank is given: new questions, questions whose k grew or fell, questions not seen this time, and status changes (for example contradictory → answered with proof).

## Out of scope

Comparing won and lost deals, saying which answer "works", and buyer quotes without seller replies. Statuses are per question, never per seller; sellers appear only as pseudonyms beside their quotes.
