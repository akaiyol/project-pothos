# Glass diary review — 2026-10-01

## Scope

Raised, cloudy, colourless glass replaces the notebook material. Original sample stickers move behind a lower compartment; existing diary controls stay visible and directly usable. The notebook prototype is preserved separately. The material uses layered CSS blur, highlights and shadows: it is an optical approximation, not physically accurate refraction.

## Correction during review

The first unrestricted sticker pass failed: decorations behind the history could look like diary colours and overlapped text. The brief was explicitly revised to propose a lower bounded compartment. Also separated preview control rows at enlarged text. All captures were regenerated after these corrections.

## Evidence

- verify.cjs passed in Chromium and WebKit: 72 captures per engine, covering initial, note draft, saving/saved, details, past readback, long/cleared note, empty/sparse history and 200% text.
- motion.cjs passed in both engines: 42 captures each, covering settled, tilted, paused, unavailable sensor, simulated orientation, reduced motion and increased contrast.
- All capture sets use 320/390/430 widths and both host appearances. Diary checks cover exact RGB, single-day updates, typing, endpoints, direct midpoint selection, dragging, emulated touch, overflow and script errors. Motion checks cover preview keyboard/drag, fixed content geometry, paused/static pixel stability and denied/unavailable input fallbacks.
- Primary reviewer inspected Chromium 390 diary and motion sheets. Continued reviewers inspected Chromium 320/430 and all WebKit sheets.

Physical iPhone sensor permission, actual tilt behavior, VoiceOver and native Dynamic Type remain unverified. The contrast fallback also uses the same opaque surface rule as reduced transparency, but the reduced-transparency media query was not independently emulated. No external dependencies, network transfer or durable data storage were introduced.

## Review choices

Glass cloudiness/bevel, sample sticker artwork, lower compartment and motion strength remain proposals. The technology metaphor is intentionally unresolved. Tests do not imply owner approval of visual direction.

Final localized correction: dark preview focus outline changed to light grey; all six affected dark tilted captures were regenerated and inspected in both engines. WebKit renders sticker details sharper than Chromium; material matching on a physical phone remains a follow-up.
