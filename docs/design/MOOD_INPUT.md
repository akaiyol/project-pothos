# Mood Input Design Exploration

## Document Status

- Feature: daily mood input
- Product stage: concept exploration
- Last updated: 2026-09-19
- Status: two-dimensional input direction retained; exact selector remains undecided; visible pigment naming rejected
- Related specification: [DAILY_DIARY.md](DAILY_DIARY.md)
- Seasonal palette specification: [SEASONAL_PALETTES.md](SEASONAL_PALETTES.md)

## Current V1 Revision — 2026-09-19

The mood input should remain two-dimensional, flat, and minimal. The exact selector has not been chosen.

- It is a plane, not a rendered material, raised surface, orb, or three-dimensional object.
- A subtle grid may clarify that both axes can be explored.
- The control uses one small marker and no enlarged sample, material animation, or descriptive result row.
- Visible endpoint names such as “Peony” and “Pea Leaf” are removed.
- The app does not name the selected color or translate it into mood language.
- Seasonal source colors may still shape the field internally, but their poetic pigment names are not part of the daily interface.
- Accessibility cannot depend on visible color alone; the equivalent nonvisual interaction remains an unresolved prototype requirement.

Three current prototype candidates:

1. Continuous field: maximum nuance, but may imply false precision.
2. Stepped grid: a finite two-dimensional matrix that is faster and easier to make accessible.
3. Color constellation: a small set of discrete choices placed spatially, with less technical visual character but less precision.

The daily history grid is not a selector. It is a separate record of saved entries and must never be presented as another way to choose today's color.

This direction supersedes the visible pigment labels, sensory descriptions, and material-study language in the earlier concepts below. Those sections are retained as design history, not current V1 requirements.

## Design Question

How can a user express the emotional character of a day in a few seconds without reducing it to a generic emoji, rigid label, or clinical score?

The input should be satisfying enough to use daily, understandable later in the Calendar, accessible without color perception, and useful as source material for seasonal art.

## Is a Mood and Color Chart a Good Experience?

Color is a strong foundation for this product, but a conventional continuous color chart is probably not the best final control.

### What works

- Selection can be immediate and intuitive.
- Color feels expressive rather than clinical.
- The diary, Calendar, and final artwork can share one visual language.
- A color choice can preserve ambiguity when no mood word feels accurate.
- The selected pigment can become direct art material instead of data that a model must psychologically interpret.

### What can go wrong

- Colors do not have universal emotional meanings.
- A full spectrum creates too many nearly identical choices and false precision.
- Users may choose a favorite color rather than the color that represents the day.
- A two-dimensional chart can feel like an assessment tool.
- Precise dragging is slower and less accessible than selecting a discrete option.
- Color alone is not usable by everyone and can become unclear when revisiting old entries.

### Design conclusion

Use a curated palette of discrete visual choices rather than an unrestricted color picker. Ask the user which color feels closest today instead of assigning each color a fixed emotion.

Words should remain available as optional personal meaning and as an accessible equivalent, but they do not need to dominate the visual experience.

## Concept A: Emotional Palette

### Idea

Present a small collection of tactile pigment swatches. The user selects the color that feels most like the day.

The palette is not a labeled scale from happy to sad. Each pigment is a valid material with its own depth, brightness, and visual presence.

### Interaction

1. The prompt asks, “What color does today leave behind?”
2. Six to nine large pigment swatches appear in a stable arrangement.
3. The user taps one swatch.
4. The chosen pigment comes into focus while the others recede.
5. The user can keep it immediately or add an optional undertone and note.

### Visual character

- Swatches resemble real pigment, ink, pastel, dyed paper, or another chosen medium.
- Subtle texture gives each one material presence.
- Selected state uses border, scale, symbol, and label in addition to color.
- The palette remains stable across days so the user develops a personal relationship with it.

### Strengths

- Fast and distinctive
- Directly connected to art-making
- Leaves emotional interpretation with the user
- Produces clear palette data for the seasonal artwork
- Can become a recognizable product signature

