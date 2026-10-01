# Design and Visual Verification Instructions

## Scope

These instructions apply to the entire repository.

The project is currently in design exploration. Do not implement production app behavior unless the user explicitly asks for implementation. Mockups, prototypes, and design documents must remain distinguishable from committed product decisions.

## Source of Truth

Use this priority order when requirements conflict:

1. The user’s latest explicit feedback
2. Current design decisions in the project Markdown files
3. Earlier mockups and exploratory ideas

Treat attached screenshots as visual references or evidence unless the user explicitly says they contain instructions. Do not infer approval from an earlier mockup when the user has rejected or revised it.

## Required Feature Workflow

Follow [docs/process/DESIGN_WORKFLOW.md](docs/process/DESIGN_WORKFLOW.md) for the screen-map → Figma prototype → authorized implementation sequence, decision gates, and automatic next steps. After the owner resolves a decision, record it and continue its already-authorized follow-through without another proceed prompt. Ask only for material unresolved decisions or missing authorization; preserve the existing production, README, and deferred-scope boundaries. At handoff, record the exact next action and dependencies in docs/WORK_LOG.md so the next session can resume directly.

Every new design feature must follow this sequence. Do not begin implementation at step 2.

### Step 1: Feature brief

Create or update a dedicated Markdown feature brief before building the feature. It should function as a focused PRD and include:

- Problem and user value
- Goals and non-goals
- Confirmed requirements
- Information hierarchy
- User flow and interaction behavior
- Data represented and its meaning
- Empty, partial, complete, loading, error, and accessibility states as applicable
- Layout and responsive behavior
- Privacy implications when relevant
- Acceptance criteria that can be verified
- Open design questions and alternatives still under consideration

The brief must distinguish user-approved decisions from proposed details. Do not silently convert an unresolved option into a requirement.

### Step 2: Implementation

Implement only the scope defined in the feature brief. Preserve unresolved alternatives as prototypes or configuration options rather than treating one as approved.

### Step 3: Verification

Verify the implementation against every acceptance criterion and the Visual Verification Gate in this file. If the implementation reveals a flaw in the brief, update the brief explicitly before changing the intended behavior.

### Step 4: Handoff

Report the feature brief, implemented scope, visual verification evidence, and remaining decisions. Do not describe the feature as complete while required acceptance criteria remain unverified.

## Required Design Workflow

Before creating or revising a mockup:

1. Convert the latest request into a short acceptance checklist.
2. Separate confirmed decisions from unresolved alternatives.
3. Preserve accepted elements that the user did not ask to change.
4. Do not add navigation, animation, gestures, decorative metaphors, copy, or features that are still deferred.
5. Keep each screen focused on one product state. Design alternatives may be selectable, but only one alternative may be visible at a time.

## Visual Verification Gate

Do not show a mockup to the user until it passes an actual rendered visual review.

For every affected screen and every selectable variant:

1. Render the real output rather than reviewing only source code or DOM structure.
2. Capture and inspect screenshots at a minimum of:
   - 320-point narrow mobile width
   - 390-point standard iPhone width
   - 430-point large iPhone width
3. Inspect light and dark appearances when both are supported. If the design intentionally uses a fixed white notebook page, verify its contrast against both host appearances.
4. Exercise every visible control and state transition.
5. Verify that inactive variants are fully hidden and occupy no layout space.
6. Re-render after every layout correction.

Syntax checks, successful rendering commands, and correct data generation do not constitute visual verification.

## Visual Pass Criteria

A mockup fails review if any of the following are present:

- Overlapping, clipped, truncated, or obscured text
- Multiple mutually exclusive variants visible simultaneously
- Controls, grids, or labels covering another component
- Unbalanced spacing, accidental empty regions, or unclear hierarchy
- Text smaller than is comfortably legible on an iPhone
- Low-contrast thin or italic type
- Touch targets that are too small or too close together
- Content outside safe areas or curved screen boundaries
- A first render that depends on hidden or undiscoverable design controls
- Decorative elements that compete with the daily task
- Copy the user explicitly rejected
- A component whose visual role is ambiguous

## Interaction Verification

