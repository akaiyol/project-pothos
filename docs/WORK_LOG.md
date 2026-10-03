# Project Pothos — work log

Repository record of non-sensitive progress and direction. Append a dated entry for each meaningful session: work completed, confirmed direction, open questions, verification, and next step. Record whether the public snapshot changed and why. Distinguish proposals from approved decisions; do not invent past progress or store secrets here.

## 2026-09-27 — Identity and public presentation

### Confirmed direction

- Name: Project Pothos.
- Public framing: my personal art project, with an emphasis on design and an eventual connection to personal material.
- The README is for visitors and must not surface indecision.
- Its approved introduction stays fixed; meaningful snapshots update the content below it.
- Progress and direction belong in this separate log.

### Work completed

- Drafted a personal introduction and a notebook-study snapshot.
- Added README editorial rules and ignore patterns for private material, working documents, credentials, caches, and builds.

### Open questions

- Introduction wording awaits approval.
- App versus website remains undecided.
- Personal source material is undecided; photos are a possibility, not a requirement.

### Verification and publication

- The local repository has no commits or tracked files.
- Remote contents could not be retrieved through the web tool; no remote audit is claimed.
- Draft remains local; no commit or push was made.

### Next step

Review the README voice and introduction before publishing the first snapshot.

## 2026-09-27 — Personal introduction and curated features

- Replaced the prior conceptual introduction with the owner's values: colours, beautiful things, and sharing life and memories. Preserved “More to come!” as part of the fixed introduction.
- Removed “On the page”; drafted a short history-grid feature description.
- Updated guidelines: one or two ranked features, no third slot, replacements must be more interesting and better designed, and future README changes require permission. This supersedes the earlier automatic-refresh direction.
- Screenshot remains pending: located the existing history-grid HTML, but local Playwright has no installed browser and Google Chrome is unavailable. No image link was added and no visual verification is claimed.
- No commit or push made. Next step: capture and inspect the actual history-grid image for this feature.

## 2026-09-27 — Name definition

- Added the definition of Pothos directly beneath the README title, distinguishing its literal meaning from the project interpretation.
- Preserved the introduction and feature description. Updated README guidelines to retain this placement.

## 2026-09-27 — Owner copy and README formatting

- Preserved the owner's new introduction verbatim and synchronized the fixed introduction in process/README_GUIDELINES.md.
- Added spacing below the title, italicized the definition, and made Feature highlight a section heading above the feature title.
- Checked screenshot status: assets/ contains no image and the README has no image reference. Screenshot publication remains pending; nothing was pushed.

## 2026-09-27 — First GitHub publication

- Published README.md and .gitignore to akaiyol/project-pothos on main, commit 523d3ca.
- Private working documents and local instructions remain ignored.
- Used a GitHub noreply commit email. Screenshot remains pending and was not published.
- Push succeeded; local tracked working tree is clean.

## 2026-09-27 — Publish non-sensitive project content

- Owner clarified that all non-sensitive project content belongs in the repository. This supersedes earlier local-only rules for working documents.
- Included design briefs, ideas, README guidelines, work log, AGENTS.md, skill inventory, and project-scoped skill resources.
- Retained exclusions for credentials, private source material, machine-local settings, dependencies, and generated build output.
- Reviewed content for credential patterns and local paths; flagged skill references were explanatory security examples rather than secrets.
- The history-grid screenshot still does not exist in the project and is not part of this publication.

## 2026-09-27 — Repository organization

- Grouped design studies, feature briefs, and process guidance into docs/design/, docs/features/, and docs/process/. Moved the work log to docs/WORK_LOG.md.
- Added docs/README.md as the contributor index and updated document references.
- Preserved the public README and kept AGENTS.md and .agents/skills/ at discovery-compatible locations.
- No production scaffold or platform commitment was introduced.
- Verified local Markdown links after the moves.

## 2026-09-27 — Routine small-change publishing