### Risks

- A single color may feel too reductive.
- Users may not remember what an old color meant.
- The system may be perceived as decorative rather than reflective.

### Response to the risks

Allow an optional second pigment as an undertone and an optional written line. On revisit, show the actual pigment, date, and any user-authored meaning rather than an app-generated interpretation.

## Concept B: Pigment and Gesture

### Idea

The user chooses both a color and the way that color behaves. Color captures emotional tone; gesture captures energy or texture.

Possible gesture families include:

- Still
- Flowing
- Flickering
- Scattered
- Knotted

Each gesture has a static pattern as well as optional subtle motion.

### Interaction

1. Select a pigment.
2. Select one of three or four visual gestures.
3. See the combination as a small material study.
4. Add an optional note and keep the moment.

### Strengths

- Captures more nuance than color alone.
- Creates rich inputs for seasonal composition.
- Makes two days with the same color meaningfully different.
- Feels like composing with artistic materials rather than completing a survey.

### Risks

- A second required decision may burden daily use.
- Animated options can be distracting or inaccessible.
- Users may not understand what each gesture represents.

### Best use

Treat gesture as optional refinement after color selection. Static texture, text descriptions, and non-motion selected states remain available at all times.

## Concept C: Tone and Undertone

### Idea

The user selects one main pigment and may layer a second pigment beneath it. This expresses mixed emotion using the language of painting rather than a list of mood terms.

### Interaction

1. Choose today’s tone.
2. Optionally respond to “Is there an undertone?”
3. Select a second pigment.
4. The two pigments appear layered, marbled, edged, or adjacent rather than blended into an indistinct color.

### Strengths

- Simple mental model
- Acknowledges mixed feelings
- Preserves the speed of a one-choice check-in
- Produces visually meaningful combinations for the Calendar and art system

### Risks

- “Tone” and “undertone” may be too abstract for some users.
- Literal color blending can become muddy or visually inconsistent.
- Two colors still do not express energy or intensity.

### Best use

Make the second color optional and preserve both source pigments rather than calculating a single blended result.

## Concept D: Atmospheric Studies

### Idea

Instead of colors, present a small set of abstract animated scenes: diffuse light, slow ripples, sharp static, drifting grain, dense fog, or expanding space. The user chooses the atmosphere that feels closest.

### Strengths

- Highly experiential and memorable
- Expresses qualities that a single color cannot
- Can establish a strong visual identity

### Risks

- Expensive to design and maintain well
- Slower to scan than a palette
- Motion may be overwhelming or inaccessible
- Can feel like choosing a wallpaper instead of recording a mood
- Meanings may be difficult to remember in the Calendar

### Best use

Explore as a later refinement of Pigment and Gesture, not as the first prototype.

## Concept E: A Daily Mark

### Idea

The user creates one simple mark through a short gesture. Pressure, speed, direction, and length influence its appearance.

### Strengths

- Each entry is genuinely personal.
- The act itself may feel meditative.
- Seasonal art can be composed from marks the user actually made.

### Risks

- Motor ability and device hardware affect the result.
- Users may feel pressure to make the mark aesthetically pleasing.
- Meaning is inconsistent and hard to revisit.
- Gesture-only input creates major accessibility issues.
- Daily effort is less predictable.

### Best use

Consider it as an optional expressive addition later, not the required mood input.

## Concept F: Seasonal Color Field

### Idea

Present a continuous-looking two-dimensional field of color and material. Each season is defined by two pigments. The field blends between them horizontally and moves from airy to deep vertically.

The user does not select a named emotion. They locate the point that feels closest to the day.

### Stable geometry

The recommended field uses:

- Horizontal: seasonal pigment A to seasonal pigment B
- Vertical: airy to deep

The interaction remains consistent across the year even though the horizontal pigment names change. Neither direction is assigned a universal emotion or treated as better.

### Seasonal rendering

