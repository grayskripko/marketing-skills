# Instagram evidence and drafting decisions

Verified/read on 2026-10-11. These are packaged observations, not live account checks. Read the applicable sections before drafting. Publication dates below are source dates; an older page still loading does not prove that every rollout detail remains current. The package never opens these URLs at runtime.

## Source register

- **S — Search:** [Breaking Down How Instagram Search Works](https://about.instagram.com/blog/announcements/break-down-how-instagram-search-works). Instagram, Adam Mosseri, published 2021-08-25. Full article retrieved successfully on the verification date. Its search explanation recommends relevant keywords and hashtags in captions rather than comments. It also describes personalization and popularity signals. This is historical first-party guidance, not a verified current ranking formula.
- **P — Production:** [IG User Media reference](https://developers.facebook.com/docs/instagram-platform/instagram-graph-api/reference/ig-user/media/). Meta developer documentation; whole-page revision date not supplied. Retrieved on the verification date, redirecting to Meta's documentation route with readable reference content. All numeric specifications below come from this retrieved page, not from a third-party summary. Scope: this publishing endpoint, not every Instagram app or scheduler.
- **O — Originality and recommendations:** [Ayudando a los creadores a encontrar nuevas audiencias](https://about.fb.com/ltam/news/2024/05/ayudando-a-los-creadores-a-encontrar-nuevas-audiencias/). Meta, published 2024-05-02; full Spanish article retrieved on the verification date. It describes replacing identical reposts with originals in recommendation surfaces, with matching-confidence, recency and substantial-transformation exceptions. It distinguishes recommendation rules from intellectual-property rules. Treat rollout specifics as historical, not a current eligibility verdict.
- **A — Accessibility:** [Using AI to Improve Photo Descriptions for People Who Are Blind and Visually Impaired](https://about.fb.com/news/2021/01/using-ai-to-improve-photo-descriptions-for-blind-and-visually-impaired-people/). Meta, published 2021-01-19, updated 2021-11-02; full article retrieved on the verification date. Explains screen-reader image descriptions and automatic alternative text; automatic recognition is not a reliable substitute for checking the actual image. Current endpoint support for custom image descriptions is independently documented by P.

Every linked source above returned a successful HTTP response and readable substantive content on 2026-10-11. Research evidence and response metadata are in the task scratch directory, outside the shipped plugin. Help Center pages that returned only a shell were excluded from the source register.

## Search: write the subject in the caption

S supports using accurate topic words and supplied location names naturally in the caption itself. Do not move all useful topic wording into a first comment. Choose a specific product, process or event noun from the facts; do not manufacture a location or stuff synonyms. No source here establishes an optimal hashtag count, a fixed visible-caption cutoff, exact ranking weights or a reach guarantee. Package hashtag defaults are editorial preferences. Historical placement guidance does not establish the current algorithm.

Worked example, fictional notes: a bike cleaning class in Leeds; brushes supplied; bring your bike. Caption opening: “Bike cleaning class in Leeds: brushes provided; bring your own bike.” This makes the subject explicit without inventing a discovery result. An unrelated #Viral tag supplies neither factual detail nor a supported benefit.

## Production: distinguish the publishing route

P documents the following endpoint constraints, read 2026-10-11:

| Field or format | Documented endpoint specification | Drafting decision |
|---|---|---|
| Caption | Maximum 2,200 characters, 30 hashtags, 20 @ tags | When the user specifies this API route, check the complete caption including tags and line breaks. Shorten without dropping terms or disclosures. These are ceilings, not targets or app-wide recommendations. |
| Carousel | Up to 10 image/video children; Reels cannot be carousel items | For an API-bound longer sequence, propose separate posts or an approved shorter version; never silently discard required points. Put the caption on the parent, not each child. A video carousel item is not a Reel. |
| Image alt_text | Up to 1,000 characters; single images and image children in carousels; not Reels or Stories | Provide separate image descriptions per actual image when useful; do not call Reel subtitles an alt_text field. |
| Image | JPEG; maximum 8 MB; aspect ratio 4:5 through 1.91:1; width 320–1,440 pixels; sRGB | For API-bound visual briefs, select a compatible frame and avoid placing required text where a proposed crop loses it. Text alone cannot certify the exported file. |
| Reel | MOV or MP4; HEVC or H264; 23–60 FPS; duration 3 seconds–15 minutes; maximum 300 MB; recommended 9:16 | Use a vertical filming brief where appropriate. Flag an out-of-range API duration and offer a feasible format, without guaranteeing successful upload or recommendation. |
| Reel cover | Recommended 9:16; nonmatching covers use a central 9:16 crop; feed cover uses central 1:1 crop | Keep the identifying subject and useful title in the central square; do not invent a universal pixel safe zone for overlays. Preview the actual crop during production. For an API editor handoff, identify the separate cover asset and move a bottom-edge title into the central square; describe these crops as the packaged endpoint specification, not a guarantee of every displayed surface. |

For ordinary manual-paste copy, follow the user's brief; do not assert these API numbers as current app maxima. If a requested size, hashtag quota or duration makes compatibility decisive and the route is unknown, ask which app or publisher they use. Do not issue a needless setup question for a short ordinary draft. Count characters deterministically when asserting exact length; ambiguous emoji counting or publisher validation requires checking the target tool, not guessing from a word count.

Worked example, fictional brief: an API-bound carousel with eleven required ideas. Offer a split carousel sequence or ask permission to merge related points; do not claim the app itself rejects eleven slides. For a Reel cover, place the repair subject and “Jacket zip repair” centrally rather than making the bottom edge the only place that says what the service is.

## Originality, rights and recommendation eligibility

O describes a preference for originals over confidently matched, relatively new identical reposts in recommendations, not removal of all reposts or a prohibition on quoting. It gives substantial transformation examples such as a new voiceover or reaction remix; those examples do not automatically confer rights or eligibility. Licensing/permission exceptions are discussed separately. Do not reuse historical repetition thresholds, appeal intervals or category lists as current policy; policies can change.

Draft from the user's owned notes and available original footage. When the plan relies on another creator's media, distinguish attributable quotation from copying their media. Ask for the public-use basis if it determines the plan; attribution alone is not permission. A new caption or credit line does not establish that an identical video is original. Offer original demonstration footage or a fact-based explanation rather than promising to evade duplicate detection. Do not remove a watermark merely to disguise ownership.

O also explains that content allowed on Instagram can be ineligible for recommendation. Its examples include clickbait, engagement bait and exaggerated health claims. Use an honest opening that delivers the promised information and a useful voluntary next step. Never certify recommendation eligibility from a text draft, or promise a change will restore reach. The user must review their account's status and current rules when eligibility is the actual question.

Worked example, fictional brief: “Use someone else's repair clip; change the caption so Instagram treats it as ours.” Plan a user-shot zip demonstration instead; retain credit for any approved quote. “Save this if you need the repair details later” is an editorial option; “Comment a word or we withhold the price” is not a substitute for stating essential offer terms.

## Accessibility and disclosures

A explains why descriptions matter to screen-reader users; P documents custom image descriptions for this endpoint. Draft alt text from a supplied photo description or approved visual plan, labeling a plan as provisional until the finished image is checked. Describe the relevant subject, action and essential visible wording; omit inferred identities, motives and unseen details. Alt text is separate from promotional caption copy and is not a keyword reservoir. For text-heavy slides, include essential slide wording in each image description. For Reels, supply a transcript/subtitle plan and include important silent visual information in speech or descriptive text; this is an editorial accessibility practice, not a claim about an API alt_text field or a current app menu. For an editor handoff, check the finished export muted: the service, qualifying conditions and next step should remain understandable. Budget spoken words around silent beats and allow pauses; shorten copy if the read-aloud check overruns.

Worked example, fictional supplied image: a hand beside a jacket zip and the visible words “Estimate after inspection.” Alt text: “Hand beside a jacket zip. Text: Estimate after inspection.” Do not replace this with a sales hook or infer that the person is a customer.

P documents a Paid partnership label mechanism separately from caption text. Preserve disclosed sponsorship in the draft. Include a brief reminder to review the separate platform label when the user asks for publishing guidance or the requested workflow depends on activating it; a caption-only rewrite does not need an extra publishing note. Writing “Paid partnership” in a caption does not activate the platform label. Do not infer sponsorship, submit IDs, set flags or certify legal compliance; this package only drafts text and production notes.

## Format choice

When the format is open, use a caption for a self-contained announcement around an existing image; use a carousel when the supplied explanation benefits from an ordered sequence; use a Reel when the available footage can demonstrate the point or a speaker can explain it. This is editorial judgment grounded in production feasibility, not an algorithm preference. Keep the user's chosen format where it can deliver the facts. Do not stretch a thin announcement into slides or manufacture footage just to suggest a supposedly favored format.
