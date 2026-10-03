> Historical specification, superseded on 2026-10-03. See [current direction](../../APP_DESIGN.md). Retained for chronology, not current requirements.

# Product Idea Backlog

## Document Status

- Purpose: capture speculative design ideas before they become product decisions
- Last updated: 2026-09-12
- Status: ideation only
- Implementation status: none of the ideas in this document are approved for implementation

Ideas may conflict with each other or with current specifications. They should remain here until they have been compared, prototyped, and either promoted into the relevant design document or discarded.

## Book-System Direction

### Shared library, distinct books

Use books as the broader interaction world without making the entire app one folio.

- The daily diary is its own folio or Daybook.
- The seasonal image collection is a separately designed Scrapbook.
- Closing a book may return the user to a quiet library, desk, or book-selection space.
- Each book can have its own cover, paper, proportions, and internal layout.
- Page-based navigation provides continuity across the objects.

Potential value:

- Gives the app a strong spatial identity.
- Lets the diary and image collection feel meaningfully different.
- Makes “closing the book” a real navigation concept rather than a decorative animation.
- Creates room for future books without adding a conventional dashboard.

Questions:

- Is a library or desk necessary, or does it add a screen before common actions?
- Should the app always reopen the last-used book?
- Can users reach the diary and scrapbook directly without watching a closing animation?
- Does the metaphor remain clear to someone who ignores gestures?

## Core Spatial Model

A possible left-to-right sequence inside the daily book is:

1. Closed Daybook or library
2. Today’s page
3. Current monthly calendar
4. Selected past diary page

Movement toward the left opens or advances further into the book. Movement toward the right returns or closes.

This gives the user-proposed gestures a consistent meaning:

- On Today, swipe right to close the book.
- On Today, swipe left to open the monthly calendar.
- On Calendar, swipe right to return to Today.
- Selecting a recorded date opens that diary page.
- On a past page, swipe right to return to the Calendar that opened it.

The exact direction should adapt to right-to-left reading locales if page direction is localized.

## Idea: Book-Opening Animation

### Basic concept

Opening the daily diary begins with a closed seasonal cover. The cover moves aside and reveals Today as the first active page.

### Possible versions

#### Automatic opening

The book opens when the diary is selected.

Potential value:

- Immediate sense of entering a private object
- No extra tap
- Strong first impression

Concern:

- Can become a repeated delay.
- May feel ornamental after the novelty fades.

#### User-initiated opening

The user taps the cover or chooses an explicit Open action.

Potential value:

- The ritual is controlled by the user.
- The closed cover can establish season and object identity.

Concern:

- Adds friction before the daily task.
- A drag-only opening would be undiscoverable and inaccessible.

#### First opening of the day

Use the full opening only the first time the Daybook is opened each day. Later visits return directly to the last relevant page or use a shortened transition.

Potential value:

- Preserves the daily ritual without replaying it excessively.
- Gives the daily quote a natural first appearance.

Concern:

- Behavior changes across visits and needs to remain predictable.

#### Context-sensitive opening

- Normal app launch: open to the Daily Frontispiece.
- Reminder notification: open directly to Today’s entry page.
- Calendar-related deep link: open directly to the requested date.
- Returning within the same session: restore the last page.

Potential value:

- Preserves atmosphere without obstructing user intent.

### Animation character

The motion should feel like revealing a page, not demonstrate realistic paper physics.

Potential details:

- Cover rotates only enough to establish depth.
- A narrow shadow passes across the page as it opens.
- The page settles with a restrained haptic.
- The seasonal bookmark becomes visible beneath the cover.
- The daily quote appears only after the page is fully readable.

Avoid:

- Long three-dimensional animation
- Forced animation on every return
- Loud paper sound by default
- Content becoming interactive before it is visually stable
- A realistic effect that performs poorly or makes navigation feel slow

## Idea: Swipe Right to Close the Daily Book

### Proposed behavior

From Today, a rightward swipe closes the Daybook and returns to the containing library or book-selection view.

### Potential value