Each season uses two defining pigments:

- Spring: Peony and Pea Leaf
- Summer: Sunstone and Baby Sky
- Autumn: Red Persimmon and Damson
- Winter: Frost Blue and Soft Mulberry Ink

The upper field mixes both pigments toward a shared paper surface. The lower field deepens them toward ink. This creates light, dark, muted, and concentrated regions without introducing unrelated seasonal colors.

### Interaction

1. The field appears with no preselected value.
2. The user taps anywhere that feels appropriate.
3. A marker samples the point and displays its pigment clearly above the finger.
4. The user can drag to refine or keep the first tap.
5. The selected sample separates from the field and becomes the day’s mark.
6. The user may add a written line before saving.

### Why the dimensions remain stable

Changing the field geometry each season would force the user to relearn the diary. Stable geometry creates continuity; changing the two source pigments makes the passage of seasons tangible.

### Strengths

- More nuanced than a fixed set of swatches
- Makes every daily choice feel personal without requiring artistic skill
- Gives each season a distinct visual identity
- Connects daily use directly to the seasonal-art premise
- Produces structured coordinates and a pigment sample for the art system
- Avoids a generic mood list

### Risks

- An unexplained field may feel arbitrary.
- Continuous choice can cause hesitation or false precision.
- Seasonal colors may change a user’s interpretation of the same coordinate.
- Dragging and color-only feedback are inaccessible.
- Rich gradients can become visually muddy or reduce marker contrast.

### Response to the risks

- Use one tap as a complete choice; dragging is optional.
- Quantize the field internally into a manageable grid while rendering it smoothly.
- Provide a short introduction to the dimensions, then let the ritual become intuitive.
- Give every sampled point a sensory description and non-color pattern or material quality.
- Offer an equivalent two-control or stepped-grid interaction for assistive technologies.
- Use a marker with adaptive light or dark contrast and a strong boundary.

## Recommended Direction

Prototype the Seasonal Color Field as the primary direction. Keep the Emotional Palette and Tone and Undertone concepts as lower-complexity fallbacks if the field creates hesitation or lacks emotional meaning in testing.

### Proposed flow

1. Ask, “Where are you today?” or “What color does today leave behind?”
2. Present the current season’s two-dimensional field.
3. Let one tap make a valid selection.
4. Allow optional drag refinement.
5. Separate the sampled pigment into a daily mark.
6. Offer a short note.
7. Save the mark without showing an artwork preview.

### Why this fits the product

- The season is present every day, not only at the final reveal.
- The interaction remains calm and nonverbal.
- A stable emotional space provides continuity across changing palettes.
- The selected pigment becomes direct material for seasonal art.
- The act feels closer to choosing and preserving pigment than completing a survey.

## Proposed Screen Behavior

### Resting state

The field occupies the central portion of the diary with enough surrounding space to feel like a material surface rather than a technical color picker. It begins without a cursor or default value so the app does not imply how the user feels.

Subtle material texture may vary by season. Texture cannot interfere with legibility, pointer contrast, or the ability to distinguish regions.

### Selected state

A tap places a high-contrast sample marker and lifts an enlarged pigment sample above the touch point. The sample receives a concise sensory description without being assigned an emotion.

The user can keep it immediately. Fine adjustment is available but never required.

### Accessible adjustment state

The same selection can be expressed through two discrete dimensions. VoiceOver can expose each as an adjustable control, while Voice Control, Switch Control, and keyboard users can move through defined steps.

The interface announces the resulting material description and selected state after adjustment without repeatedly interrupting exploration.

### Writing transition

The chosen sample reduces into a small material mark above the optional note. The field recedes but remains available through an Adjust action.

### Calendar mark

Each recorded day receives a mark based on its sampled pigment and quantized position. A distinct symbol or texture also communicates recorded state. Accessible Calendar descriptions include the stable dimensional qualities and seasonal pigment description.

## Relationship to Seasonal Art

