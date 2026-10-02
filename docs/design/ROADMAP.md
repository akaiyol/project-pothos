# Project Pothos — Tentative Roadmap

## Status and purpose

- Updated: 2026-10-02
- Status: design workflow agreed; milestone scope remains proposed; no delivery dates or release commitments
- Purpose: connect current component studies to a coherent whole-product experience.
- Platform: app versus website remains unresolved in the current project decisions.

This roadmap does not authorize production implementation or approve unresolved features. The latest user feedback and confirmed feature requirements take priority. Detailed behavior belongs in dedicated feature briefs before implementation.

## Where the project stands

The [product vision](APP_DESIGN.md) already describes a private daily journal whose accumulated reflections become seasonal artwork and a lasting scrapbook. The overall concept exists; the complete experience has not yet been designed and verified.

Current work is concentrated on the daily notebook page, [daily color selection](../features/FEATURE_DAILY_COLOR_SELECTION.md), seasonal palettes, and the [compact diary history grid](../features/FEATURE_DIARY_HISTORY_GRID.md). The history grid has an accepted visual snapshot. The selector alternatives, save behavior, and history date range remain under exploration. These studies are not a working end-to-end product.

The vision document also contains earlier mood-label, intensity, navigation, and animation proposals. They must be reconciled with newer color-first requirements and deferred-interaction rules before they are used as specifications.

## Glass diary MVP delivery roadmap

This focused track advances the current daily-page study without waiting for seasonal/photo decisions. Confirmed now: glass slate, stars behind it for MVP, orientation-responsive stars, exploration of subtle moving coloured reflections, and mockup-only work. Mixed shapes and materials are later scope. The full usable diary release boundary remains to be reviewed; “MVP stars” does not approve a production release.

| Stage | Deliverable | Gate to advance |
| --- | --- | --- |
| 1. Refine the material mockup — current | Revise the existing daily page: stars only, clearer glass depth and subtle tilt-responsive reflection. Preserve direct history, colour selection and writing. | Owner accepts the material direction and motion feel; inspect affected states at 320/390/430 and supported appearances. Physical sensor verification remains a separate requirement. |
| 2. Map the daily slice | A short screen/state map covering initial/empty diary, editing, saving/saved, history readback and motion/accessibility fallbacks. Identify remaining save/history decisions and the proposed first usable slice. | Owner reviews the slice boundary and resolves choices that block its connected prototype. Seasonal and mixed-material expansion do not block this daily track. |
| 3. Move the accepted design into Figma | Editable surface, star artwork, typography and controls; connected daily states and motion annotations. Continue unresolved details incrementally rather than recreating the material experiment in full. | Connected walkthrough has no material interaction gaps; required layouts/states are reviewed. Keep the interactive mockup alongside Figma as evidence for reflection and physics behavior. Figma alone does not verify phone motion. |
| 4. Prepare development handoff | Approved slice brief, assets, state/interaction specification, motion parameters, accessibility behavior and acceptance criteria. Assess platform/rendering feasibility and define storage/privacy boundaries. | Owner selects the platform, approves the production slice and explicitly authorizes implementation. Visual approval alone is insufficient. |
| 5. Develop and validate the authorized slice | Build the agreed daily flow, real saving/history and material/motion behavior with supported fallbacks. Verify actual phone tilt, touch, keyboard behavior, accessibility, performance and data integrity on the selected platform. | Slice acceptance criteria pass; report any device or performance limits. Confirm the pilot/release destination before distribution. |
| 6. Pilot and expand | Evaluate daily usability and motion comfort, fix findings, then consider mixed shapes and materials. | Evidence supports expansion and owner approves its scope; seasonal/photo features retain their separate decisions. |

**When Figma begins:** after the refined material direction is accepted and the focused daily screen/state map and slice boundary are reviewed. Do not wait for the whole product to be designed. Until then the existing interactive mockup remains the material experiment.

**When development begins:** after the connected Figma experience and implementation brief are ready, blocking product decisions are resolved, a platform is chosen, and production implementation is explicitly authorized. A small device feasibility experiment may be proposed during handoff; it requires separate authorization and does not establish production readiness.

**Exact next action:** revise the stars-only glass mockup and review its moving reflections. Then prepare the focused daily map and advance into Figma once its gate is satisfied. No Figma file or revised visual output is created by this documentation update.

## Working whole-product journey

Understand the private journal → choose a daily color and optionally write → save and revisit memories → reach a seasonal boundary → create and receive an artwork → preserve and revisit it in a collection.