- Owner requested that small changes always be pushed after completion and verification. Recorded this standing instruction in AGENTS.md.
- Prepared the documentation reorganization and publishing rule for commit and push. README content approval rules remain unchanged.

## 2026-09-27 — README history-grid screenshot

- Captured the existing history-grid prototype using sample data and added assets/history-grid.png.
- Linked the image beneath the README feature title without changing the introduction or feature description.
- Inspected all 12 captures: long and short date ranges at 320, 390, and 430 points with light and dark host backgrounds. The exported image uses the long April–October view.
- The standalone snapshot has no visible interactive controls; no product interaction behavior was changed.
- Checked the PNG and relative image path before publication.

## 2026-09-29 — Agent skill and plugin audit

### Work completed

- Audited the latest available snapshots of `openai/plugins`, `anthropics/skills`, `anthropics/claude-code`, and `dpearson2699/swift-ios-skills` against the app's design and implementation needs.
- Confirmed that the installed Swift/iOS source is still at the latest inspected upstream commit; no existing skill required replacement.
- Added six missing Swift/iOS foundations: architecture, concurrency, navigation, gestures, performance, and simulator workflows.
- Added Anthropic's `frontend-design` skill for subject-specific visual direction and anti-template critique.
- Added third-party source, revision, and license notices.

### Plugin findings

- `build-ios-apps` is the most valuable Codex code plugin once the Xcode project exists because it adds simulator, build, debug, performance, and leak tooling through XcodeBuildMCP.
- Figma is the most useful optional design integration when editable files or collaborative handoff become necessary.
- Claude Code's `feature-dev` duplicates the repository's feature-brief workflow; its review and security plugins are deferred until production code exists.
- No plugin was installed or connected during this audit.

### Verification and publication

- Verified every added skill has a readable `SKILL.md` and that no added skill contains executable files.
- Kept the public README unchanged.
- The unfinished daily color-selector prototype remains outside this audit's publication scope.

## 2026-09-29 — Figma design integration

- Connected the Figma plugin after the skill and plugin audit.
- Recorded its scope as optional design-file creation, design-system work, and SwiftUI handoff.
- Kept Figma's plugin-managed skills out of `.agents/skills/` to avoid duplicating or vendoring externally managed tooling.
- Preserved repository feature briefs and design decisions as the product source of truth.
- No Figma file or production implementation was created.

## 2026-10-01 — Tentative whole-product roadmap

- Added a dedicated tentative roadmap linking daily feature studies to the seasonal-art and collection vision, and linked it from the documentation index.
- Distinguished the existing product concept from an unresolved end-to-end experience. Flagged older mood-label and interaction proposals for reconciliation with newer requirements.
- Proposed milestones, evidence for advancement, and early seasonal-art exploration using synthetic data; dates, release scope, navigation, and platform remain unapproved.
- Documentation only: no production implementation or new visual verification. The public README snapshot is unchanged.
- Next step: review the whole-product journey and first-release boundary with the owner.

## 2026-10-01 — Photograph resonance direction

- Recorded the owner's tentative seasonal/yearly sentiment direction, personal photographic library, accompanying personal context, and requirement that photographs reflect the user's feelings.
- Recorded the explicit similarity-radius constraint: no forced nearest match; the no-match alternative is still undecided.
- Separated owner-stated direction from assistant suggestions, including user-confirmed reflections, local matching, match rejection, and yearly collections.
- Linked the decision record from the roadmap and documentation index. No daily-input requirements, production behavior, or public README content changed.
- Checked documentation links and whitespace; no prototype or matching validation is claimed.
- Next step: allow the owner to reflect before resolving the emotional input and fallback experience.

## 2026-10-01 — Decision-driven design workflow

