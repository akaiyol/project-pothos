# Daily page rebuild

## Status and purpose

2026-10-01. User-authorized interactive design prototype, not production implementation. Replaces the rejected overlapping daily-page study. Preserve the accepted history-grid visual language and integrate it into a coherent daily notebook page.

## Confirmed requirements

- White notebook with softly curved edges and one red margin; no horizontal ruling.
- SF Pro/system text, Baskerville Italic only for the short quotation.
- Date, optional city, compact colour selection, optional unlabelled note, and separate compact history.
- Exact note placeholder: “A thought, a fragment, a detail…”
- History preserves seven weekday rows, aligned months, seasonal saved colours, neutral unrecorded/future dates, and no scores or streaks.
- Preserve the accepted history snapshot's palette, square cells, restrained heading and date range.
- Only one colour selector occupies the page. No duplicate swatches or mood names.

## Proposed details for this review

- Continuous selector only, using the history snapshot's autumn anchors. Other selector directions remain unresolved in their existing brief and are not selectable in this page study.
- No emotional prompt: a functional accessible field label introduces colour selection without inventing mood meanings.
- Quiet autosave after a selection or edit settles; simulated in memory only. Reload resets the demo. This is not approval of production saving behavior.
- A fixed sample date of 19 September 2026 aligns with the accepted April–October history snapshot; city omitted because optional.
- Retain the long history range and fit its grid at every required width. Range remains a product decision.

## Hierarchy and flow

Date → short quotation → colour field → optional note → one save status → recent pages history. Initial state has no selection and an empty current-day cell. Tap or keyboard-select a colour; optionally write; after the debounce, only the current-day cell changes. Subsequent edits replace that day's data. History is a view, never a selector. No calendar navigation, new screen, animation, or page-turn metaphor is introduced.

## Data and privacy

Synthetic history and one draft contain a date, normalized coordinates, canonical RGB colour, and optional note. The gradient and saved colour use the same interpolation. Nothing is persisted or transmitted. No backend, analytics, model, or location permission is used. The demo notice is outside the product page.

## States

- Empty: no marker, neutral current-day cell, no saved claim.
- Partial: note without a colour remains a draft; history does not change.
- Selected/saving: marker and one saving status; history retains its previous saved state until the timer completes.
- Saved/edit: exact colour applied to the current date, one saved status; later edits update the same entry.
- Loading/error/offline: no remote resources or persistence in this scoped demo. Production recovery, durable drafts, and loading/failure behavior remain required in the colour-selection brief, not simulated as functioning storage here.
- Empty/sparse history: sample-data fixtures cover these states without changing the component hierarchy.

## Layout and accessibility

One column, natural page height, no fixed-position controls or clipping. Notebook remains white against light and dark hosts. At 320/390/430 points, month labels remain 12px and controls at least 14px; note uses 16px. Cells and gaps adapt to available width without horizontal scrolling.

The field is a group with two range inputs as an equivalent input path, exposed through “Adjust colour” disclosure. Coordinates describe horizontal/vertical position, not emotions. All controls have 44px targets, visible focus, and screen-reader labels. Selection works with a tap or drag, and range keys support assistive input. History includes a textual summary and current-date saved state. No motion is required; larger text must reflow without overlap, with history retaining its week layout. Native Dynamic Type/VoiceOver validation is deferred until platform implementation.

## Acceptance checklist

- [x] Visually inspect initial, partial, selected/saving, saved, edited, expanded accessible controls, empty and sparse history at 320/390/430 and both host appearances.
- [x] No overlap, clipped text, duplicate selector, decorative paper stack, or unbalanced blank region.
- [x] Note and history are visibly separate from colour selection.
- [x] History palette, cells, month alignment and typography match the accepted direction; narrow widths adapt cells without clipping labels.
- [x] Tap, drag, note entry, range keys, and disclosure work; controls update only intended data.
- [x] Saving and re-saving alter only the sample date's cell, with the exact selected RGB colour; no selection exists initially.
- [x] Note-only draft does not fill history; reload resets the demo.
- [x] Inspect larger text and reduced-motion settings; record limits honestly.

## Open decisions

Selector form, save boundary, history range and functional label wording remain proposals. Platform and production persistence remain unapproved. This rebuild does not settle seasonal emotional profiles or photograph matching.

## Verification record

See the [rendered review and evidence](../design/reviews/daily-page-2026-10-01/REVIEW.md). Checked the scoped HTML prototype, not production storage or native accessibility.
