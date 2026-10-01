# Daily page rebuild

## Status and purpose

2026-10-01. User-authorized interactive design prototype, not production implementation. Replaces the rejected overlapping daily-page study. Preserve the accepted history-grid visual language and integrate it into a coherent daily notebook page.

## Revision — 2026-10-01

Owner requested a one-dimensional gradient slider, history near the top, and a more connected composition. This supersedes the earlier two-dimensional selector study. The revised hierarchy is date → compact history → quotation → shade slider → optional note → one save status.

Acceptance checklist for this revision:

- [x] One native shade slider has verified pointer and keyboard paths; visible thumb is neutral until the user chooses. Physical touch-device verification remains deferred.
- [x] Gradient, thumb and saved day share the same one-dimensional colour mapping.
- [x] History sits directly below the date; shorten the inline sample range to July–September to improve daily-cell readability. This range is a review proposal, not a production decision.
- [x] Writing grows with content, has no resize handle, and remains close to the slider and save status.
- [x] Inspect initial, note-only, saving, saved, edited, long-note, empty/sparse history and larger-text states at 320/390/430 points on both hosts.
- [x] Only the sample day updates; exact colours, keyboard endpoints, reload reset, overflow and browser errors are checked.

The existing autosave simulation, sample quotation, privacy boundary and white notebook treatment remain unchanged. The visible neutral thumb indicates an available control, not a selected or saved colour.

## Confirmed requirements

- White notebook with softly curved edges and one red margin; no horizontal ruling.
- SF Pro/system text, Baskerville Italic only for the short quotation.
- Date, optional city, compact colour selection, optional unlabelled note, and separate compact history.
- Exact note placeholder: “A thought, a fragment, a detail…”
- History preserves seven weekday rows, aligned months, seasonal saved colours, neutral unrecorded/future dates, and no scores or streaks.
- Preserve the accepted history snapshot's palette, square cells, restrained heading and date range.
- Only one colour selector occupies the page. No duplicate swatches or mood names.

## Proposed details for this review

- One-dimensional shade slider is owner-selected for this revision, using the existing autumn anchors. Earlier selector alternatives remain historical explorations.
- No emotional prompt: a functional accessible field label introduces colour selection without inventing mood meanings.
- Quiet autosave after a selection or edit settles; simulated in memory only. Reload resets the demo. This is not approval of production saving behavior.
- A fixed sample date of 19 September 2026 carries forward the accepted history snapshot; city omitted because optional.
- July–September inline history is proposed for readability; the final history range remains a product decision.

## Hierarchy and flow

Date → recent history → short quotation → shade slider → optional note → one save status. Initial state has a neutral thumb, no selected colour, and an empty current-day cell. Tap, slide or keyboard-select a colour; optionally write; after the debounce, only the current-day cell changes. Subsequent edits replace that day's data. History is a view, never a selector. No calendar navigation, new screen, animation, or page-turn metaphor is introduced.

## Data and privacy

Synthetic history and one draft contain a date, a normalized slider position, canonical RGB colour, and optional note. The gradient and saved colour use the same interpolation. Nothing is persisted or transmitted. No backend, analytics, model, or location permission is used. The demo notice is outside the product page.

## States

- Empty: neutral slider thumb, neutral current-day cell, no saved claim.
- Partial: note without a colour remains a draft; history does not change.
- Selected/saving: marker and one saving status; history retains its previous saved state until the timer completes.
- Saved/edit: exact colour applied to the current date, one saved status; later edits update the same entry.
- Loading/error/offline: no remote resources or persistence in this scoped demo. Production recovery, durable drafts, and loading/failure behavior remain required in the colour-selection brief, not simulated as functioning storage here.
- Empty/sparse history: sample-data fixtures cover these states without changing the component hierarchy.

## Layout and accessibility

One column, natural page height, no fixed-position controls or clipping. Notebook remains white against light and dark hosts. At 320/390/430 points, month labels remain 12px and controls at least 14px; note uses 16px. Cells and gaps adapt to available width without horizontal scrolling.

The native range input has a 44px target, visible keyboard focus, a descriptive label and selected-colour value text. Arrow, Home and End keys provide an equivalent selection path. The note grows naturally with content. History has a textual summary and current-date saved state. No motion is required. Native Dynamic Type and VoiceOver validation remain deferred until platform implementation.

## Previous revision checks (superseded; not evidence for this revision)

- [x] Visually inspect initial, partial, selected/saving, saved, edited, expanded accessible controls, empty and sparse history at 320/390/430 and both host appearances.
- [x] No overlap, clipped text, duplicate selector, decorative paper stack, or unbalanced blank region.
- [x] Note and history are visibly separate from colour selection.
- [x] History palette, cells, month alignment and typography match the accepted direction; narrow widths adapt cells without clipping labels.
- [x] Tap, drag, note entry, range keys, and disclosure work; controls update only intended data.
- [x] Saving and re-saving alter only the sample date's cell, with the exact selected RGB colour; no selection exists initially.
- [x] Note-only draft does not fill history; reload resets the demo.
- [x] Inspect larger text and reduced-motion settings; record limits honestly.

## Open decisions

Save boundary, history range and functional label wording remain proposals. Platform and production persistence remain unapproved. This rebuild does not settle seasonal emotional profiles or photograph matching.

## Verification record

Previous two-dimensional study: [archived review](../design/reviews/daily-page-2026-10-01/REVIEW.md). Current slider study: [rendered review and evidence](../design/reviews/daily-slider-2026-10-01/REVIEW.md). All 60 scoped renders and automated interaction checks passed; native accessibility and physical touch-device testing remain unverified.
