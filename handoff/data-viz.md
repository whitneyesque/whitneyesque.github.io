# Design-system-applier handoff — data-viz

## Layout archetype

**Hybrid, leaning Sample 1 (minimal / 6-section).**

Reason: this case is narrative-led — its argument is a back-to-back comparison (chatbot vs. agent) carried by prose, not by research artifacts or a multi-phase process. Sample 2's process timeline + experiment-card + dual insight callouts would over-instrument an essay-shaped case. The minimal archetype's rhythm (hero → stat row → body → reframe → body → outcome) maps cleanly onto round-one → round-two, with the BotanicalDivider sitting at the chatbot/agent hinge instead of the more conventional research/design hinge.

## Components used (count 4 of 6 cap)

- **StatRow** (variant `dark`, 4 stats) — opens the case directly under the hero. Converted from the polished draft's bolded "Key Stats" markdown bullets. Numbers are 821 / 40 / 7 / 1, with the punchline stat ("Service designer who has still never opened a Python file") preserved verbatim per copywriter pull-quote candidate notes.
- **InsightCallout** (3 placements) — kept exactly where the polished draft put them: (1) after "Same data, two AI surfaces" intro, framing what the case is about; (2) closing out Round Two's iteration list, naming the bottleneck shift from execution to articulation; (3) the closing TODO callout. Default sage variant on all three. The repeated InsightCallout inside one case sits inside the V4 spec's "max 1–2 per case study, never back-to-back" guidance — these are spaced apart and each does different work, but flagged below for Whitney's call (third one is a TODO marker, not real content yet).
- **PullQuote** (2 placements) — kept exactly as composer placed them: (1) Whitney's brief to Claude Code (attribution: *"from my brief to Claude Code"*), positioned as the opening sentence of Round Two; (2) the case's thesis line, *"I did not write the HTML… That division of labor is the point."* (attribution: *"What this case is actually about"*), positioned at the end of "What's actually different" as the section-break pull. Strong placement on both.
- **BotanicalDivider** — placed once, at the round-one → round-two pivot. This is the case's cognitive turn (the chatbot mode failing → the agent mode succeeding) and the divider earns it. Other candidate placements considered and rejected: between Round Two and "What's actually different" (the reflection pivot, but less load-bearing than the chatbot/agent hinge); after the closing PullQuote (pads the bottom without doing structural work).

**Plus scaffolding (not counted toward cap):**

- **Placeholder** ×2 — preserved from the polished draft for `bubble-v1.png` and `bubble-v2.png`. These two screenshots are the visual proof of the case's central comparison and the composer wrote thoughtful `ask` / `why` props for both. Visual-director should elevate or wrap in a figure block once Whitney provides the assets.

## Components considered and not used

- **DarkBand.** I considered framing the two bubble-chart screenshots as a single side-by-side DarkBand at the comparison hinge. Composer was explicit on this: *"Strongest visual pairing is now the round-one / round-two bubble charts side by side, in their respective sections (not as a single side-by-side composite)."* The narrative wants distance between the two images so the reader feels the round-one mess before the round-two relief. Followed the composer's call.
- **ProcessTimeline.** Forcing a "Round 1 → Round 2 → Final piece" timeline on this case would be a structural lie — the case isn't about a multi-phase project, it's about two ways of working on the same dataset. Skipped.
- **ExperimentCard.** No quantitative experiment in the case to anchor (no n=24 cohort, no controlled comparison with stats). The 2,000-cell / 821-rating / 40-theme numbers already live in the StatRow.
- **No second InsightCallout variant (`forest`).** All three callouts use the same default sage variant. The third (closing TODO) could swap to `forest` for visual differentiation if it stays as a real callout — but it's a TODO marker that will likely become prose, so left as default.

## Specimen choice

