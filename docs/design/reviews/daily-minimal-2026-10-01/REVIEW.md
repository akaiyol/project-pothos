# Minimal daily page review — 2026-10-01

## Revision

The initial page now prioritizes the date, existing quotation, colour action and optional writing. History opens inline beside the date. Choose colour reveals the single shade slider; Use shade accepts its preview and returns focus to the summary. Closing the disclosure cancels the preview. No colour swatch appears until acceptance.

History contains aligned month labels, seven day rows, a date picker and textual colour/note readback. The secondary season/weekday annotation is removed. Notes and colours are stored only in the page's simulated in-memory record; reload resets them.

The current [feature brief](../../../features/FEATURE_DAILY_PAGE_REBUILD.md) distinguishes the owner's minimalism/slider/top-history direction from the prototype's proposed confirmation boundary and history range.

## Verification coverage

Automated checks cover 15 states at 320/390/430 CSS-pixel widths, light/dark hosts, and two browser engines (Chromium and WebKit): 180 rendered captures total. Each engine also exercises touch emulation. This is isolated prototype verification, not control of the user's existing browser tab.

Sheet 1: initial, history, colour editor, uncommitted preview, saving. Sheet 2: saved, both disclosures, saved readback, long note, cleared note. Sheet 3: empty history, sparse history, note-only draft, 200% initial, 200% expanded.

| Engine / host | 320 | 390 | 430 |
| --- | --- | --- | --- |
| chromium / light | [1](chromium-light-320-1.png), [2](chromium-light-320-2.png), [3](chromium-light-320-3.png) | [1](chromium-light-390-1.png), [2](chromium-light-390-2.png), [3](chromium-light-390-3.png) | [1](chromium-light-430-1.png), [2](chromium-light-430-2.png), [3](chromium-light-430-3.png) |
| chromium / dark | [1](chromium-dark-320-1.png), [2](chromium-dark-320-2.png), [3](chromium-dark-320-3.png) | [1](chromium-dark-390-1.png), [2](chromium-dark-390-2.png), [3](chromium-dark-390-3.png) | [1](chromium-dark-430-1.png), [2](chromium-dark-430-2.png), [3](chromium-dark-430-3.png) |
| webkit / light | [1](webkit-light-320-1.png), [2](webkit-light-320-2.png), [3](webkit-light-320-3.png) | [1](webkit-light-390-1.png), [2](webkit-light-390-2.png), [3](webkit-light-390-3.png) | [1](webkit-light-430-1.png), [2](webkit-light-430-2.png), [3](webkit-light-430-3.png) |
| webkit / dark | [1](webkit-dark-320-1.png), [2](webkit-dark-320-2.png), [3](webkit-dark-320-3.png) | [1](webkit-dark-390-1.png), [2](webkit-dark-390-2.png), [3](webkit-dark-390-3.png) | [1](webkit-dark-430-1.png), [2](webkit-dark-430-2.png), [3](webkit-dark-430-3.png) |

Checks include fresh keyboard midpoint acceptance, preview cancellation, keyboard endpoints, pointer dragging, focus restoration, one-day isolation, exact saved RGB, debounced latest note, saved note readback, note clearing/shrinking, reload reset, hidden disclosures, horizontal overflow and script errors. Native date-picker hit bounds are checked to be at least 44 CSS pixels high.

Testing and rendered review exposed and corrected a disclosure timing race, clipped placeholder at 200% text, WebKit resize-notification warnings, an initial swatch that implied a selected colour, and undersized native WebKit select rendering.

Final rendered inspection passed for all 180 captures. The primary reviewer inspected all 390-point sheets; independent UI/accessibility reviewers inspected all 320- and 430-point sheets, then reinspected after the date-picker correction. No overlap, clipping, hidden-content leakage or duplicate controls were observed.

## Limits and decisions

- WebKit and emulated touch do not establish physical Safari/iPhone behaviour, onscreen keyboard avoidance, VoiceOver, Switch Control, Voice Control or native Dynamic Type.
- The three-month history range and Use shade confirmation followed by note autosave remain prototype proposals for owner review.
- No production persistence, backend, navigation, animation, platform commitment or public README changes.

Run `node verify.cjs [output-directory]` with Playwright and Chromium installed; set `TEST_WEBKIT=1` to use WebKit. `PLAYWRIGHT_MODULE` and `PLAYWRIGHT_BROWSERS_PATH` can identify existing runtimes.