- Owner requested a persistent workflow that advances after decisions without repeated proceed prompts.
- Added docs/process/DESIGN_WORKFLOW.md and linked it from AGENTS.md, the documentation index, and the roadmap. The sequence is screen/state mapping, incremental Figma prototyping, connected review, then an explicitly authorized implementation slice after platform selection.
- Defined decision gates, independent daily/seasonal progress, automatic follow-through, and a handoff containing the exact next action. Material product choices remain with the owner; routine authorized follow-through requires no renewed permission.
- Current stage: workflow documented; screen/state map and Figma file have not been created. No visual verification is claimed for this documentation change.
- Next action: prepare a proposed screen/state map and first-release boundary for review. After that review, update the relevant briefs and move the established daily pieces into Figma without another proceed prompt.
- Pending owner judgment: release boundary and material journey choices surfaced by the map. Seasonal emotional input, output intent, and fallback remain unresolved and retain the owner's reflection pause.
- Public README unchanged. Existing unrelated daily-colour brief edits are outside this change.

## 2026-10-01 — Rebuild the daily notebook around accepted history

- Owner rejected the overlapping archived daily-page render and explicitly requested a rebuild consistent with the accepted history grid. This authorizes a focused prototype revision before the broader screen-map/Figma work.
- Created FEATURE_DAILY_PAGE_REBUILD.md before the prototype. Preserved the white curved notebook, red margin, restrained type, optional note, and separate seven-row history grid. Continuous selector, autosave and the long history range are review proposals, not final product decisions.
- Added the standalone in-memory prototype at docs/design/prototypes/daily-page.html; synthetic entries reset on reload, with no network or persistence. Added links from the daily diary specification and documentation index.
- Verified 54 rendered states: nine states at 320/390/430 points on light/dark hosts, including 125% text. Inspected all six contact sheets after correcting weekday spacing and marker inset. Evidence and a repeatable browser check are in docs/design/reviews/daily-page-2026-10-01/.
- Interaction checks passed for tap, drag, note, disclosure, keyboard ranges, debounce, exact endpoint colour, single-day history updates, editing and reload. Native accessibility and real storage remain unverified and outside prototype scope.
- Next action: incorporate owner feedback on this concrete daily-page revision; once accepted, record the chosen details and return to the screen/state map and release boundary before the Figma connected journey. Do not ask for another proceed prompt for already-authorized corrections.
- Public README unchanged. Unrelated daily-colour brief edits preserved and excluded from this commit.

## 2026-10-01 — Shade slider and connected top-history layout

- Owner selected a gradient slider, moved diary history near the top, and authorized the remaining UI refinements. Updated the daily-page brief before revising the prototype. This supersedes the prior two-dimensional daily selector for this study.
- Reordered the page to date → history → quotation → slider → writing → save status. Proposed July–September history to improve cell readability. Preserved the notebook, palette, placeholder and quotation.
- Added one native range input with consistent gradient/thumb/saved-colour mapping and keyboard access. Removed coordinate controls and textarea resize chrome; notes expand with content.
- Inspected 60 rendered captures across 320/390/430 points, both host appearances and ten states. Tests passed for click/drag/keyboard endpoints, one-day exact-colour updates, note growth, reload and overflow. Evidence: design/reviews/daily-slider-2026-10-01/REVIEW.md. Native assistive technology, physical touch and durable storage remain outside this verification.
- Next action: incorporate owner feedback on the displayed slider/top-history composition. The three-month history range and save boundary remain decisions for review. After acceptance, return to the recorded screen/state map and release boundary before the connected Figma journey.
- Public README unchanged; pre-existing daily-colour brief edits remain outside this revision's commit.

## 2026-10-01 — Minimal daily page with expandable controls