**Pomegranate** (split, per the polished draft's `specimen: 'pomegranate-split'` field).

Reason: Composer + copywriter handoff explicitly proposed pomegranate-split for this case, with two reads — *"clustered themes opening to reveal what's inside, plus the 'split' reads as the chatbot/agent comparison."* Both readings hold up: the pomegranate's interior structure (40 themes clustering into 7 critical / 9 categories) maps to the synthesis work, and the "split" reads directly to the round-one / round-two binary the case is built on. I converted the slug-style `'pomegranate-split'` to a path-style `'/images/specimen-pomegranate.jpg'` so it matches the live site's frontmatter convention (agetech, sfpl, ferguson-cx, ferguson-data all use full `/images/specimen-*.{jpg,png}` paths).

(If you want a different specimen, change `specimen` in the MDX frontmatter. The composer also flagged thistle/tangle as a fallback.)

## Image assets referenced (TODO — Whitney to upload)

- `/images/specimen-pomegranate.jpg` — hero specimen watermark. Does not yet exist in `public/images/`. The existing specimen library is rose, celosia, monarda, orchid, paradise, passion, protea, amaranthus — pomegranate would be a new addition. Confirm botanical, then shoot/source.
- `bubble-v1.png` — referenced inside the Round One Placeholder. Source asset is in `raw-case-material/Data-Viz/bubble-v1.png`. When elevated, will need a stable path under `public/images/data-viz/bubble-v1.png` (or similar). Caption (preserved from polished draft): *"Can you see the dark blue CR2 bubble? Can you??"*
- `bubble-v2.png` — referenced inside the Round Two Placeholder. Source asset is in `raw-case-material/Data-Viz/bubble-v2.png`. Same hosting + naming question as above. Caption: *"New bubble chart displays information about the data point when you hover over it."*

## Frontmatter changes vs. polished draft

- `status: 'draft'` (was: `'draft'`). Held at draft because the case still has two un-elevated Placeholders and a TODO InsightCallout, plus three `[LAST NAME — TODO]` markers for Felisha. Flip to `'published'` once those clear (matches ferguson-data's current state).
- `specimen: '/images/specimen-pomegranate.jpg'` (was: `'pomegranate-split'`). Path-format conversion to match the live layout's `<img src={specimen}>` rendering — the bare slug would render as a broken image src. No `specimenSignoff` field added; the layout doesn't currently render one and none of the shipped reference cases use it.
- `slug: 'data-viz'` added. The polished draft didn't include a slug field; all live cases have one in frontmatter. Added to match.

## Narrative content that didn't fit V4 vocabulary

- **The closing TODO InsightCallout.** The polished draft's last component is a placeholder for a future outcome update: *"TODO: outcome update once leadership has acted on (or quietly ignored) the open questions. Honest result either way."* Per the design-system-applier rules I did not modify the prose, so this lives in the file as-is. Two options for handling: (1) when leadership acts, replace the TODO with the real outcome line; (2) cut the callout entirely and let "What I'm still thinking about" close the case (it already names the open-questions ambiguity in body prose). My read: option (2) is cleaner. The TODO callout repeats a beat the body just named, and visually it stops the case mid-thought.
- **Three `[LAST NAME — TODO]` markers** in frontmatter (`role`, `team`) and body (one in the opening paragraph). Held verbatim from the polished draft per the no-modify-prose rule. Replace before publishing.
- **The live deployed URL** (`royal-night-e624.whitney-masulis.workers.dev`) was deliberately left out of the body by composer pending Whitney's call on whether to link to a personal-Workers-account artifact. The body says *"deployed to a public URL the studio can open in a meeting"* without the URL. If Whitney wants it included, the natural insertion point is the first sentence of "What the final piece looks like."
- **`agents vs llm.png`** — third-party Notion-AI explainer image in the raw material folder. Composer correctly flagged this as a citation/attribution risk and excluded it. Not surfaced in the case; not surfaced in any Placeholder. No action needed unless Whitney wants a sidelink.

## Open questions for Whitney

- **Specimen confirm.** Pomegranate has been the recommended specimen since round one. The composer's two reads (clustered/split) are both sharp, but pomegranate is not in the live specimen library yet and adding a botanical means a shoot. Confirm before we commission. Composer's fallback was thistle/tangle.
- **Closing InsightCallout TODO.** Keep as a placeholder for a future real outcome line, or cut and let "What I'm still thinking about" close the case? My recommendation is cut.
- **Live URL inclusion.** Composer's open question — *"Do you want the live URL included in the case body as a 'see the live deliverable' link?"* — still open. Currently absent from body. If included, it's the strongest possible "show, don't tell" closer the case could have.
- **Felisha's last name and exact role.** Three `[LAST NAME — TODO]` markers still in the file (frontmatter `role`, `team`, and body opening paragraph). Replace all three before flipping `status: 'published'`.
- **Status flip timing.** Currently `'draft'` because Placeholders + TODOs remain. Once visual-director adds its "What I need from you" section and Whitney resolves it, flip to `'published'` to make the case live at `/cases/data-viz.html`.
- **InsightCallout count.** Three callouts in one case sits at or just past the V4 spec's "max 1–2, never back-to-back" guidance. They are spaced apart and each does different work, but if the third one (the TODO) gets cut per my recommendation above, this lands at two cleanly.