This is a planning model drawn from the existing vision. Navigation, seasonal timing, artwork generation, and the collection experience remain unresolved. Daily use must retain value even before any artwork exists, and sparse entries must not be treated as failure.

## Proposed milestones

| Milestone | Intended outcome | Scope and decisions | Evidence needed before advancing |
| --- | --- | --- | --- |
| 1. Define the whole experience | A coherent product boundary and journey | Reconcile older proposals; map first use, daily use, revisiting, seasonal transition, artwork, and collection; distinguish first-release needs from later ideas. | A reviewed screen/state map, proposed release boundary, and explicit list of remaining decisions. |
| 2. Resolve the daily experience | A complete, lightweight daily action | Carry forward the selected direct gradient slider in the glass study; settle saving and editing behavior; decide the compact history range; define the separate full-year view and access to past entries. | Feature briefs and an interactive prototype covering empty, selected, saved, and revisited states, with required visual and accessibility checks. |
| 3. Test the seasonal promise | Evidence that accumulated daily colors can produce meaningful artwork | Use synthetic entries to study visual direction, the relationship between saved colors and artwork, sparse seasons, seasonal timing, and input privacy. Compare generation approaches only against those needs. | Reviewed artwork studies and a documented input-to-output rationale; a decision on whether the result supports the product promise. Start these studies alongside milestone 2 to expose major risks early. |
| 4. Connect the full journey | One understandable experience from first use through a completed season | Prototype onboarding, daily use, history, seasonal readiness, artwork creation/reveal, collection, and artwork detail. Define loading, failure/retry, no-artwork, and deletion states where applicable. | An end-to-end walkthrough using simulated time and sample data; no unexplained navigation gaps. It remains a prototype, not proof of production behavior. |
| 5. Choose and build the first release | A usable implementation of the agreed experience | Select platform; approve release scope and feature briefs; decide storage, export/deletion, and any remote processing; implement only after explicit authorization. | Working core flows, appropriate data and failure-path checks, and platform-specific accessibility and visual verification. |
| 6. Evaluate before expanding | Evidence of everyday and long-term value | Evaluate ease of daily recording, memory retrieval, trust, and whether artwork feels connected to the season. Use simulated seasonal transitions for early testing and actual use for longer-term findings. | Findings and a prioritized revision list; clearly distinguish observed use from prototype assumptions. |

## Near-term focus

1. Prepare and review the screen/state map and proposed first-release boundary.
2. Carry the established daily page and history grid into Figma; resolve the daily selector and connected states incrementally within updated feature briefs.
3. Explore seasonal input/output decisions separately, respecting the owner's pause for reflection. After those decisions, prepare a dedicated brief and studies using synthetic data.

The agreed [design workflow](../process/DESIGN_WORKFLOW.md) defines decision gates and automatic follow-through. Use Figma for editable layouts, component comparisons, and the connected visual prototype after the initial map is reviewed. Preserve established work; do not rebuild everything or wait for every future detail to be settled. Recreating screens alone does not satisfy a product milestone. Interactive behavior still needs appropriate prototype or implementation checks. Production work follows platform selection and explicit implementation authorization.

## Decisions requiring user judgment

The subsequent [photograph resonance discussion](PHOTOGRAPH_RESONANCE.md) records a tentative direction: personal photographs reflecting the user's feelings, with creator-authored context and a similarity radius that permits no match. Its emotional inputs, fallback, yearly output, and relationship to generated artwork remain unresolved. It refines the exploration for milestone 3 without approving implementation.

- What is essential to the first usable version: should it include the full seasonal-art and collection loop, or should a limited diary pilot precede it?
- What should connect the daily journal, history, current season, and completed artwork without adding unnecessary navigation?
- What makes a seasonal piece feel personally connected to the saved daily colors and optional writing?
- How are seasons defined, and what happens when someone starts late or records very little?
- Which platform best supports the intended experience, and what privacy/storage boundaries should it enforce?

## Deferred scope and verification

Book-opening animation, page-turn gestures, covers, and library navigation remain deferred ideas. Their presence in older documents does not make them roadmap commitments. Social features, scores, streaks, diagnostic interpretations, and general-purpose AI chat remain outside the existing product direction.

Each new feature requires a dedicated brief, implementation within its approved scope, verification, and handoff. Visual prototypes must pass the repository's rendered review at 320, 390, and 430 points for every affected variant and supported appearance. This planning document makes no new visual-verification or implementation-completion claims.
