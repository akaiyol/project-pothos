# Feature Brief: Diary History Grid

## Document Status

- Feature: compact diary-entry history grid
- Stage: feature definition and visual prototype
- Last updated: 2026-09-27
- Status: accepted design snapshot; element removal and visible date range remain open
- Related daily specification: [../design/DAILY_DIARY.md](../design/DAILY_DIARY.md)
- Daily color selection: [FEATURE_DAILY_COLOR_SELECTION.md](FEATURE_DAILY_COLOR_SELECTION.md)
- Seasonal colors: [../design/SEASONAL_PALETTES.md](../design/SEASONAL_PALETTES.md)

## Accepted Snapshot — 2026-09-27

The current light-mode prototype is accepted as a useful snapshot of the intended history-grid direction. It is a baseline for further refinement, not final approval of every visible element. The default date range, user-facing title, and any elements to remove remain open.

## Problem

The seasonal artwork is intentionally delayed, so the daily page needs a quiet form of cumulative value. Users should be able to see their diary practice taking shape without introducing streak pressure, scores, or a preview of the final artwork.

## Feature Summary

Show a compact contribution-style calendar on the daily page. It follows the visual grammar of GitHub’s contribution grid in light mode:

- Seven weekday rows
- Consecutive weeks arranged as columns
- Month labels aligned above the relevant week columns
- Small evenly spaced square cells
- Neutral cells before an entry is recorded
- A recorded day filled with the exact color selected for that diary entry

The history grid is separate from the color selector. Choosing today’s color updates today’s history cell only after the entry is saved.

## Core UX Qualities

### Glanceable

The user should understand the recent rhythm of entries in one look. The component must remain compact enough to live on the daily page without competing with the diary input.

### Cumulative without pressure

Consistency becomes visible as cells fill, but the product does not count streaks, grade completion, or label missed days. Empty cells are factual, not punitive.

### Chronologically trustworthy

Every cell corresponds to one real calendar date. Weekday position, month boundaries, current day, and future dates must be accurate.

### Faithful to the diary

A filled cell uses the color saved for that date. Color does not represent frequency, intensity, completion quality, or an app-generated mood category.

### Seasonally legible

As months cross seasonal boundaries, the recorded colors should make the palette transition visible. The grid should help evaluate whether adjacent seasonal palettes feel cohesive and sufficiently distinct.

### Calm and restrained

The component should resemble a quiet archival index rather than a dashboard, analytics card, or gamification surface.

## Goals

- Surface recent diary history directly on the daily page.
- Make accumulating entries satisfying without adding a streak system.
- Preserve the exact saved color for every recorded day.
- Show month and seasonal progression clearly.
- Provide enough historical range to reveal seasonal transitions.
- Include one future month for temporal orientation without allowing future diary entries.
- Support evaluation and adjustment of the working seasonal palettes.

## Non-Goals

- Selecting today’s color
- Previewing the generated seasonal artwork
- Mood analytics or interpretation
- Streaks, contribution counts, completion percentages, or “less/more” legends
- Multiple entries per day
- Editing future dates
- Reproducing GitHub branding or engineering terminology in the user-facing app

## Date Window Alternatives

### Option A: five previous months, current month, one future month

- Seven visible months
- Best for seeing transitions across as many as three seasons
- Denser and requires smaller cells on an iPhone
- Recommended default for palette evaluation

### Option B: three previous months, current month, one future month

- Five visible months
- Larger and more legible cells
- Stronger fit on the daily page
- Usually shows one seasonal boundary rather than the broader yearly rhythm

Both ranges remain prototype options. The implementation must allow direct comparison before one is selected.

## Information Hierarchy

1. Small feature title or current season context
2. Season labels spanning their applicable months
3. Month labels aligned to week columns
4. Weekday reference labels for Monday, Wednesday, and Friday
5. Daily cells

Do not add a count, descriptive paragraph, streak label, legend, or motivational statement.

## Data Model

Each calendar date needs:

- Date
- Entry state: recorded, unrecorded, or future
- Saved season
- Saved normalized color coordinates or canonical saved color
- Light-mode rendered color

The grid derives position from the date. It must not store or infer position separately.

## Visual Behavior

### Recorded day

- Filled with the exact light-mode rendering of the saved daily color
- Remains visually distinct from the neutral background
- Has an accessible recorded-state description independent of color

### Unrecorded past day

- Neutral cell
- No warning, gap symbol, or negative state

### Current day

- Uses a subtle outline or shape distinction
- Displays today’s selected color after saving
- Does not pulse or demand completion

### Future day

- Neutral and noninteractive
- Visually quieter than an unrecorded past day if the distinction is needed
- Never accepts an entry from this component

### Seasonal boundary

- Month and season labels provide orientation
- Recorded colors reveal the transition
- Do not add a background tint, divider, or decorative overlay that could be mistaken for diary data

## Interaction

- The grid is read-only on the initial daily-page prototype.
- A later version may allow tapping a recorded cell to open that date’s diary page.
- Future cells are never interactive.
- The grid must not act as or visually merge with the color selector.

## Seasonal Palette Evaluation

The prototype exposes the two working light-mode anchors for each visible season as design controls. Adjustments update recorded cells for review without changing the underlying feature meaning.

Evaluate:

- Whether adjacent seasons are distinguishable at small cell sizes
- Whether transitions feel coherent rather than abrupt
- Whether pastel cells remain visible on a light neutral background
- Whether midpoints become muddy
- Whether autumn and winter dark values overpower spring and summer
- Whether color-vision differences collapse important distinctions

Palette controls are prototype tools, not app settings.

## Responsive Layout

- The component must fit without horizontal scrolling at 320, 390, and 430 points.
- Cell size may adapt to the selected date range.
- Month labels may shift to avoid collisions but must remain aligned with their first visible week.
- The seven weekday rows remain stable at every width.
- The component should not become a vertically stacked list of months on the daily page.

## Accessibility

- Provide one accessible element or navigable group for the grid with a concise summary.
- If individual cells become interactive later, each recorded cell must announce date and recorded state without relying on color names alone.
- Current day needs a non-color distinction.
- Do not use seasonal colors for text.
- Verify neutral and colored cell contrast in light mode.
- Maintain legibility under increased text size without letting labels cover cells.

## Acceptance Criteria

- The feature renders as a continuous GitHub-like week grid in light mode.
- The grid has exactly seven weekday rows.
- Month labels align with the correct week columns.
- The prototype can switch between five-past/current/one-future and three-past/current/one-future ranges.
- The future month is visible and contains no recorded entries.
- Recorded days use varied colors from the palette active on their saved dates.
- Seasonal changes are visible through cell colors and season labels.
- No “less/more” legend, score, streak, count, or explanatory slogan appears.
- The feature remains visually separate from the color selector.
- No text or cells overlap at 320, 390, or 430 points.
- Only one date-range variant is visible at a time.
- Light-mode palette controls can update spring, summer, and autumn anchors for evaluation.

## Open Decisions

- Choose the default range: five previous months or three previous months.
- Choose the component’s user-facing name; “commit grid” is a working analogy, not final product language.
- Decide whether unrecorded past days and future days need different neutral tones.
- Decide whether recorded cells eventually open past diary entries.
- Confirm whether seasons follow meteorological dates, astronomical dates, or a configurable regional model.
