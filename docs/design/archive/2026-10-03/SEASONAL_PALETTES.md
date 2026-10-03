> Historical specification, superseded on 2026-10-03. See [current direction](../../APP_DESIGN.md). Retained for chronology, not current requirements.

# Seasonal Color System

## Document Status

- Feature: seasonal color field
- Product stage: art-direction exploration
- Last updated: 2026-09-27
- Status: two-anchor proposal; colors and selector rendering are not final
- Related exploration: [MOOD_INPUT.md](MOOD_INPUT.md)
- Daily selection feature: [../features/FEATURE_DAILY_COLOR_SELECTION.md](../../../features/FEATURE_DAILY_COLOR_SELECTION.md)

## Current Interface Revision — 2026-09-27

The seasonal names below remain useful internal art-direction language, but they are not visible labels in the daily selector. The interface does not name a chosen color or translate it into mood language.

The current mapping proposal preserves a normalized two-dimensional position, its season, its palette version, and a canonical resolved color. This allows the same interaction to work throughout the year without silently recoloring past diary entries when a working palette is revised. The exact relationship between canonical, light-mode, and dark-mode saved colors remains an open design decision.

This revision supersedes later references in this document to visible pigment names and sensory descriptions.

## Direction

Each season is defined by a relationship between two pigments. The field blends horizontally between them and varies vertically from airy to deep.

This is more disciplined than a multicolor gradient:

- Seasonal identity becomes immediate and memorable.
- Every point in the field still has nuance through mixing and depth.
- The daily interaction feels like sampling pigment rather than using a technical color picker.
- Seasonal artwork receives a coherent color constraint rather than an unrestricted palette.

The two pigments should feel related to the season without becoming a literal holiday or weather theme.

## Shared Product Neutrals

| Role | Working name | Color | Purpose |
| --- | --- | --- | --- |
| Light surface | Unbleached paper | `#F3EFE7` | Airy end of the field and primary light surface |
| Dark surface | Night paper | `#1D201F` | Deep end of the field and primary dark surface |
| Light text | Carbon ink | `#25231F` | Primary text on light surfaces |
| Dark text | Chalk | `#ECE8DF` | Primary text on dark surfaces |

Paper and ink shape the tint and depth of the field but are not treated as additional seasonal pigments.

## Appearance Strategy

Light and dark interfaces need separate tonal variants of the same pigments.

- Light-mode anchors are pastel, supporting the feeling of pigment on pale paper. They receive very little additional whitening inside the field so they remain visible rather than washed out.
- Dark-mode anchors are richer and more luminous so they retain presence against Night Paper.
- Hue identity and pigment names remain consistent between modes.
- The diary stores the selected season and field coordinates, not the appearance-specific hex value.
- Switching appearance re-renders the same selection through the corresponding palette variant; it does not change the recorded emotional position.
- Seasonal artwork uses its own canonical art palette and must not depend on the interface appearance active when an entry was created.

This creates visual adaptation without maintaining two different emotional systems.

## Field Geometry

- Horizontal axis: seasonal pigment A to seasonal pigment B
- Vertical axis: airy to deep

| Position | Result |
| --- | --- |
| Top left | Airy tint of pigment A |
| Top right | Airy tint of pigment B |
| Bottom left | Deep shade of pigment A |
| Bottom right | Deep shade of pigment B |
| Center | A balanced mixture of both pigments at medium depth |

The horizontal axis intentionally has no fixed emotional label. The user chooses the hue relationship intuitively. The vertical axis describes pigment presence rather than emotional intensity, avoiding a hidden good-to-bad scale.

## Proposed Seasonal Pairs

| Season | Pigments | Light palette | Dark palette | Relationship |
| --- | --- | --- | --- | --- |
| Spring | Peony + Pea leaf | `#E8A8B6` + `#C4D99A` | `#D97990` + `#A8C779` | Blossom and emergence |
| Summer | Sunstone + Baby sky | `#F2D58A` + `#B9DCEC` | `#E1AD3F` + `#91C6D8` | Heat and open air |
| Autumn | Red persimmon + Damson | `#E99A7D` + `#B58AA1` | `#CA613F` + `#68405A` | Dry warmth and ripened depth |
| Winter | Frost blue + Soft mulberry ink | `#CFE1E7` + `#BA8499` | `#A9C7CF` + `#91536B` | Exterior quiet and interior color |

The working pairs form a broader yearly rhythm:

- Spring: pink and green
- Summer: yellow and blue
- Autumn: orange and purple
- Winter: pale blue and dark berry

They are related enough to feel like one product but distinct enough that a saved mark carries seasonal context.

## Spring: Peony and Pea Leaf

Spring should feel tender, wet, and newly alive rather than generically pastel.

