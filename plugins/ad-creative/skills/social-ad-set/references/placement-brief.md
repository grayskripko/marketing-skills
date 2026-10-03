# Social placements: concepts, text sizing, safe zone, asset section

## Concept rows

A concept is one idea a viewer could repeat in a sentence ("month-end close without the backlog"). Variants inside a concept change exactly one declared variable and say which:

| Concept | Variant | Variable changed | Opening line | Proof (F-id) | Format | What this variant tests |
|---|---|---|---|---|---|---|

Variables to choose from: opening line, proof type (number, customer quote, demo), offer, format (static, short video, carousel), call to action. Two variants that differ only by synonyms are merged, and two concepts may not share both their angle and their proof. Write the variable down before writing the copy, so ad-test-readout can read the test later. Prefer 2–4 clearly different concepts over many small rewrites of one (heuristic, see `angle-method.md`).

## Text per placement

Size every field to the recommendation and show the hard limit next to it (`platform-specs.md`). Where only a recommendation exists, say "no hard limit stated; text past this point is cut in the feed". Where nothing is stated (TikTok caption), print "maximum unknown — check the platform's current spec" and keep the caption short by choice, not by a number.

## Video opening and on-screen text

- First line spoken or shown: the concept in plain words, no question that presumes something about the viewer (META-PA).
- On-screen text: about 7 words or fewer per card (a readability heuristic of this plugin, not a platform rule), placed inside the safe zone.

## Safe-zone arithmetic

Margin in pixels = percentage × canvas side, **rounded up** so text never sits inside the margin. Text box = canvas minus both margins.

Instagram Reels image, 1440×2560 (row M-IGR-SZ: 14% top, 35% bottom, 6% each side):
- top 0.14 × 2560 = 358.4 → 359 px
- bottom 0.35 × 2560 = 896 px
- each side 0.06 × 1440 = 86.4 → 87 px
- text box 1440 − 2×87 = 1266 px wide, 2560 − 359 − 896 = 1305 px tall, starting 87 px from the left and 359 px from the top.

For another canvas, recompute with the same rule. TikTok: no pixel values in the checked table; TikTok's in-feed page offers downloadable safe-zone templates in standard, right-to-left and with-anchor versions (row T-IF-VID), so point the user to them.

## Asset section (for whoever makes the visuals; this plugin makes none)

- Ratio, pixels and file limits per placement from `platform-specs.md`.
- Text layer: on-image words set by a person in a design tool, not left to an image model; they add to the headline rather than repeat it.
- Rights list: every person's likeness (signed release), music (licence covering paid ads), quoted reviews (permission and source), third-party logos (permission), stock items (licence covers ads).
- AI-artefact checklist, if any visual is AI-made or AI-edited: count fingers, limbs and objects; check repeated structures (fences, tiles, keys); check text inside the image is legible and spelled; check the product's shape, colours and label match the real one; check faces and voices are not a real person's.
- Disclosure lines: AI label on TikTok when content is made or significantly changed by AI (TT-AIGC); Google AI label optional (GOO-AI); creator or customer content made for any payment or perk discloses the connection inside the ad (US-FTC-END).
- Alt text: one plain sentence describing what is shown, for placements that accept it.

## Must-survive list

Qualifier words that keep the wrong buyers away. Remind the user that automated text options (for example, platform features that generate text variations or enhance creatives) can drop or reword them, so they should check those settings before launch. Google calls its feature text customization (formerly automatically created assets); Meta's creative enhancement setting names were not read at build, so name no setting for Meta.
