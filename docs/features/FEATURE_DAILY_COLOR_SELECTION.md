# Feature Brief: Daily Color Selection

## Document Status

- Feature: daily color selection and seasonal color mapping
- Stage: feature definition before visual prototyping
- Last updated: 2026-09-27
- Status: mapping model proposed; selector form and save behavior remain unresolved
- Parent specification: [../design/DAILY_DIARY.md](../design/DAILY_DIARY.md)
- Seasonal colors: [../design/SEASONAL_PALETTES.md](../design/SEASONAL_PALETTES.md)
- History output: [FEATURE_DIARY_HISTORY_GRID.md](FEATURE_DIARY_HISTORY_GRID.md)
- Earlier exploration: [../design/MOOD_INPUT.md](../design/MOOD_INPUT.md)

## Problem and User Value

The daily color choice must let a user register the character of a day quickly without forcing them to name, rank, or diagnose an emotion. It also needs enough structure that selections made across months become coherent material for the history grid and the seasonal artwork.

The control should feel expressive rather than technical, but its mapping must remain stable and reproducible. A saved choice cannot change meaning because the app appearance, palette tuning, or season later changes.

## Acceptance Checklist for the Next Prototype

- The selector is visibly separate from the diary history grid.
- It presents one two-dimensional choice using the palette for the entry date's season.
- It begins without a default selection.
- One tap is a complete valid choice; dragging only refines it.
- The interface shows no mood labels, scores, pigment names, or selected-color description.
- The selected state uses a small, high-contrast marker rather than a second large color sample.
- Saving fills the correct date in the history grid with the saved daily color.
- The same selection geometry works in all four seasons.
- Only one selector alternative is visible at a time.
- The control has an equivalent path that does not require precise dragging or color perception.

## Confirmed Decisions

- Color is the primary daily emotional input.
- The input is two-dimensional, flat, minimal, and seasonally constrained.
- The user chooses intuitively; the product does not translate the choice into emotion words.
- Each season is based on two anchor hues.
- The daily selector and contribution-style history grid are different components with different roles.
- The history cell represents the color saved for that date, not completion intensity.
- There is no preselected answer.
- The seasonal palette changes with the entry date, not the date on which an old entry is viewed.

## Proposed Mapping Model

The user selects a normalized position `(x, y)` within a seasonal field:

- `x`, from `0` to `1`, moves between the season's two anchor hues.
- `y`, from `0` to `1`, changes pigment presence from airy to deep.
- Neither axis represents positive versus negative emotion.
- The same position has the same structural meaning in every season.

The active palette is determined by the diary entry's calendar date. The sequence is:

`entry date -> season and palette version -> selected (x, y) -> resolved daily color -> saved history cell`

The interpolation method is not yet approved. It should be prototyped in a perceptual color space so the middle of the field does not become unintentionally gray or muddy.

## Seasonal Mapping

| Season | Horizontal anchors | Vertical behavior |
| --- | --- | --- |
| Spring | pastel pink to pea green | airy tint to deeper pigment |
| Summer | warm yellow to baby blue | airy tint to deeper pigment |
| Autumn | red-orange to warm plum | airy tint to deeper pigment |
| Winter | frost blue to softened mulberry | airy tint to deeper pigment |

The seasonal anchors constrain the day's color without assigning a fixed psychological meaning to either side. Seasonal identity should be visible across many saved entries, not through labels or decorative overlays.

## Data Represented

A saved daily color should retain:

- Entry date
- Season identifier derived for that date
- Palette version
- Normalized `x` coordinate
- Normalized `y` coordinate
- Canonical resolved color used for long-term continuity
- Appearance-specific display values if light and dark modes need separate renderings

Palette versioning prevents later art-direction changes from silently recoloring a user's history. The normalized coordinates remain useful as season-relative input for artwork generation, while the resolved color preserves what the user saw and saved.

## Information Hierarchy

1. Date and restrained seasonal context
2. Daily color selector
3. Selection marker
4. Optional written thought
5. Compact diary history grid
6. Quiet saved or saving state

The selector should not become the largest visual object on the page. Seasonal context should be communicated through its color range rather than explanatory copy.

## Primary Interaction

1. The page opens with the current seasonal field and no selected point.
2. The user taps once to choose a position.
3. A small marker appears at that position.
4. The user may drag the marker to refine the choice.
5. The selection becomes part of the day's entry at the approved save boundary.
6. The saved color fills the corresponding date in the history grid.

