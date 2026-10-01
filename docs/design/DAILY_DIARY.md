# Daily Diary Design Specification

## Document Status

- Feature: daily diary
- Product stage: concept development
- Last updated: 2026-09-27
- Status: recommended direction with unresolved design decisions
- Parent document: [APP_DESIGN.md](APP_DESIGN.md)
- Format exploration: [DIARY_FORMATS.md](DIARY_FORMATS.md)
- Daily landing exploration: [DAILY_LANDING.md](DAILY_LANDING.md)
- Diary history grid: [../features/FEATURE_DIARY_HISTORY_GRID.md](../features/FEATURE_DIARY_HISTORY_GRID.md)
- Daily color selection: [../features/FEATURE_DAILY_COLOR_SELECTION.md](../features/FEATURE_DAILY_COLOR_SELECTION.md)

## Current direct-access daily page — 2026-10-01

The owner clarified that minimalism must preserve visible core features and avoid unnecessary clicks. History, the gradient slider and optional writing are now visible on first render. A shade selection directly updates today's sample entry; only individual-date lookup and readback sit behind Entry details. This supersedes the rejected disclosure design below. Three-month history and simulated autosave remain prototype proposals. See the [current brief](../features/FEATURE_DAILY_PAGE_REBUILD.md).

## Rejected disclosure revision — 2026-10-01

The owner requested minimal visible detail with simple controls that reveal more. The current study gives the date priority; History opens the calendar and individual date readback near the top. Choose colour opens the shade slider; Use shade accepts a preview, then returns to the compact entry. Optional writing remains visible. No shade is implied before acceptance. The notebook and quotation remain unchanged. The explicit confirmation plus simulated note autosave is a review proposal, not a production decision. See the [current brief](../features/FEATURE_DAILY_PAGE_REBUILD.md).

## Earlier slider revision — 2026-10-01

The owner selected a one-dimensional gradient slider and requested history near the top, with a more connected page composition. The current order is date, compact history, quotation, shade slider, optional writing and one quiet save status. This supersedes the two-dimensional selector and bottom-history layout below. The shorter July–September sample range remains a review proposal. See the [current brief](../features/FEATURE_DAILY_PAGE_REBUILD.md).

## Current daily-page prototype — 2026-10-01

The owner rejected the overlapping archived page and requested a rebuild consistent with the accepted history grid. See the [rebuild brief](../features/FEATURE_DAILY_PAGE_REBUILD.md) and [interactive prototype](prototypes/daily-page.html). This focused HTML study supersedes the rejected page presentation; it does not select a production platform or finalize selector/save behavior. The current request authorizes this component revision before the broader screen map and Figma stages.

## Current V1 Interface Direction — 2026-09-19

The first V1 study is a single, minimal notebook page. It intentionally excludes the proposed opening animation, page gestures, cover, library, and scrapbook navigation while the core daily interaction is being resolved.

Current hierarchy:

1. Small date and season
2. Optional city-level location
3. Short quotation in a wispy italic accent face
4. Small prompt with wording still under review
5. One compact two-dimensional color selector without visible color names; its exact form remains undecided
6. Optional note showing only the placeholder “A thought, a fragment, a detail…”
7. Compact diary history grid populated by saved daily colors
8. Quiet automatic save state

Visual constraints:

- White page with curved notebook edges
- Simple red margin line
- No horizontal paper rules
- Two type roles: SF Pro for dates, metadata, controls, and writing; Baskerville Italic for the quote and restrained accent text
- A third typeface should be introduced only if a distinct functional role cannot be served by the first two
- Small sizes and regular weights; “wispy” must not become low-contrast or illegibly thin

The working save model is background draft saving. Whether a separate Done action is necessary remains unresolved. The previous full-width “Keep this moment” button is rejected as too bulky and generic.

The daily page should surface a compact contribution-style history grid that is separate from the color selector. It uses months across the top and one small cell per day. Saving an entry fills that date's cell with the exact color the user selected. As the user records more days, more cells become colored and consistency becomes visible through the filled pattern. Days without entries remain neutral. The grid must not reinterpret colors as contribution intensity or display a streak score.

A separate full-year calendar should arrange all 12 compact month grids in a 3-by-4 layout. Each month uses the colors recorded during that season so the palette shift becomes visible across the year.

Location can add meaningful context when revisiting a memory, but it should be optional and coarse. V1 should request a one-time location snapshot only while making an entry, store a user-readable city or region rather than continuous movement history, and allow manual entry or omission. Exact privacy and retention behavior remains to be specified before implementation.

### Prompt workshop

“Where are you today?” is rejected while location appears on the page because “where” reads as a geographic question.

Current candidates:

- “Today, in colour” — concise and directly connected to the selector
- “How did today feel?” — clearest emotional prompt, but more conventional
- “What stayed with you?” — reflective, but may read as a writing prompt rather than a color prompt
- No prompt — lets the date, quote, and selector establish the task

The location, if shown, belongs only in the date metadata. It should not be presented as an input field in the core daily flow.

The detailed recommendations below predate this revision where they conflict with it.

## Role in the Product

The daily diary is the product users actually live with. Seasonal art creates long-term meaning, but the diary must make a brief moment of attention feel worthwhile today.

Its purpose is to help the user:

- Pause without being delayed
- Name a feeling without reducing it to a score
- Preserve as much or as little context as they choose
- Leave with a sense of quiet closure
- Revisit their own memories without receiving an automated judgment

The diary is not an intake form, productivity habit, clinical assessment, social post, or prompt-writing interface.

## Experience Standard

Every state should feel intentionally designed, including:

- First use
- Ordinary repeat use
- A day when the user has little to say
- A day with mixed or difficult emotions
- An interrupted entry
- A missed day
- A return after a long absence
- Editing and deletion
- Offline use
- Persistence failure
- Large text and assistive-technology use

Visual richness alone does not satisfy this standard. Detail should clarify the experience, respect the user, or deepen its emotional character.

## Recommended Interaction Model

The diary is one page per day. A page contains one point selected from the current season’s color field and an optional short note. The user can return and edit it during the day.

This is a working hypothesis. One page per day keeps the Calendar and seasonal input understandable. A continuous-looking field allows nuance without requiring the user to choose from a rigid list of named emotions.

## Primary Flow

| Stage | User sees | User does | Product response |
| --- | --- | --- | --- |
| Arrive | Date, subtle seasonal context, one calm question | Pauses or begins immediately | No modal, tutorial, score, or countdown interrupts the task |
| Locate | A two-dimensional color field designed for the current season | Selects the point that feels closest to today | A clear marker samples the color and exposes a sensory description; subtle haptic is optional |
| Confirm | The selected pigment separated from the field | Keeps the selection or returns to adjust it | The sampled color becomes today’s material without receiving an emotional label |
| Write | A deliberately small writing area | Adds a word, phrase, or short note, or skips | Draft is preserved locally while typing |
| Keep | A clear closing action | Saves the entry | A restrained transition marks the moment as kept |
| Close | Saved daily page and routes to Calendar or exit | Leaves or revisits context | No advice, grade, confetti, or demand for another action |

## Screen Anatomy

### 1. Date and seasonal context

The top of the page should orient rather than measure.

Recommended content:

- Day and date
- Current season name or restrained seasonal marker
- Access to the Calendar

Do not lead with days remaining, number of completed entries, or a streak. Current-season information can be available through a secondary action.

The current direction places a minimal daily landing page before this entry sheet. The landing page holds the date and daily epigraph; the interactive color field appears only after the user opens today’s page.

### 2. Opening question

Use one short prompt that makes emotional room without sounding clinical or overly poetic.

Recommended initial direction:

> What is present today?

The prompt should remain stable enough to become familiar. Constantly changing copy can make the experience feel like a prompt generator rather than a ritual.

### 3. Seasonal color field

Use a two-dimensional field defined by two pigments that change with the season. The field blends between those pigments horizontally and moves from airy to deep vertically.

Recommended behavior:

- The field has no selected point until the user touches it.
- A tap places a sample marker; dragging allows optional refinement.
- The marker displays the exact sampled pigment outside the user’s finger.
- A second tap confirms the point, or the user can continue directly once a clear selection exists.
- The same point always returns the same pigment within that season.
- The field changes only at a seasonal boundary, not from day to day.

Touch users can respond intuitively to the field. Text descriptions and discrete step controls provide an equivalent way to adjust the pigment relationship and depth without relying on color or precise dragging.

The field, seasonal palettes, and semantic model are explored in [MOOD_INPUT.md](MOOD_INPUT.md).

### 4. Optional writing area

The writing area begins as a quiet invitation rather than a large empty text box.

Recommended label:

> Leave a line, if you want.

Behavior:

- Tapping expands the field and brings in the keyboard.
- The field grows for several lines, then scrolls internally only at an intentionally generous limit.
- A draft is saved locally during typing.
- A character count appears only near the limit.
- Dismissing the keyboard does not discard the text.
- The selected feeling remains visible while writing.

A working limit of roughly 500 characters preserves the lightweight character without making a difficult day fit into an arbitrary sentence. This requires prototype testing.

### 5. Closing action

The primary action should describe preservation, not task completion.

Recommended working label:

> Keep this moment

The control must look and behave like a button even if its visual styling is custom. It should remain visible with the keyboard open and at large text sizes without obscuring the note.

### 6. Saved state

After saving, the same page settles into read mode. The user sees what they recorded and can leave immediately.