- Gives closure a physical meaning.
- Creates a natural way to leave the diary.
- Reinforces that the Daybook and Scrapbook are separate objects.
- Can make the app feel spatial rather than tab-based.

### Interaction questions

- Does the book close immediately, or follow the finger interactively?
- If a draft exists, is it saved automatically, left as a draft, or confirmed before closing?
- Does a short or accidental swipe cancel cleanly?
- Where does the user land after closing: library, home, or scrapbook shelf?
- Should the book remember whether it was closed when the app relaunches?

### Guardrails

- Do not take over the iOS system back gesture at the left screen edge.
- Provide a visible Close Book action; the swipe cannot be the only path.
- An incomplete gesture should return the page to rest without losing input.
- Reduce Motion should replace the physical close with a brief state change or crossfade.
- VoiceOver, Voice Control, keyboard, and Switch Control need equivalent actions.

## Idea: Swipe Left to Open a Single Monthly Calendar

### Proposed behavior

From Today, a leftward swipe turns one page and reveals the current month as a single calendar page.

### Calendar character

The calendar should feel like the Daybook’s index rather than a dashboard.

- One month occupies one page.
- Each day retains a clear date number.
- Recorded days carry small pigment studies.
- Blank days remain neutral paper.
- Today has a positional marker, not a completion badge.
- Tapping a recorded day opens its diary page.
- Tapping a blank past day may offer Add a Memory if backfilling is supported.

### Potential value

- Keeps the diary’s navigation within the book metaphor.
- Provides near-term value without statistics.
- Makes the Calendar easy to reach from the daily page.
- Avoids showing the entire season as a dense three-month dashboard.

### Month navigation options

#### Page through months horizontally

Continue swiping left for the next month and right for the previous month.

Concern:

This conflicts with using right swipe to return to Today. The back behavior changes depending on calendar position.

#### Use visible month controls

Keep horizontal right swipe reserved for returning to Today. Use small previous and next month controls in the calendar header.

Potential value:

- Preserves clear spatial navigation.
- Makes month movement visible and accessible.

#### Stack months vertically

The initial page is the current month; vertical scrolling reveals adjacent months.

Concern:

This weakens the single-page book metaphor and can turn the folio into a conventional scrolling calendar.

### Current idea preference

Use one monthly page with visible previous and next month controls. Reserve horizontal swipes for moving between Today and Calendar until the broader navigation model has been tested.

## Idea: The Daily Frontispiece as the First Open Page

The opening animation could reveal the minimal landing page rather than the entry form.

Sequence:

1. Closed seasonal cover
2. Frontispiece with date and daily epigraph
3. Today’s entry page
4. Monthly calendar

Potential value:

- Creates a complete book sequence.
- Gives the quote a clear home.
- Keeps color selection out of the opening composition.

Concern:

This may introduce too many layers before entry. The user would open the book and then open Today again.

Alternative:

Combine the Frontispiece and Today. The upper portion holds date and epigraph; the diary controls appear only after an explicit Begin or a partial page turn.

This should be tested against opening directly to Today.

## Idea: Seasonal Covers

Each seasonal Daybook receives a distinct cover based on its two pigments.

Possible details:

- Cloth, paper, board, or printmaking-inspired material
- Season and year as the only cover text
- Small volume mark inside rather than on the cover
- One pigment on the cover and the second on the bookmark or inside paper
- Cover wear or aging remains static rather than tied to logging frequency

Avoid showing entry count through book thickness, wear, page count, or ornament. That would turn the cover into a disguised progress indicator.

## Idea: The Fore Edge as a Memory Trace

When the Daybook is closed, small pigment traces could appear along the page edges.

Potential value:

- Suggests that private material exists inside.
- Makes each closed seasonal volume unique.
- Connects daily color samples to the physical book object.

Concern:

- Can become a preview of the accumulated seasonal artwork.
- May function like a completion meter.
- Could make sparse logging feel visibly deficient.

Safer version:

Use a fixed seasonal fore-edge pattern unrelated to entry quantity. Saved daily pigments remain visible only inside the Calendar.