- Peony introduces bloom, softness, vulnerability, and warmth.
- Pea leaf introduces tender growth, new shoots, softness, and return.
- Their center mixture will naturally mute, creating an important neutral territory between bloom and foliage.

The pastel pea green should stay yellow-leaning rather than mint. The pink should retain enough pigment to avoid a cosmetic or confectionery character.

## Summer: Sunstone and Baby Sky

Summer should hold exposure and depth at the same time.

- Sunstone introduces heat, long light, dryness, and energy.
- Baby sky introduces clear air, open water, softness, and distance.
- Their mixture can produce pale mineral green and weathered coastal territory.

The yellow should lean ochre rather than lemon. The blue should feel airy and soft without becoming gray or overly sweet.

## Autumn: Red Persimmon and Damson

Autumn should feel mature, dry, layered, and concentrated rather than decorative or holiday-themed.

- Red persimmon introduces ripeness, leaf pigment, clay, and low sun with slightly more ember-red than orange.
- Damson introduces fruit skin, shadow, wine, and cooling evenings.
- Their mixture creates rust, earth, and brown-purple territory without requiring a separate brown anchor.

The orange should avoid pumpkin brightness. The purple should remain warm and organic rather than jewel-toned.

## Winter: Frost Blue and Soft Mulberry Ink

Winter should feel quiet and crystalline while retaining interior warmth and life.

- Frost blue introduces pale sky, ice, breath, and open quiet.
- Soft mulberry ink introduces berries, interior warmth, long nights, and inward intensity without becoming nearly black.
- Their mixture creates slate, mauve, and blue-violet territory.

Avoid a red and green pair, which would make the field feel tied to one holiday tradition. Avoid an entirely blue field, which would equate winter with sadness.

## Field Construction

The field should look continuous but remain computationally stable.

1. Blend horizontally between the two seasonal pigments.
2. Mix the upper region toward Unbleached Paper.
3. Mix the lower region toward Carbon Ink or a deep shade derived from the pigments.
4. Preserve the two pigments’ chromatic identity through the middle.
5. Quantize selections internally even if the surface renders smoothly.

Direct RGB blending may create muddy centers, especially between spring pink and green. Prototype using a perceptual color space and compare it with a deliberately pigment-like subtractive mix. A muted center can be valuable, but it should feel intentional rather than digitally gray.

## Daily Interaction Implications

- The field starts with no selected point.
- One tap is a complete choice.
- Horizontal movement changes the pigment relationship.
- Vertical movement changes pigment depth.
- The selected sample receives a sensory description based on both source pigments and depth.
- Saved entries retain their season and normalized field coordinates when the season or interface appearance changes.

The dimensions remain mechanically consistent even though the horizontal pigment names change with the season.

## Seasonal Transition

The two-pigment relationship should be introduced as part of opening a new season.

1. The closing field remains unchanged through the final diary entry and artwork generation.
2. The next diary page reveals the new pair together.
3. The field demonstrates its airy and deep ranges without assigning emotional meanings.
4. The user makes the first sample normally.

Do not gradually blend one seasonal pair into the next. Stable color relationships make entries reproducible and give each season a distinct chapter.

## Accessibility and Legibility

- The field must have a discrete alternative that does not require color perception or precise dragging.
- A selected point is described by source relationship and depth, such as “mostly Peony, medium depth.”
- The sampling marker uses an adaptive light and dark boundary.
- Calendar marks include a recorded-state symbol and may add pattern or position information.
- Color-vision simulations are tested for all four pairs and their intermediate mixtures.
- Seasonal colors should not be used for text or essential controls unless contrast is verified against the actual surface.
- Pigment names are unique and speakable for Voice Control.

## Questions to Resolve

- Are these four pigment pairs emotionally broad enough?
- Does the spring midpoint become intentionally earthy or unpleasantly muddy?
- Should airy to deep change only lightness, or both lightness and saturation?
- Does the horizontal axis need visible pigment names after onboarding?
- Should the field interpolate smoothly or retain faint zones of recognizable pigment?
- Is watercolor, ink, pastel, dyed fiber, or printmaking the right material treatment?
- Should palettes adapt to hemisphere only, or also climate and cultural context?
- How should users browse entries from different seasonal color systems together?
- Does changing appearance preserve the perceived identity of a saved sample closely enough?
- Do the light-mode pastels remain deliberate and legible without becoming a generic wellness palette?

## Current Recommendation

Start by prototyping Spring with Peony and Pea Leaf in both appearance variants. It directly reflects the proposed pink-and-green relationship and presents the hardest interpolation problem. If its middle territory remains expressive and the same coordinate feels related across light and dark modes, the remaining seasonal pairs can follow.

The colors above are working anchors. Their relationship and tonal behavior matter more at this stage than final hex precision.
