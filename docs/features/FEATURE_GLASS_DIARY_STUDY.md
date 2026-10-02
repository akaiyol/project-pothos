# Glass diary interactive study

## Scope and authorization

2026-10-01: owner authorized an interactive mockup based on the existing direct-access diary, adding the raised glass and orientation-responsive stickers described in [the direction](../design/GLASS_DIARY_DIRECTION.md). This is a prototype, not production implementation or a platform decision.

## Confirmed requirements

Replace paper with one raised, rounded, slightly cloudy and colourless glass slab with a small outer margin. Put loose stickers behind it that fall and respond to phone orientation. Preserve visible top history, direct gradient selection, note writing, save feedback and secondary historical-entry readback. Keep the technology metaphor unresolved. Modern, assertive visual character; no extra steps for diary entry.

## 2026-10-02 revision: stars and reflective glass

Owner-confirmed: use stars only for MVP stickers. A later direction may mix shapes and materials; that expansion is outside the MVP. Current work remains a mockup, with no extra product features or production implementation.

Owner-requested exploration: orientation should affect both the stars behind the slate and subtle coloured reflections on the glass. Purple and blue are candidate hues, not a fixed palette. This supersedes the earlier prohibition on any glass colour: the base remains neutral, while angle-dependent reflections may carry colour.

Proposed refinement: thinner single bevel, less uniform haze, clearer star silhouettes, breathing room around settled stars, and a broad faint reflection that moves independently of the stars. Keep text, controls and history stable and sharp; suppress reflections over colour-critical history cells. Star count, finish, reflection strength and motion tuning remain review choices. Do not add sticker picking, uploads, navigation or other product features.

### Revision acceptance checklist — not yet verified

- [ ] Only star silhouettes appear as MVP stickers behind the glass.
- [ ] Initial, tilted and settled states communicate separate background, star, glass and content layers.
- [ ] Tilt changes both star position/rotation and glass reflection; returning to level lets motion settle.
- [ ] Reflection hue is subtle and angle-dependent; diary colours and reading remain clear.
- [ ] Inspect every affected state at 320/390/430 in supported appearances, including paused, reduced-motion and motion-unavailable fallbacks.
- [ ] Verify preview interactions and distinguish simulated tilt from physical phone verification.

Earlier checked criteria below apply to the previous study only and do not establish acceptance of this revision. See [the delivery roadmap](../design/ROADMAP.md#glass-diary-mvp-delivery-roadmap) for Figma and development gates.

## Proposed study choices

- Neutral silver environment, edge bevel/reflection, translucent cloudy centre and layered shadows. CSS optical approximation for this first material study, not a physically accurate ray-traced glass renderer.
- Superseded sample sticker artwork from the earlier study: chrome star, blue disc, orange oval and violet geometric label. Decorative only, no implied emotional meanings or product rewards.
- A canvas layer beneath the glass uses gravity, collision separation and damping. Desktop users drag unused glass space to tilt; a labelled preview tilt slider supplies a keyboard equivalent. Phone motion is optional through an explicit enable button where supported; unavailable/denied motion leaves the preview slider functional.
- Sharp system type and controls remain above the material. Existing quote wording is retained in restrained system type for this exploration.
- Review correction: confine stickers to the lower glass compartment below the entry status. Earlier unrestricted motion visually contaminated history colours and overlapped text. The bounded compartment preserves motion and material depth without changing diary data perception.

## Visual plan

Palette: graphite #202328, secondary ink #555c65, silver background #cbd0d6, white highlights #ffffff, sticker blue #485dea and orange #ff743d. Glass has no pigment; colour comes from objects behind it. Existing diary colour values remain unchanged.

System/SF type: 28px date, 16px writing, 13–14px supporting controls. Left-aligned date → history → quote → shade → writing, in one continuous inset slab. The material and stickers are the only decorative focus; no red margin, nested cards, neon trim or new navigation. This replaces the notebook metaphor rather than dressing it with glass buttons.

## Data, privacy and states

Reuse synthetic dated entries and exact colour mapping. No persistence, network calls or user uploads. Orientation is transient local input and is neither logged nor transmitted. Empty/sparse history, note-only draft, saving/saved, history readback and long/cleared notes remain supported. Motion has supported, active, denied/unavailable and paused states. Glass falls back to a more opaque material when transparency/contrast preferences require it. Reduced motion starts with static stickers; diary controls are unaffected.

## Acceptance checklist

- [x] Initial history, slider and note remain visible, with one direct shade-selection path and exact saved cell colour.
- [x] Glass appears raised and slightly cloudy, keeps a visible screen inset and replaces the red paper margin.
- [x] Stickers are visibly behind glass, settle within bounds and respond to preview tilt without shifting diary UI or intercepting controls.
- [x] Pointer and keyboard preview controls work; optional orientation permission failures are handled without blocking entry.
- [x] Reduced motion uses static artwork; pause stops animation; contrast/transparency fallbacks remain usable.
- [x] Inspect real renders at 320/390/430 in light/dark hosts, initial/settled/tilted/paused, all entry/detail states, 200% text and accessibility fallbacks.
- [x] Verify Chromium/WebKit interactions and distinguish simulated orientation from physical-device verification.

## Open decisions and handoff

Owner to judge the material, sample sticker direction and motion strength. Exact technology metaphor, sticker ownership/source and production platform remain unresolved. Next step after review: refine this material study, then carry the accepted surface into the mapped/Figma journey. Physical phone sensor behavior and durable storage remain outside desktop verification.

Evidence: [rendered review](../design/reviews/daily-glass-2026-10-01/REVIEW.md). Reduced-transparency uses the tested opaque contrast rule but its media query was not separately emulated. Physical sensor and native accessibility verification remain deferred.
