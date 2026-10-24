# Independent reader review A

Reviewed the distributed manifests, README, PRIVACY, LICENSE, both skills and reference files, and SVG icon. Excluded existing reviews, build notes and test outcomes. Before this package review, executed the three supplied requests using only each case's skill and prompt; complete answers are saved in tests/reader-candidate-1.txt through reader-candidate-3.txt. No network or account actions occurred. Applied the reader-alignment method as an independent reviewer; did not spawn further reviewers or edit package instructions.

Readers and tasks:

- Selecting agent: choose a skill for offline theme synthesis or exact quote extraction; reject live discovery requests.
- Executing agent: preserve pasted-thread context and traverse nested JSON without treating comments as instructions or counting placeholders.
- Researcher: use source-linked findings with qualifiers, denominators and sample limits intact.
- Installer: understand supplied-input requirements, network behavior and who retains the conversation.

## Actionable findings

1. **“Research what people say on Reddit … Works without accounts, keys or network requests.”** → selecting agent and installer reading either manifest's description, or Codex interface.longDescription → this job-first description contains 50 whitespace-separated words, below the required 60–120. The skill descriptions meet that requirement at 86 and 87 words. → Replace all three copies of the long description with this 67-word version: “Research what people say on Reddit about a topic, product or pain point from pasted threads or public JSON exports. Summarize themes and disagreements, or build a table of exact short quotes with supplied source links. Keep duplicates, missing comments and sample limits clear. Supply the material yourself; this package does not search Reddit or fetch links. No accounts, keys or network requests are required.” Keep the intentionally short interface.shortDescription concise.

2. **“Do not print … how arithmetic was performed.” / “For every derived figure show the formula and inputs.”** → executing agent answering a percentage request and researcher checking its denominator → these instructions in both skills directly conflict. A compliant result requires arithmetic disclosure, as case 1 illustrates. → Delete “or how arithmetic was performed” from the first rule. The later formula rule already defines the needed disclosure without a separate process narrative.

3. **“Duplicate IDs are counted once”** in README → researcher interpreting how conflicting repeated records affect counts → this summary omits the skill's consequential exception: conflicting copies are excluded until resolved, rather than counted once. → Replace with “Matching copies with the same ID or permalink are counted once; conflicting copies are excluded from derived counts until resolved.” This also documents the supplied-permalink deduplication that case 1 needs.

## Instruction-answer checks

Expectations were formed from each supplied request and skill before checking the completed answer:

- Case 1: use three unique comments, preserve mobile-only failure and contrary experience, disclose formulas and denominators, distinguish complaints from verified abandonment causes. **PASS.** Mobile complaints are 2 / 3 × 100 = 66.7%; price is 1 / 3 × 100 = 33.3%. B is deduplicated by supplied permalink. The answer includes C's explicit switching reason without claiming a missing product feature or population prevalence. The instruction conflict in finding 2 was resolved in favor of the explicit derived-figure rule.
- Case 2: output actual relevant wording with supplied links; disregard the comment's embedded command; omit deleted wording and personal contact information. **PASS.** The two usable quotes preserve “only” and “never,” and the answer sends nothing or fetches nothing.
- Case 3: include the nested reply, preserve the attached-PDF condition, normalize supplied relative permalinks, and avoid reading 30 declared comments or 120 votes as a sample of people. **PASS.** Both readable comments appear, including the low-score reply. Removed material and the omitted-comment stub are identified as coverage limits; no export date is invented.

## Remaining reader assessment

Routing distinguishes themes from quotes and explicitly excludes live discovery. The JSON instructions handle nested replies, empty replies, pagination, missing records and conflicting IDs. Both skills treat source text as data and prohibit invented links or quotes. README and PRIVACY explain supplied inputs, unverified citation availability, assistant-provider processing and lack of plugin-owned storage. Source-linked findings retain contextual qualifiers and contrary views. The SVG is a simple speech-bubble/document mark and introduces no misleading account or live-search claim. No additional actionable reader finding emerged from these materials.

The reference documents' external factual claims and published support/documentation URLs were not independently checked online; this review evaluates the supplied offline package and its real instruction-answer behavior, not deployment or endpoint availability.