## Idea: Today’s Bookmark

A bookmark always returns to Today from anywhere in the Daybook.

Potential behavior:

- Its base color comes from the current seasonal pair.
- After today is saved, a small portion adopts the selected pigment.
- Tapping it returns directly to Today.
- Its label changes between Today, Draft, and Kept without using status color alone.

Potential value:

- Gives Today a permanent spatial location.
- Reduces the need for a conventional tab bar inside the book.
- Supports quick recovery after browsing past pages.

Concern:

- Too many edge tabs can make the interface resemble a planner.
- Status changes could become a completion mechanic.

## Idea: Calendar as Table of Contents

Instead of presenting the month as a standard calendar grid, treat it as a visual table of contents.

Possible forms:

- Dates in a vertical editorial index with pigment marks in the margin
- Week rows treated as short sections
- A traditional grid with page-number typography
- Dates connected to page numbers or short note fragments

Potential value:

- Feels more book-specific than a generic calendar component.
- Can make recorded days easy to scan without charts.

Concern:

- Departing too far from a calendar grid may reduce date-finding speed.
- Showing note fragments could expose private information unexpectedly.

## Idea: Page Corners as Visible Controls

Small but clearly tappable page-edge controls can make navigation discoverable.

- Left or forward edge: Calendar
- Right or backward edge: Close Book
- Bookmark: Today
- Calendar header: previous and next month

These should use readable labels or accessible names. A folded-corner graphic cannot be the only indication that a page can turn.

## Idea: Closing Ritual After Saving

Saving and closing should remain separate actions.

- Keep This Moment preserves the entry.
- Swipe right or Close Book leaves the diary.

This separation allows the user to review a saved entry or continue to the Calendar without being ejected from the book.

Possible closing response:

- The page settles and becomes read-only.
- The selected pigment dries into its Calendar mark.
- The bookmark receives the pigment sample.
- The user chooses whether to close the book.

## Idea: Book State Across Sessions

Possible reopening rules:

- First open of the day: closed cover and opening ritual
- Same-day return: reopen directly to Today
- Return after browsing: restore the last page
- Reminder tap: open directly to the diary entry state
- New season: begin with the new cover and seasonal introduction

The chosen rule should prioritize the user’s apparent intent over preserving animation.

## Idea: Page Sound and Haptics

Potential use:

- One subtle haptic as a page settles
- Optional, nearly silent paper movement
- Distinct response for saving versus navigating

Requirements:

- Sound remains optional and should default to restraint.
- Haptics and sound never communicate unique information.
- Rapid page navigation should not create repeated noise or vibration.

## Ideas to Avoid or Treat Carefully

- Realistic page curl on every navigation action
- Requiring users to drag a page corner precisely
- Hiding navigation behind gestures
- Closing the book automatically after saving
- Showing a thicker book when more days are logged
- Torn pages for deletion or missed days
- Page-flipping through every day to reach the Calendar
- Multiple nested book-opening steps before entry
- Treating the library shelf as a decorative home screen with no practical value
- Using the book metaphor for settings, permissions, and error dialogs

## First Concept Prototype

The first prototype should test only the spatial logic:

1. Closed Daybook
2. Short opening into Today
3. Swipe right or visible action to close
4. Swipe left or visible action to open the current monthly Calendar
5. Swipe right or visible action to return from Calendar to Today

It should not yet attempt realistic page physics, cover materials, sound design, a complete scrapbook, or multiple months.

Questions to evaluate:

- Do users understand where the Daybook exists spatially?
- Do the swipe directions feel natural?
- Is the Calendar discoverable without instruction?
- Does closing the book feel satisfying or like an unnecessary exit step?
- Does the animation remain pleasant after repeated use?
- Can users ignore the gestures and still complete every task?

## Promotion Rule

An idea moves from this backlog into a feature specification only after:

- Its purpose is clear.
- It does not weaken the calm daily workflow.
- Its navigation remains understandable without gesture instruction.
- Its accessibility alternative is defined.
- A simple prototype supports the intended experience.