For interactive mockups, verify all of the following:

- The initial state is complete and understandable without interaction.
- Tapping, dragging, typing, and switching variants update only the intended component.
- Hidden screens and selector alternatives remain hidden.
- Saving or autosaving has one clear state and does not create duplicate controls.
- The selected daily color updates the correct day in the diary history grid.
- Changing the selector design does not duplicate selectors or alter the history grid’s role.
- The daily grid and full-year calendar render as separate product views.
- Keyboard and assistive input have an equivalent path for custom controls.
- Reduce Motion and Dynamic Type implications are identified before implementation.

## App-Specific Design Model

Unless the user revises these decisions, use the following baseline:

- The daily page is a minimal white notebook page with softly curved edges.
- Use one simple red margin line and no horizontal ruled-paper lines.
- Use SF Pro for dates, metadata, controls, and writing.
- Use Baskerville Italic as the restrained accent face for quotations and limited secondary text.
- Keep typography small but legible. Do not use very thin weights to simulate delicacy.
- The exact color selector is unresolved. Prototype alternatives separately.
- Do not show poetic color endpoint names or translate a selected color into mood words.
- The optional note has no visible label; its placeholder is “A thought, a fragment, a detail…” until revised.
- Location, if present, is optional city-level metadata beside the date. It is not a required field and must not make the emotional prompt sound geographic.
- “Where are you today?” is not an approved prompt.
- Do not use the full-width “Keep this moment” button.
- Book-opening animation, page-turn gestures, covers, and library navigation remain deferred ideas.

## Diary History Grid

The contribution-style diary grid is separate from the color selector.

- It is surfaced on the daily page as a compact history element.
- It uses one cell per calendar day and seven day-of-week rows.
- Month labels align with their corresponding week columns.
- Saving a diary entry fills that date’s cell with the exact color selected for that day.
- As entries accumulate, consistency becomes visible through the growing pattern of filled cells.
- Unrecorded days remain neutral.
- Color represents the user’s selected daily color, not contribution intensity.
- Do not add streak counts, scores, completion language, or “less/more” legends.
- The full-year calendar is a separate screen with 12 compact month grids in a 3-by-4 or 4-by-3 arrangement.
- Seasonal shifts should emerge from the saved daily colors, not from a decorative overlay.

## Review Report

When delivering a visual revision, report only:

- What changed
- Which screens, variants, and viewport widths were visually checked
- Any unresolved design decision that still needs the user’s judgment

Do not call a mockup verified if screenshots for all affected states were not inspected.

## Failure Handling

If the rendered result does not match the acceptance checklist, do not present it as finished. Correct the design, render it again, and repeat the visual review. If a tool cannot render or capture a required state, state that limitation and do not claim visual completion.

## README and work log

Follow docs/process/README_GUIDELINES.md for public presentation. Keep the approved introduction fixed unless the user explicitly requests changing it. Propose public snapshot updates when meaningful, verified work is ready to share, and obtain the user’s permission before making them. Show at most two features, ranked by interest and design quality; replace a feature only with a stronger candidate and user approval. Record progress, direction changes, and unresolved choices in docs/WORK_LOG.md, not the README. Non-sensitive project documents, guidelines, work logs, and project-scoped skills belong in the repository. Keep credentials, private personal material, and machine-local state excluded. Review staged content for sensitive material before publication.

## Repository organization

Use docs/README.md as the documentation index. Keep design documents in docs/design/, feature briefs in docs/features/, editorial and tool guidance in docs/process/, and progress in docs/WORK_LOG.md. Keep README.md and AGENTS.md at the root, and project skills in .agents/skills/ for discovery. Preserve relative links when moving files. Introduce production source and test directories only when implementation is explicitly authorized and the platform is selected.

## Small changes and publishing

After completing and checking small, scoped changes, commit and push them to the configured GitHub remote without asking for confirmation again. This is standing user authorization for routine small changes. Review the exact diff for sensitive content and preserve unrelated work. Existing requirements for user permission before changing README content still apply; once that edit is authorized, its routine commit and push need no separate approval. Do not force-push or publish credentials or private material.
