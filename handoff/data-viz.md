# Design-system-applier handoff — data-viz

## Layout archetype

**6-section / Minimal** (with one V4 visual hinge added).

Reason: this is a narrative-led case about a single methodology shift (using agentic AI as a working business analyst), not a research- and process-heavy engagement with multiple prototypes or frameworks. The Sample 1 archetype fits: hero + StatRow → problem context → approach → process detail → DarkBand visual hinge → output description → takeaways → reflection.

## Components used (count 5 of 6 cap)

- **StatRow** (variant="dark") — directly under the hero. Carries the four key numbers from the synthesized deliverable (821 ratings, 40 themes, 7 critical themes, 1 service designer doing analyst work). The fourth stat is the case's thesis stated as a number.
- **BotanicalDivider** — placed once at the narrative hinge between the conventional-synthesis section and the "what I did differently" section, marking the pivot from "we did the votes" to "I gave the data to Claude Code."
- **PullQuote** ×2 — first one is Whitney quoting her own brief to Claude (the operating instructions that made the iteration work); second one is the meta-line about the case's actual argument, lifted from the body. The Critic flagged the second quote as candidate-for-cut and the Copywriter agreed in spirit; left in place because removing it is a structural call for the next composer round, not a design-system decision.
- **InsightCallout** ×2 — first one carries the "shift wasn't AI made the charts; the shift was iterating at conversation speed" reframe inside the approach section; second one is the explicit outcome-update TODO at the end (composer left this in deliberately as a placeholder for a future revision once leadership acts on the open questions).
- **DarkBand** — replaces the in-body Placeholder from the polished draft. Carries a side-by-side figure: tagged Miro board (before) next to two of the cleanest views from the final HTML (bubble chart + category × role heatmap). Sits between the process-detail section and the "what the final piece looks like" section as the visual hinge.

Components considered and skipped:

- **ProcessTimeline** — would over-formalize the iteration. The "Brief, draft, push back, repeat" section is already structured as bulleted rounds; a timeline would compete with that prose.
- **GPTConversation** / **SystemRulesExcerpt** / **ConversationStackFailure** / **InteractionModelComparison** / **RulesObservations** / **QuestionnaireTiers** — these are agetech-specific custom components. None of them apply to this case's content.

## Specimen choice

**pomegranate-split**

Reason: carried forward from the polished draft frontmatter (composer proposed it: "clustered themes opening to reveal what's inside" — fits a synthesis case where the work is segmenting one body of pain into legible parts). The visual exists in the V4 mockups as the "Minimal" sample's watermark. Converted from slug to path format (`/images/specimen-pomegranate-split.jpg`) to match the convention used by `agetech.mdx` and `ferguson-cx.mdx`.

The composer flagged a thistle/tangle motif as an alternative ("data-knot framing"). If you want a different specimen, change `specimen` in the MDX frontmatter.

## Image assets referenced (TODO — Whitney to upload)

- `/images/specimen-pomegranate-split.jpg` — cover specimen, set in frontmatter. Used by `CaseLayout.astro`. **Currently doesn't exist.** Upload before publishing or remove the frontmatter line to fall back to no specimen.
- `/images/data-viz/miro-before.jpg` — DarkBand left figure. The "before" Miro board with 40 themed stickies tagged by category, severity, and frequency. Composer confirmed there's a Miro screenshot in `raw-case-material/Data-Viz/` though it isn't a JPG yet; you may already have the source.
- `/images/data-viz/final-charts.jpg` — DarkBand right figure. Two views from the final interactive HTML deliverable: bubble chart of all 40 themes + category × role heatmap. Source is `raw-case-material/Data-Viz/retrospective-synth.html` — you'll want to screenshot the bubble chart and heatmap views and combine into a single JPG (or split into two figures if that reads cleaner).

If `/images/data-viz/` doesn't exist yet, create it under `public/`.

## Narrative content that didn't fit V4 vocabulary

- **The interactive HTML deliverable itself.** The strongest possible "show, don't tell" move for this particular case would be embedding or linking to a live version of `retrospective-synth.html` — both the composer and copywriter flagged this. The V4 vocabulary doesn't have a component for "embedded live artifact" today. Left out of the MDX. Worth raising as a future capability: this case is the strongest argument so far for an iframe or hosted-static-asset slot under `/artifacts/<slug>/`.

## Open questions for Whitney

- **Status field.** Set to `'published'` per the design-system-applier spec. The polished draft was `'draft'`. The case still has live TODOs (Felisha's last name, the outcome-update InsightCallout). Flip back to `'draft'` before merge if you don't want it live until those are filled in.
- **Felisha [LAST NAME — TODO]** appears three times: in `role`, `team`, and the body's second paragraph. Copywriter intentionally preserved the placeholder markup. Replace before merge.
- **Outcome InsightCallout at the bottom.** The Critic recommended cutting this on the grounds that the prose paragraph just above it already does the same work. The Copywriter agreed but kept it because the call is structural, not copy. Keep, replace with a real outcome line once you have one, or delete — your call.
- **Second PullQuote** ("Senior service designers don't have to choose..."). Same situation: Critic recommended replacing it with a Felisha quote or cutting it; left in because the call is structural.
- **`status: 'published'` + missing images.** The DarkBand figures will 404 until the `/images/data-viz/` assets exist. The visual-director step (next in the chain) typically swaps missing-asset references for `<Placeholder />` components so the page builds cleanly during preview. If you want to skip that step and ship straight, upload the images first, or temporarily comment out the DarkBand block.
- **Work page card.** Adding this case to `src/pages/work.astro` is a separate manual edit (per the site repo's CLAUDE.md). Not done here.