The selected colors are creative ingredients, not psychological diagnoses.

Potential mappings include:

- Coordinate distribution influences compositional balance.
- Sampled pigments influence palette weighting.
- Movement through the field over time influences rhythm and placement.
- Blank days create no inferred mood value.
- Optional gesture may later influence line or texture.
- Optional text may contribute themes through a separate, disclosed process.

The seasonal artwork should not simply display a pie chart of color frequency. Its composition needs a designed transformation system so the result feels authored and surprising while remaining connected to the recorded material.

## Personal Meaning Versus Fixed Meaning

### Fixed emotional labels

Assigning “happy,” “sad,” or “angry” to pigments makes analytics easier but recreates a generic mood tracker in visual form.

### Entirely personal meaning

Letting every color mean anything preserves ambiguity but may reduce recall and accessibility.

### Recommended balance

Keep the emotional meaning personal while giving each swatch a stable sensory description. The visible interface can remain primarily visual. Accessibility labels and an optional detail view can describe qualities such as hue, lightness, warmth, and texture without claiming an emotion.

Later research can test whether users want to privately name what individual pigments mean to them. Personal definitions should never be required during onboarding.

## Accessibility Requirements

- Tapping anywhere in the field makes a complete selection; precise dragging is optional.
- The sample marker has a minimum 44-by-44-point interactive region and adapts its contrast to the underlying pigment.
- A stepped grid or two adjustable controls provide equivalent access to the stable dimensions.
- Every sampled region has a speakable sensory description and selected state.
- Pattern, material quality, marker state, and text supplement color.
- Color-vision simulations are included in visual testing for every seasonal palette.
- VoiceOver, Voice Control, Switch Control, and Full Keyboard Access can select, adjust, reset, and confirm the sample.
- Motion is supplemental; Reduce Motion uses static material changes.
- Increased Contrast and Reduce Transparency preserve field and marker boundaries.
- Large Dynamic Type does not compress the field below a usable size or hide adjustment and confirmation controls.

## Prototype Plan

Test the Seasonal Color Field against one discrete fallback.

### Variant 1: seasonal field

- Stable two-dimensional geometry
- One season-specific pigment pair
- Tap to select and optional drag to refine
- Optional note

### Variant 2: seasonal swatches

- Eight samples taken from the same seasonal pigment pair
- One tap to select
- Optional note
- Lower-complexity comparison

Evaluate:

- Selection speed
- Emotional resonance
- Whether users choose based on feeling or visual preference alone
- Whether choices feel meaningfully different across several days
- Whether users understand what movement across the field changes
- Whether stable geometry creates continuity when the seasonal pigments change
- Whether users can understand past entries without fixed mood labels
- Whether the field adds nuance or merely adds hesitation
- Whether the interaction remains usable without relying on color perception
- Whether light and dark palette variants preserve the identity of the same selected coordinate

Begin with one seasonal palette before designing all four. The prototype should isolate whether locating a point in a field is a strong daily language.

## Open Decisions

- Whether pigment relationship and depth provide enough emotional range without explicit emotional axes
- Continuous selection versus a visibly discrete grid
- Internal grid resolution
- Exact seasonal pigment pairs and material medium
- Whether pigment and depth labels are always visible or introduced once
- Whether sampled points have visible sensory descriptions
- Whether users can privately name sampled regions later
- Whether the question references color directly or remains more open
- How field coordinates appear in the Calendar beyond color
- How the field transitions at a seasonal boundary
- How hemisphere and local season are determined
- Whether gesture becomes a later optional dimension

## Current Recommendation

Move forward with a season-specific two-dimensional color field defined by two pigments. Blend between the pigments horizontally and move from airy to deep vertically. One tap must be sufficient, adjustment must be optional, and an equivalent discrete interaction must exist beyond color and dragging.

This direction makes the seasons present in everyday use without revealing the final artwork. It should be validated with one seasonal palette before the remaining palettes, textures, and transitions are designed.