Recommended acknowledgement:

> Kept for today.

This state should include a visible Edit action and access to the Calendar. It should not immediately show a mood analysis, motivational message, sharing prompt, or seasonal progress reward.

## Interaction Character

### Selection

A feeling selection should feel responsive but grounded. A small change in depth, border, texture, or scale can establish state. Optional haptics should use a restrained selection response rather than a celebratory impact.

### Saving

Saving can evoke placing a page, pressing a flower, closing a folio, or setting down a mark. The final metaphor should align with the scrapbook’s art direction.

The transition should:

- Last long enough to register but never block the user unnecessarily
- End in an unmistakable saved state
- Avoid previewing the seasonal artwork
- Have a crossfade or immediate alternative under Reduce Motion
- Work without sound or haptics

### Sound and haptics

Sound should be off by default unless research supports another choice. Haptics may reinforce selection and saving, with an in-app preference if their use becomes prominent.

Neither can carry information unavailable visually and semantically.

## Visual Direction

The diary’s object and calendar metaphors are explored in [DIARY_FORMATS.md](DIARY_FORMATS.md).

### Composition

The diary should use generous negative space and a clear top-to-bottom rhythm. It should not resemble a settings form or a dashboard made of cards.

The primary visual hierarchy is:

1. Opening question
2. Feeling selection
3. Optional writing
4. Closing action

Date and navigation remain available but visually quieter.

### Typography

Use an editorial voice for the prompt and a highly legible companion for controls and writing. A system-based pairing can create character without introducing licensing, performance, or legibility risk.

Typography should communicate calm through scale, spacing, and rhythm rather than very thin weights or low contrast.

### Color and material

The base interface should be quiet enough for mood colors and future artwork to have presence. Warm neutral surfaces, ink-like foregrounds, and restrained texture are possible directions.

Mood color should enrich the selection but never become the only indication of meaning or state. Texture must not reduce text contrast.

### Seasonal atmosphere

Subtle environmental details may shift over the season—for example light, tone, or background material. These should reflect passage of time, not claim to represent the user’s emotional state.

The effect should remain recognizable as the same product across seasons.

## Thoughtful Detail Opportunities

These areas can add value without adding product complexity:

### Draft continuity

If the user is interrupted, returning opens the unfinished entry exactly where they left it. The app does not turn an interruption into lost emotional effort.

### Stable prompts

The opening question changes rarely, if at all. Optional writing prompts can rotate slowly and never change while a draft is in progress.

### Honest timestamps

A backfilled entry is labeled as written later while still belonging to the intended date. The distinction should be quiet but preserved for trust.

### Respectful language

The app never says “Great job,” “You completed today,” or “You are doing better.” It acknowledges preservation rather than evaluating behavior or emotion.

### Keyboard care

The note remains visible when the keyboard appears, the save action is reachable, cursor position is preserved, and accidental dismissal never loses the draft.

### Visual continuity

The shape or material language used for daily feelings can reappear in the calendar and scrapbook metadata without exposing how the final artwork will look.

### Time-aware restraint

The app may adapt its ambient lighting to the local time of day, but the control hierarchy and mood meanings must remain stable. Dark mode should be intentionally composed rather than mechanically inverted.

### Meaningful emptiness

Blank space should create calm and focus. It should not hide necessary controls, make the screen feel unfinished, or require excessive scrolling.

## State Specifications

### No entry today

- Present the opening question and feeling selector.
- Keep optional writing secondary.
- Do not show an empty-state illustration that competes with the task.

### Draft exists

- Restore mood, nuance, note, and cursor state where practical.
- Indicate draft status subtly.
- Provide explicit discard behavior if the user chooses to start over.

### Entry saved today

- Open in read mode.
- Preserve the exact user language.
- Expose Edit without making it the primary action.
- Do not invite a second entry in the initial model.

### Editing

- Return to the same control layout used for creation.
- Preserve the original entry date and update the modification timestamp.
- Save replaces the current daily version.
- Cancel restores the last saved version, not the transient draft.

### Deleting

- Explain what will be removed and whether the entry has already contributed to a completed artwork.
- Require confirmation because deletion is destructive.
- Return focus to the logical date in the Calendar after dismissal.

### Missed day

- Display the day neutrally in the Calendar.
- Do not place an alert badge or warning color on it.
- If backfilling is supported, label the action “Add a memory” rather than implying the user failed to complete a task.

### Returning after an absence

- Open on today, not on a recovery flow.
- Do not enumerate missed days.
- Keep prior entries available without demanding that gaps be filled.

### Offline

- Creation, editing, saving, and Calendar access should work normally.
- No network status should be shown when it does not affect the diary task.

### Save failure