- Owner authorized the UI-review improvements and asked for minimal, intuitive controls that reveal detail. Updated the feature brief before implementation. The prototype now prioritizes the date, existing quotation and writing; History and Choose colour reveal their controls inline.
- History remains near the top and exposes calendar labels, a date picker and textual colour/note readback. Colour preview is separate from acceptance: Use shade accepts the slider value, closes the editor and restores focus. The initial page has no implied colour selection. Three-month history and the confirmation/save boundary remain prototype proposals.
- Replaced raw RGB announcements with literal colour descriptions; preserved native controls and keyboard paths. Notes expand and shrink, and the in-memory record now includes their contents for history readback. Reload still resets all sample edits.
- Chromium and WebKit tests passed, including emulated touch, fresh keyboard midpoint confirmation, cancellation, exact endpoint RGB, one-day updates, rapid note edits, readback, clearing, hidden panels, control height, overflow and script-error checks.
- Inspected all 180 captures: 15 states × 320/390/430 widths × light/dark hosts × two engines. Independent reviewers checked 320 and 430; the primary reviewer checked 390. Rechecked after fixing disclosure timing, large-text placeholder clipping, WebKit resize warnings and date-picker appearance. Evidence: design/reviews/daily-minimal-2026-10-01/REVIEW.md.
- Physical iPhone/Safari, onscreen keyboard, VoiceOver, Switch Control and native Dynamic Type remain unverified; browser emulation does not replace them. No production platform or persistence was introduced.
- Exact next action: incorporate owner feedback on the minimal initial view and the expanded controls. Resolve the proposed history range and confirmation boundary during this review; after acceptance, continue the screen/state map and release boundary before the connected Figma journey.
- Public README unchanged. Pre-existing daily-colour brief edits remain outside this scoped commit.

## 2026-10-01 — Restore direct access to core diary features

- Owner clarified that minimalism must not hide features or require unnecessary clicks. Corrected the brief before revising the mockup. The earlier disclosure review passed rendering but missed this product requirement.
- Restored visible top history, directly usable shade slider and optional writing. Removed colour opening and confirmation steps. Only historical date lookup/readback uses a disclosure. Preserved the notebook, quotation, native controls and expanded-note behavior.
- Inspected 144 captures across Chromium/WebKit, 320/390/430, both host appearances and 12 states including 200% text. Interaction tests passed; evidence: design/reviews/daily-direct-2026-10-01/REVIEW.md. Physical assistive technology remains unverified.
- Exact next action: owner reviews this direct-access mockup and proposed three-month history range. Incorporate authorized feedback, then resume the screen/state map and release boundary before the connected Figma journey. Production saving remains unresolved.
- README unchanged; unrelated daily-colour brief edits excluded.

## 2026-10-01 — Record raised glass and moving stickers direction

- Owner requested a modern material direction before implementation: raised rounded glass with small outer margins, slight cloudiness and no tint, with falling stickers responding to phone orientation behind it. Technology metaphor is explicitly deferred.
- Added design/GLASS_DIARY_DIRECTION.md with confirmed intent, proposed layering, retained direct-access diary requirements, future verification criteria, unresolved choices and primary-source references. Linked it from the daily specification and documentation index.
- Documentation only; prototype and public README unchanged. No dependencies installed, artwork chosen or platform selected. Verified the documentation diff and reference links through primary project pages; no visual verification is claimed.
- Exact next action: owner reviews direction/reference shortlist; subsequent authorized visual study should establish material and layering, then motion. Sticker artwork and containment remain dependencies for implementation. Preserve the existing screen-map/Figma/production authorization boundaries.

## 2026-10-01 — Interactive raised glass diary study

- Owner authorized building the glass study on the direct-access diary. Added FEATURE_GLASS_DIARY_STUDY.md before implementation; preserved the prior notebook as daily-page-notebook.html.
- Replaced paper/red margin with raised cloudy neutral glass, sharper system typography and original sample stickers. Preserved top history, direct shade selection, writing and entry readback. Added preview tilt, drag, pause and optional sensor input outside diary controls.
- Initial review rejected unrestricted sticker positions because they visually contaminated diary colours and text. Revised the brief and bounded motion below the save status; separated preview rows at 200% text, then regenerated captures.
- Chromium/WebKit diary and motion checks passed: 228 captures across 320/390/430 and light/dark, including entry states, 200% text, paused/reduced motion, sensor fallback and contrast. Evidence: design/reviews/daily-glass-2026-10-01/REVIEW.md. Physical phone orientation and assistive technology remain unverified; glass is a CSS optical study rather than accurate refraction.
- Exact next action: owner evaluates material, proposed sticker artwork/compartment and motion feel. Incorporate authorized refinements, then carry the accepted surface into the screen-map/Figma journey. Technology metaphor and production platform remain unresolved.
- Public README unchanged; unrelated daily-colour brief edits preserved outside this commit.

