# Raised glass diary direction

Recorded 2026-10-01. Design direction and reference research only; no prototype or production implementation is authorized by this document. The owner requested documentation before implementation. Existing notebook prototype remains available as historical evidence.

## Owner-confirmed direction

- Replace the simple workbook/notebook base with a modern, three-dimensional piece of glass.
- One raised, rounded rectangular glass surface occupies most of the screen, with a small visible outer margin.
- Glass is colourless and slightly cloudy, with a convincing sense of physical depth.
- Stickers sit behind the glass. They fall and move in response to phone orientation.
- The object should evoke some form of technology; the specific reference is deliberately undecided.
- Preserve direct access to core diary features: minimalism must not hide the history, colour slider or writing behind unnecessary steps.

This supersedes the white-paper material and red notebook margin for the next visual exploration. It does not authorize removing diary functionality, choosing a platform or adding navigation.

## Purpose

Give the diary a contemporary, tactile identity while preserving a clear daily task. The glass and moving stickers should make the surface feel physical without competing with reading, colour selection or writing.

## Proposed visual model — not yet approved

Back to front: quiet background → loose sticker layer → raised glass slab → sharp diary text and controls.

Use a subtly rounded bevel, restrained edge highlights, background refraction and a soft separation shadow to communicate thickness. Apply light cloudiness to the background seen through the glass. Keep tint neutral; sticker colours may show through, but the glass itself has no chosen hue. Avoid heavy rainbow fringes, excessive glow or blur applied to text.

Propose bounded sticker motion with gentle collisions and settling. Exact depth, friction, bounce, quantity and boundaries require a motion study. Flat sticker artwork moving behind a 3D-looking slab does not inherently require a full 3D physics scene.

## Preserved information hierarchy

Date, compact history near the top, directly usable shade slider and optional writing remain accessible. Exact placement and quotation/typographic treatment should be evaluated in the new material, rather than silently removed or treated as finalized. The selected shade must still map exactly to the saved day's history cell; refraction must not distort that meaning.

## States and acceptance criteria for a future study

- First render communicates raised, slightly cloudy, colourless glass with a visible outer margin at 320, 390 and 430 points.
- History, slider and writing are visible without opening another control; decorative motion never gates diary use.
- Inspect empty, partial and populated history; draft, saving and saved entry states; long notes and enlarged text.
- Text and controls remain legible over every tested sticker position in light and dark surroundings. Stickers cannot intercept diary input.
- Demonstrate level, tilted and settled sticker states; changing orientation affects stickers without moving the diary controls.
- Proposed accessibility fallbacks: still stickers for Reduce Motion, a more opaque surface for Reduce Transparency/contrast needs, and a usable still composition when motion access is unavailable or denied.
- Motion loading/error states must not prevent diary entry. Any motion permission flow depends on the selected platform and must be verified before implementation.
- Proposed privacy boundary: orientation is transient on-device input, not stored or transmitted. Sticker source/import behavior remains undecided.
- Inspect rendered screenshots for every affected variant at required widths; test motion separately on a physical device before claiming phone-orientation behavior verified.

## Open decisions

- Technology/object metaphor: deliberately deferred by the owner.
- Sticker artwork, source, count, meaning and whether users can choose it.
- Whether stickers occupy the whole background or a bounded compartment behind the slab.
- Glass thickness, cloudiness, inset and how strongly stickers remain visible through it.
- Motion strength and whether it settles while writing.
- Treatment of the existing quotation and accent typography.
- Platform, rendering approach and durable saving remain unselected.

## Reference shortlist

Reviewed primary project documentation on 2026-10-01. These are inspiration sources, not selected dependencies or verified mobile implementations. Inspect exact licenses and target-device performance before reusing code or assets.

| Reference | What to study | Relevance and limit |
| --- | --- | --- |
| [Poimandres / Drei MeshTransmissionMaterial](https://drei.docs.pmnd.rs/shaders/mesh-transmission-material) · [GitHub](https://github.com/pmndrs/drei) | Thickness, refraction, roughness blur and transparent objects behind glass | Closest material reference for the raised slab. Documentation notes additional rendering cost; this does not establish phone performance. |
| [ybouane/liquidglass](https://github.com/ybouane/liquidglass) · [demo](https://liquid-glass.ybouane.com/) | Rounded glass panels, edge highlights, bevel depth, blur and shadows | Useful reference for placing readable UI on a glass panel. Dynamic background capture has documented cost; do not assume it suits continuous sticker movement. |
| [Matter.js](https://github.com/liabru/matter-js) · [examples](https://brm.io/matter-js/demo/) | Gravity, collisions and settling of flat objects | Relevant to loose sticker behavior. Mapping phone orientation into gravity is separate integration work. |
| [React Three Rapier](https://github.com/pmndrs/react-three-rapier) | Rigid-body physics in a React Three Fiber scene | Useful if actual 3D sticker depth becomes necessary; not a reason to choose a more complex implementation now. |
| [Codrops](https://github.com/codrops) | Creative interaction, WebGL and material experiments | A broader source of visual studies and source code. Assess individual demos and their licenses; avoid copying spectacle that undermines the daily task. |

Recommended research sequence: compare glass material references first, then study sticker motion separately. Combine them only after the surface is readable and the movement is calm. Keep the technology metaphor open as requested.

## Next action

Owner reviews the recorded direction and reference shortlist. No visual implementation in this change. A subsequent authorized study should establish the glass material and layer arrangement using sample artwork, then test sticker motion; artwork choices and containment must be specified before dependent implementation.