- Keep the full draft on screen and locally recoverable.
- State plainly that the moment was not yet saved.
- Offer Retry without blaming the user.
- Never play the completed save transition before persistence succeeds.

## Calendar Relationship

The diary and Calendar should feel like two views of the same material.

- Selecting a date opens its diary page.
- Returning from a past entry restores Calendar position and accessibility focus.
- Today is visually distinct but not ranked above other recorded days.
- Recorded, blank, and draft days have distinguishable text or symbols in addition to color.
- The Calendar may show the user’s chosen feeling but should not compute a visible quality score.

Detailed Calendar design will be specified separately.

## Notification Relationship

Reminders are optional and user-scheduled. Their purpose is invitation, not compliance.

Requirements:

- Ask for notification permission only after explaining the benefit and after the user chooses a reminder time.
- Do not use guilt, streak preservation, urgency, or artwork completion pressure.
- Tapping a reminder opens directly to today’s entry.
- Do not reveal mood text on the lock screen.
- Allow easy adjustment, pause, and disabling.

## Accessibility Contract

### Seasonal color field

- The field exposes its two source pigments, depth dimension, and current sampled value.
- Tap selection is supported; precise dragging is never required.
- An accessible alternative uses discrete steps or two adjustable controls for pigment relationship and depth.
- The sample marker and confirmation controls are at least 44 by 44 points.
- Selected state uses a marker, outline, description, and state announcement rather than color alone.
- VoiceOver, Voice Control, Switch Control, and Full Keyboard Access can select, adjust, reset, and confirm a point.
- Seasonal pigment descriptions are unique and speakable.

### Writing

- The field has a persistent accessible label rather than relying only on placeholder text.
- Dynamic Type does not hide the selected feeling, writing field, or save action.
- VoiceOver focus moves intentionally when optional content expands.
- Keyboard dismissal and focus changes do not discard text.

### Saving and transition

- The save control has a unique, speakable name and exposes disabled or saving state.
- Completion is announced once without moving focus unexpectedly.
- Reduce Motion replaces spatial movement with a short fade or immediate state change.
- Reduce Transparency uses solid surfaces with sufficient contrast.
- Sound and haptics are supplemental only.

### Simplified presentation

Under Assistive Access or an equivalent simplified mode, present fewer choices at once, use larger controls, and keep language literal while preserving the same diary task.

## Content Rules

- Do not diagnose, interpret, or prescribe.
- Do not label emotions as positive or negative.
- Do not imply that frequency equals commitment or wellness.
- Do not force written explanation.
- Do not expose private note content in notifications or widgets by default.
- Do not rewrite the user’s entry with AI.
- Do not use completion language associated with productivity tracking.

## Data and Privacy Requirements

- Drafts and saved entries are stored locally by default.
- Draft recovery should not require an account or network connection.
- Entry content is excluded from analytics and diagnostic logs.
- Product analytics, if added, record interaction events without mood labels or note text.
- The user can edit, delete, and eventually export their entries.
- Any later model processing must be separately disclosed and must not silently occur during daily entry.

## Prototype Questions

The first interactive prototype should test:

- Does the diary feel calm or merely empty?
- Can a first-time user understand the feeling selector without instruction?
- Does optional nuance feel expressive or burdensome?
- Does the writing invitation reduce pressure compared with a standard text box?
- Does “Keep this moment” feel natural and clear?
- Does the save interaction create closure without feeling slow?
- Is the sealed-season presence intriguing without becoming a progress mechanic?
- Can users complete the flow comfortably with large text and VoiceOver?
- Do returning users find value in the saved page and Calendar without generated insights?

## Decisions Needed

### Color-field semantics

Confirm the two-pigment seasonal pairs, airy-to-deep behavior, and accessible language explored in [MOOD_INPUT.md](MOOD_INPUT.md).

### Entry frequency

Confirm one editable page per day versus multiple moments per day.

### Writing constraint

Confirm the tone, expansion behavior, and maximum length of the note.

### Save metaphor

Choose a material action that can connect the diary to the eventual scrapbook without previewing the artwork. The current recommendation is a loose daily study being placed into a seasonal folio.

### Backfilling

Decide whether users can add past entries, how far back they can go, and how those entries are labeled.

### Weekly review

Decide whether it belongs in the initial product or should be tested after the basic daily ritual.

## Current Recommendation

Prototype the smallest emotionally complete version first:

1. One editable entry per day
2. One point selected from a season-specific two-dimensional color field
3. Optional note with a soft invitation
4. Explicit “Keep this moment” action with automatic local draft recovery
5. Restrained saved state with Edit and Calendar access
6. No streak, daily analysis, artwork preview, or weekly summary

The next design decision is the exact seasonal pigment pair and mixing behavior because they shape interaction, accessible descriptions, Calendar marks, and the seasonal art system.
