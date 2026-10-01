# Project Pothos — Tentative Roadmap

## Status and purpose

- Updated: 2026-10-01
- Status: proposed sequence for discussion; no delivery dates or release commitments
- Purpose: connect current component studies to a coherent whole-product experience.
- Platform: app versus website remains unresolved in the current project decisions.

This roadmap does not authorize production implementation or approve unresolved features. The latest user feedback and confirmed feature requirements take priority. Detailed behavior belongs in dedicated feature briefs before implementation.

## Where the project stands

The [product vision](APP_DESIGN.md) already describes a private daily journal whose accumulated reflections become seasonal artwork and a lasting scrapbook. The overall concept exists; the complete experience has not yet been designed and verified.

Current work is concentrated on the daily notebook page, [daily color selection](../features/FEATURE_DAILY_COLOR_SELECTION.md), seasonal palettes, and the [compact diary history grid](../features/FEATURE_DIARY_HISTORY_GRID.md). The history grid has an accepted visual snapshot. The selector alternatives, save behavior, and history date range remain under exploration. These studies are not a working end-to-end product.

The vision document also contains earlier mood-label, intensity, navigation, and animation proposals. They must be reconciled with newer color-first requirements and deferred-interaction rules before they are used as specifications.

## Working whole-product journey

Understand the private journal → choose a daily color and optionally write → save and revisit memories → reach a seasonal boundary → create and receive an artwork → preserve and revisit it in a collection.

This is a planning model drawn from the existing vision. Navigation, seasonal timing, artwork generation, and the collection experience remain unresolved. Daily use must retain value even before any artwork exists, and sparse entries must not be treated as failure.

## Proposed milestones

| Milestone | Intended outcome | Scope and decisions | Evidence needed before advancing |
| --- | --- | --- | --- |
| 1. Define the whole experience | A coherent product boundary and journey | Reconcile older proposals; map first use, daily use, revisiting, seasonal transition, artwork, and collection; distinguish first-release needs from later ideas. | A reviewed screen/state map, proposed release boundary, and explicit list of remaining decisions. |
| 2. Resolve the daily experience | A complete, lightweight daily action | Compare selector alternatives in the notebook page; settle saving and editing behavior; decide the compact history range; define the separate full-year view and access to past entries. | Feature briefs and an interactive prototype covering empty, selected, saved, and revisited states, with required visual and accessibility checks. |
| 3. Test the seasonal promise | Evidence that accumulated daily colors can produce meaningful artwork | Use synthetic entries to study visual direction, the relationship between saved colors and artwork, sparse seasons, seasonal timing, and input privacy. Compare generation approaches only against those needs. | Reviewed artwork studies and a documented input-to-output rationale; a decision on whether the result supports the product promise. Start these studies alongside milestone 2 to expose major risks early. |
| 4. Connect the full journey | One understandable experience from first use through a completed season | Prototype onboarding, daily use, history, seasonal readiness, artwork creation/reveal, collection, and artwork detail. Define loading, failure/retry, no-artwork, and deletion states where applicable. | An end-to-end walkthrough using simulated time and sample data; no unexplained navigation gaps. It remains a prototype, not proof of production behavior. |
| 5. Choose and build the first release | A usable implementation of the agreed experience | Select platform; approve release scope and feature briefs; decide storage, export/deletion, and any remote processing; implement only after explicit authorization. | Working core flows, appropriate data and failure-path checks, and platform-specific accessibility and visual verification. |
| 6. Evaluate before expanding | Evidence of everyday and long-term value | Evaluate ease of daily recording, memory retrieval, trust, and whether artwork feels connected to the season. Use simulated seasonal transitions for early testing and actual use for longer-term findings. | Findings and a prioritized revision list; clearly distinguish observed use from prototype assumptions. |

## Near-term focus

1. Review the whole-product journey and proposed first-release boundary before expanding the component inventory.
2. Continue the daily selector and history studies within their existing briefs.
3. Begin a small seasonal-art study using synthetic data so the central long-term promise is tested early.

Figma can support editable layouts, component comparisons, and a connected visual prototype. Whether to create that file remains a tooling choice; recreating screens alone does not satisfy a product milestone. Interactive behavior still needs appropriate prototype or implementation checks.

## Decisions requiring user judgment

- What is essential to the first usable version: should it include the full seasonal-art and collection loop, or should a limited diary pilot precede it?
- What should connect the daily journal, history, current season, and completed artwork without adding unnecessary navigation?
- What makes a seasonal piece feel personally connected to the saved daily colors and optional writing?
- How are seasons defined, and what happens when someone starts late or records very little?
- Which platform best supports the intended experience, and what privacy/storage boundaries should it enforce?

## Deferred scope and verification

Book-opening animation, page-turn gestures, covers, and library navigation remain deferred ideas. Their presence in older documents does not make them roadmap commitments. Social features, scores, streaks, diagnostic interpretations, and general-purpose AI chat remain outside the existing product direction.

Each new feature requires a dedicated brief, implementation within its approved scope, verification, and handoff. Visual prototypes must pass the repository's rendered review at 320, 390, and 430 points for every affected variant and supported appearance. This planning document makes no new visual-verification or implementation-completion claims.
