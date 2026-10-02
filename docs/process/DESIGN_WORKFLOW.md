# Design decisions and next steps

## Working agreement

Approved by the owner on 2026-10-01: map the experience first, resolve it incrementally in Figma, then build an agreed first slice after platform selection and explicit implementation authorization. Preserve established studies rather than rebuilding from scratch. Do not wait for every future feature to be settled before prototyping the current scope.

Markdown feature briefs remain the requirements source of truth. Figma holds editable visual studies and connected prototypes; a polished frame does not constitute approval or proof of working product behavior.

## Sequence and decision gates

| Stage | Work to prepare without another proceed prompt | User judgment needed | Next step once the gate is satisfied |
| --- | --- | --- | --- |
| 1. Screen and state map | Inventory existing pieces; map first use, daily entry, saving, revisiting, seasonal output, and collection. Mark confirmed, proposed, missing, and deferred states. Propose a first-release boundary. | Review the journey and release boundary; resolve only choices that block the next study. | Update affected briefs and prepare the daily experience in Figma. |
| 2. Daily experience | Carry forward the notebook page and accepted history-grid direction. Compare unresolved selectors in the same context; prototype entry, save, edit, history, and revisit states. | Select the interaction, save boundary, history range, and navigation behavior where still unresolved. | Record decisions, revise affected states, and run the required visual and interaction checks. |
| 3. Seasonal experience | Document input/output alternatives and dependencies alongside daily work. After the owner resolves the emotional-input and output intent, write a dedicated brief and prepare studies with synthetic data. | Decide how feelings are represented, how photographs relate to artwork, seasonal/yearly outputs, and insufficient-data/no-match behavior before dependent designs. | Prototype the approved seasonal direction and its non-ideal states, then connect it to daily history and the collection. |
| 4. Connected prototype | Assemble the agreed release journey, including applicable empty, partial, loading, error, privacy, and deletion states. Use simulated time and sample data. | Resolve material gaps exposed by the walkthrough and review the resulting experience. | Correct and verify the prototype; prepare the implementation scope and platform decision. |
| 5. First implementation slice | Prepare a concrete slice with approved briefs, data/privacy boundaries, acceptance criteria, dependencies, and a platform recommendation based on the agreed experience. | Select the platform and explicitly authorize production implementation. | Implement the authorized slice, verify it, and report results. Continue subsequent slices only within the authorized scope. |

Stages 2 and 3 may progress independently when their dependencies permit. An unresolved seasonal decision must not block independent daily-page work. Do not infer emotional categories from daily colours: the current input deliberately assigns no fixed emotional meaning to them. Preserve the pause for owner reflection recorded in the photograph direction until the owner resumes that decision.

## How to continue after a decision

1. Record the decision in the affected brief or design document, identify superseded guidance, and update the work log.
2. Check the next stage's dependencies and existing authorization. Approval of a decision triggers its already-authorized follow-through; do not ask “should I continue?” or ask the user to repeat the same decision.
3. Complete routine documentation, prototype revisions, verification, and scoped commit/push steps automatically within that authorization. Preserve accepted elements and unrelated work.
4. Ask only when an unresolved choice materially changes product behavior, scope, privacy, platform, or visual direction; when instructions conflict; or when a required authorization/access is missing. Present the concrete choice and consequence, not a broad request for direction. Do not invent product decisions to avoid asking.
5. Continue independent authorized work while a decision is pending. Silence, elapsed time, a draft, and successful rendering are not approval.
6. If verification exposes a flaw, correct it within the approved intent and recheck. Return to the owner only if the correction changes that intent. Report tool limitations without claiming completion.

Do not introduce a fresh approval gate for every routine design adjustment. Production implementation, README changes, deferred features, and actions outside the agreed scope retain their existing authorization requirements.

## Persistent handoff

At each meaningful stopping point, append to `docs/WORK_LOG.md`:

- Current stage and completed evidence
- Decisions made and affected source documents
- Exact next action and its dependencies
- Any specific question requiring owner judgment

On resuming, read that handoff and the current briefs, check for newer user feedback, and take the next authorized action. Do not restart discovery or request a general next-step instruction when the next action is already recorded.

## Current starting point

2026-10-02 update: the owner selected stars only for MVP stickers and requested a mockup with moving glass reflections. The focused [glass diary delivery roadmap](../design/ROADMAP.md#glass-diary-mvp-delivery-roadmap) governs the next sequence: refined material study → reviewed daily map/slice → Figma connected prototype → platform and authorized production slice → development/device validation → pilot. The whole-product map remains useful, but unresolved seasonal decisions do not delay this focused daily track.

The paragraph below records the earlier whole-product starting point; the material revision above is the immediate next action.

The next design task is a proposed screen/state map and first-release boundary. No map or Figma file is created by this workflow update. Carry forward the existing daily notebook, seasonal palette studies, selector alternatives, and accepted history snapshot. The full-year calendar and seasonal/photograph/collection experience still need connected screen and state definitions.

All visual work remains subject to the feature-brief workflow and rendered verification gate in [AGENTS.md](../../AGENTS.md), including every affected variant at 320, 390, and 430 points and supported appearances.