Changing the color before saving updates only the draft selection. The history grid should not imply that an unsaved draft is a completed entry.

## Selector Alternatives

### A. Continuous Two-Dimensional Field

- Offers the most nuance with a single tap.
- Looks clearly different from the history grid.
- Best expresses the idea that emotion does not fit into fixed categories.
- Risks implying false precision and requires a non-dragging accessible alternative.

### B. Stepped Two-Dimensional Matrix

- Provides a finite set of reproducible choices.
- Is easier to navigate with assistive input.
- Risks looking too similar to the history grid and making the two components' roles ambiguous.

### C. Color Constellation

- Uses a small set of spatially arranged color points with more open space.
- Can feel quieter and less like a technical color tool.
- Provides less nuance and weakens the consistent two-axis model.

The continuous field is the recommended first prototype because it preserves ambiguity, supports one-tap use, and remains visually distinct from the contribution-style history grid. It should be compared with a stepped alternative before the interaction is approved.

## Visual and Responsive Behavior

- Use a compact horizontal field rather than a dominant panel.
- Preserve the same aspect ratio and axis meaning at 320-, 390-, and 430-point widths.
- Keep the selection marker visible against every possible color using an adaptive boundary.
- Do not place labels, swatches, descriptions, or a second selector beneath the field.
- Only the selected selector alternative may occupy layout space.
- The control must remain legible on the white notebook page in light mode and against the surrounding interface in dark mode.

## States

### Empty

- Seasonal field is visible.
- No marker or implied answer is shown.
- History remains unchanged.

### Selected Draft

- Marker shows the draft position.
- Optional note can be entered independently.
- History remains unchanged until the entry reaches the approved save state.

### Saving

- The page exposes one restrained saving state.
- Repeated taps or navigation do not create duplicate entries.

### Saved

- Marker remains at the saved position.
- The correct history cell receives the saved daily color.
- Editing the color updates that one entry rather than creating another.

### Failure or Offline

- The selection remains locally recoverable.
- The app does not show a filled history cell if the entry cannot yet be treated as saved.
- Recovery language is factual and does not interrupt the reflective tone.

## Accessibility

- The two dimensions need adjustable, non-color-dependent values even though mood words remain absent.
- A stepped keyboard, switch-control, and VoiceOver path should move through finite coordinate increments.
- The marker needs shape and contrast, not color alone, to communicate selection.
- Haptics may confirm movement or selection but cannot be the only feedback.
- The saved history cell announces its date and recorded state; a color name is not sufficient.
- Dynamic Type must not push labels over the selector or history grid.
- Reduce Motion should remove any animated interpolation without changing the task.

## Privacy

The color choice is emotional diary data. It should be stored locally by default, excluded from analytics content, and sent to a model only when the user invokes seasonal artwork generation under the eventual data-use policy.

## Non-Goals

- Diagnosing, scoring, or naming the user's mood
- An unrestricted rainbow or system color picker
- Choosing colors from the history grid
- Previewing the seasonal artwork during daily entry
- Showing color trend analytics
- Adding texture, gesture, or a second color in the first selector prototype

## Acceptance Criteria

- A user can make a valid selection with one tap.
- No selection is present before user action.
- The selected position maps reproducibly to the palette for the entry date's season.
- The same normalized position can be represented across all four seasonal palettes.
- The selector contains no visible mood or pigment labels.
- The selector does not resemble or merge with the diary history grid.
- Saving updates exactly one history cell: the cell for the entry date.
- Past saved colors remain stable if a later palette version changes.
- Empty, selected, saving, saved, edit, failure, and offline behavior are defined before production implementation.
- The chosen prototype is rendered and visually inspected at 320, 390, and 430 points.
- Every visible interaction and the accessible alternative are exercised before the design is described as verified.

## Open Decisions

- Choose the first selector form to prototype: continuous field, stepped matrix, or color constellation.
- Decide whether the vertical axis changes lightness only or lightness and saturation together.
- Decide whether the continuous field is quantized internally and, if so, at what resolution.
- Define the save boundary: background autosave, explicit Done action, or another restrained mechanism.
- Decide whether a saved color is visually identical across light and dark appearances or has paired appearance-specific renderings.
- Define season dates and whether they follow the user's hemisphere.
- Decide how an accessible coordinate is described without introducing unwanted emotional labels.
