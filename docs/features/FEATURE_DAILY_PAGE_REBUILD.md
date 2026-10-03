> Historical brief as of 2026-10-03. Retained component/material evidence; conflicting requirements are superseded by the [seasonal ecosystem brief](FEATURE_SEASONAL_ECOSYSTEM.md). Existing visual approvals apply only to the earlier study.

# Daily page rebuild

## Status and purpose

2026-10-01. User-authorized interactive design prototype, not production implementation. Replaces the rejected overlapping daily-page study. Preserve the accepted history-grid visual language and integrate it into a coherent daily notebook page.

## Direct-access correction — 2026-10-01

Latest owner feedback supersedes the disclosure proposal below: minimalism must not conceal core features or add unnecessary steps. The previous review checked layout and interaction mechanics but incorrectly accepted hidden core controls.

Confirmed: history remains visible near the top; the gradient slider and optional writing are visible on first render. Selecting a shade directly updates the sample entry, without opening a panel or confirming a second time. Only secondary date lookup and entry readback are disclosed. Preserve notebook styling, quotation, sample data and accessible native controls.

Proposed: retain the three-month sample range and in-memory autosave. An unselected neutral thumb becomes coloured on direct interaction. Pointer release or Enter/Space can select the initial midpoint; arrow keys select normally. No durable storage or production behavior is introduced.

Acceptance checklist:

- [x] Initial history, shade slider and note are visible without interaction; no colour disclosure or confirmation button exists.
- [x] Tap, drag and keyboard select directly; only today's cell updates with the exact shade, including unchanged midpoint selection.
- [x] Secondary entry details disclose independently and show the saved colour and note; note-only drafts remain unsaved.
- [x] Long/cleared notes, empty/sparse history, saving/saved states, focus and 200% text remain usable.
- [x] Inspect rendered output at 320, 390 and 430 in both host appearances; verify responsive overflow and browser errors.

Evidence: [direct-access rendered review](../design/reviews/daily-direct-2026-10-01/REVIEW.md).

## Rejected minimal interaction revision — 2026-10-01

Owner authorized the review improvements and requested minimal visible detail, with simple clicks revealing secondary information. The owner-selected notebook, shade slider and top history remain the basis. This revision supersedes the always-expanded history and slider shown below.

### Confirmed intent and proposed mechanics

- Keep the date prominent and history reachable beside it. A clearly labelled History disclosure reveals the calendar inline; it begins collapsed to remove competing detail.
- Group the quotation, colour choice and writing into one daily-entry area. No new screen, navigation, animation or decorative treatment.
- A Choose colour disclosure reveals the single gradient slider. Opening previews the midpoint without selecting or saving it. Use shade explicitly accepts the preview and closes the control; dismissing without acceptance cancels it. This removes the ambiguous unselected midpoint and gives pointer and keyboard users the same confirmation path.
- After acceptance, the same disclosure shows the chosen swatch and Change colour. The swatch is hidden while the editor is open, leaving one active colour control.
- Colour acceptance triggers the existing simulated save. Subsequent note edits autosave only after a colour has been accepted. This confirmation boundary is a prototype proposal; production saving remains unapproved.
- History reveals month labels and the seven-row grid. Season and weekday annotation are omitted to reduce clutter; exact calendar dates remain available through a labelled date picker and text description within expanded history. This adds an accessible equivalent to the visual data, without making tiny cells touch targets.
- Stored sample records include colour and optional note in memory. Readback appears only in expanded history. No persistence or transmission; reload resets the prototype.
- Literal colour descriptions replace raw RGB announcements; they never name emotions. Existing July–September range remains a review proposal.

### Acceptance checklist

- [x] Initial page clearly offers History, Choose colour and optional writing without instructions or hidden required controls.
- [x] History and colour disclosures open and close with pointer and keyboard; hidden content has no layout footprint or focusable controls.
- [x] Opening or cancelling colour does not create an entry. Use shade accepts the unchanged midpoint equally via pointer and keyboard.
- [x] Preview changes do not save until accepted; latest accepted colour and note survive rapid edits in the simulated record; only today's history cell changes.
- [x] Exact gradient/thumb/saved-cell mapping; keyboard endpoints; clearing and shrinking notes; accessible date and colour/note readback.
- [x] Visually inspect initial, disclosures, preview, saving, saved, history readback, empty/sparse history, long/cleared note, focus and 200% text at 320/390/430 and both host appearances.
- [x] Test touch emulation and WebKit where available; distinguish these from physical iOS/VoiceOver/Dynamic Type and onscreen keyboard verification.

Native-device accessibility and real durable saving remain outside this HTML prototype. All historical checklists below describe earlier revisions only.

Current evidence: [minimal-page rendered review](../design/reviews/daily-minimal-2026-10-01/REVIEW.md). All 180 captures passed visual inspection; both browser test runs passed.

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