Final localized correction: dark preview focus outline changed to light grey; all six affected dark tilted captures were regenerated and inspected in both engines. WebKit renders sticker details sharper than Chromium; material matching on a physical phone remains a follow-up.


## 2026-10-02 — Stars-only MVP and design-to-development gates

- Owner confirmed stars as the MVP sticker shape; mixed shapes and materials remain a later direction. Current authorization is mockup-only, without extra product features.
- Recorded the requested subtle orientation-responsive glass reflection exploration. Purple/blue are candidate hues; final palette, star finish/count and motion tuning remain open.
- Updated the glass brief and direction, and added a focused delivery roadmap: material revision, daily map/slice review, Figma connected prototype, development handoff, explicitly authorized implementation/device validation, then pilot and expansion.
- Figma begins after acceptance of the refined material and review of the daily map/slice; production development additionally requires selected platform, ready specification, resolved blocking decisions and explicit authorization. Seasonal work does not block the daily track.
- Documentation only; the existing mockup still uses earlier artwork. New revision criteria are unchecked. No new visual, motion or device verification is claimed; public README unchanged.
- Exact next action: revise the existing glass mockup to stars only and add subtle tilt-responsive reflections, then inspect affected states at 320/390/430 and supported appearances. Dependencies for Figma: owner acceptance of the revised surface/motion and review of the focused daily map/slice. Dependencies for development: connected prototype, approved brief, platform/storage decisions and explicit implementation authorization.


## 2026-10-03 — Figma Version 1 glass and diary palette

- Owner requested a simple clean/cyber glass mockup: grey, slight blue, shine and white highlights; varied random diary colours matching the original graph. Complex UX explicitly deferred.
- Added FEATURE_FIGMA_V1_MATERIAL.md before editing the existing Figma file XAcSMlGq99YjRtf7In3Xna. Changed background 1:2, added reflection 25:2/25:3 and recoloured 182 cells. Preserved original layout, wheel and copy; no new product features.
- Inspected six static width fixtures at 320/390/430 against light/dark surroundings after adding the reflective sheen. Evidence: design/reviews/figma-v1-material-2026-10-03/REVIEW.md and static-widths.png. Removed temporary fixtures and focused the original glass background.
- Static appearance only: small existing labels remain; no interaction, responsive runtime, sensor or native accessibility verification. This focused Figma authorization does not approve production development or unresolved UX.
- Exact next action: owner evaluates glass appearance and diary palette in the open Figma connector; incorporate their next scoped visual feedback. No additional UX decision is required for this material pass.
- README unchanged; unrelated daily-colour brief changes preserved.


## 2026-10-03 — Simplify Version 1 background and restrict diary palette

- Owner rejected reflective glass as silk-like; glass work deferred. Updated the focused brief before editing Figma to a light blue–white gradient, removing reflection and bevel effects.
- Interpreted the requested diary palette restriction as history cells using only colours available in the colour wheel. Sampled the current wheel gradient for every cell; no unrelated palette or independent darkening.
- Inspected updated six static fixtures at 320/390/430 against light/dark surroundings. Evidence: design/reviews/figma-v1-material-2026-10-03/simple-gradient-widths.png. Existing small-label limitation remains; no UX or interaction verification claimed. Removed temporary fixtures.
- Exact next action: owner reviews the simple gradient and wheel-matched history colours. Further glass work and complex UX stay deferred pending owner direction. README and unrelated edits unchanged.
