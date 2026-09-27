# Diary Format Exploration

## Document Status

- Feature: daily diary format and metaphor
- Product stage: concept exploration
- Last updated: 2026-09-12
- Status: format concepts under consideration
- Related specification: [DAILY_DIARY.md](DAILY_DIARY.md)
- Daily landing exploration: [DAILY_LANDING.md](DAILY_LANDING.md)
- Uncommitted interaction ideas: [IDEAS.md](IDEAS.md)

## Design Question

What should the diary feel like as an object, and how literally should the interface borrow from notebooks, calendars, artist materials, and archives?

The current structural direction is a shared book theme with distinct objects: a folio or daybook for diary entries and a separately designed scrapbook for completed images. Page turning may become a common navigation behavior but is not yet specified or implemented.

The chosen format must support:

- A calm daily entry
- The seasonal color field
- Fast access to previous days
- Neutral treatment of missed days
- A growing sense of accumulated material
- A meaningful seasonal close
- Clear separation between diary material and finished artwork

## Literal Notebook Assessment

A notebook is familiar and emotionally appropriate, but direct imitation has limitations.

### Useful qualities to borrow

- Pages create a natural unit for one day.
- Paper suggests privacy, attention, and preservation.
- Dates, margins, annotations, and page sequence support memory.
- Closing a book provides a strong seasonal ritual.
- A journal and a scrapbook belong to the same material world.

### Literal details to avoid

- Fake rings, leather, stitching, page curls, and heavy shadows
- Cramped two-page spreads on a phone
- Swipe-only page turning
- Handwriting fonts for interface text
- Ruled lines that make a short note feel unfinished
- Empty physical pages representing every missed day
- Long page-flip animations that slow repeat use

### Design position

Borrow the structure and emotional logic of a notebook without recreating one as a digital prop. The interface should feel editorial and tactile, not skeuomorphic.

## Concept A: Seasonal Folio

### Metaphor

The user creates one loose study each day and places it into a portfolio for the current season. At the end of the season, the folio closes and its contents become source material for the artwork.

### Today

A single uncluttered sheet fills most of the screen. It contains the date, seasonal field, optional line, and closing action. There is no simulated book spine or facing page.

### Calendar

The folio opens to an index of the season. Three monthly sections show dated pigment samples. Selecting a day opens its individual sheet.

### Save interaction

The pigment sample settles into the page, the note becomes still, and the sheet appears to join the folio beneath it. This should be brief and optional under Reduce Motion.

### Seasonal close

The accumulated studies are gathered and the folio is sealed before artwork generation. The completed artwork becomes the public face of the season; the folio remains privately accessible behind it.

### Strengths

- Direct connection between daily material and final art
- Tactile without requiring a literal bound notebook
- Strong seasonal closing ritual
- Supports one-day pages and a calendar index naturally
- Keeps unfinished material visually distinct from finished artwork

### Risks

- “Folio” may be unfamiliar language.
- Page and paper effects can become decorative excess.
- The closing metaphor must not imply entries can no longer be corrected without explanation.

## Concept B: Seasonal Almanac

### Metaphor

The diary is a record of the season, like an observational field book. Emotional entries sit alongside the passage of dates, light, and seasonal change.

### Today

The entry feels like a dated observation: pigment sample, one line, and understated seasonal context.

### Calendar

The full season is the primary object. Its three months form a continuous vertical or foldout calendar rather than separate notebook pages.

### Seasonal close

The completed season becomes one volume or plate in a personal almanac.

### Strengths

- Makes seasonality central rather than decorative
- Gives the calendar more conceptual weight
- Supports viewing patterns across a whole season
- Avoids common journaling-app conventions

### Risks

- Can lean too heavily into nature imagery.
- May feel observational or archival rather than intimate.
- A whole-season calendar can become visually dense on a phone.

## Concept C: Pigment Archive

### Metaphor

Each day is preserved as a labeled material sample. The diary resembles an artist’s pigment library or museum study archive.

### Today

The user samples the seasonal field and creates a small color study with an optional annotation.

### Calendar

Days appear as an orderly tray or contact sheet of pigment samples. Recorded days hold material; blank days remain open cells.

### Seasonal close

The tray becomes the palette source for the completed artwork.

### Strengths

- Strongest connection to the two-color field
- Distinctive and visually coherent
- Calendar marks feel intentional rather than decorative dots
- Easy to understand at a glance

### Risks

- Can feel like a dataset or collection interface rather than a diary.
- Order and labeling may make the experience feel clinical.
- The archive may visually compete with the final artwork.

## Concept D: Accordion Season

### Metaphor

The season is one continuous sheet folded into approximately ninety daily panels. Each entry opens one fold; the completed season closes into a compact object.

### Today

Today’s panel expands while neighboring days remain visible as narrow edges or marks.

### Calendar

The accordion can be unfolded into a continuous seasonal sequence. Month transitions are folds rather than separate screens.

### Seasonal close

The complete strip folds inward and is stored with the seasonal artwork.

### Strengths

- Expresses continuity and time beautifully
- Avoids the sense of isolated daily tasks
- Creates a distinctive seasonal closing motion
- Can reveal rhythm without charts

### Risks

- Difficult to navigate efficiently on a phone
- Easy to turn into a long-scroll novelty
- Complex motion and focus behavior
- May expose an unfinished aggregate that competes with the final reveal

## Concept E: Layered Vellum

### Metaphor

Each day is a translucent layer holding one pigment sample and line. The season gradually gains visual density as layers accumulate.

### Today

A fresh translucent surface sits over a restrained trace of earlier layers.

### Calendar

The user separates or browses layers by date.

### Seasonal close

The layers are gathered as the physical source of the artwork.

### Strengths

- Beautiful expression of accumulation
- Makes time and memory feel materially present
- Supports subtle depth and parallax

### Risks

- Becomes an unfinished artwork preview
- Transparency creates contrast and accessibility problems
- Past-entry navigation is unclear
- Visual density may undermine calm

## Concept F: Cards in a Seasonal Box

### Metaphor

Each day is a small dated card placed into a private seasonal box. It borrows from correspondence, recipe cards, and keepsake collections.

### Today

A compact card contains the pigment sample and optional message to oneself.

### Calendar

Cards can be arranged chronologically or viewed through a calendar index.

### Seasonal close

The box closes and the artwork is placed on its cover or stored beside it.

### Strengths

- Personal and collectible
- Clear saving gesture
- Easy to revisit individual entries
- Less conventional than a notebook

### Risks

- Can imply that every day needs a complete written message.
- A card may feel too small for difficult or detailed entries.
- The box metaphor can become visually cumbersome.

## Recommended Direction: Seasonal Folio with an Almanac Index

Combine the strongest parts of the Folio and Almanac concepts.

### Object model

- Each day is one loose study.
- Each month is one section within the folio.
- The three months form one seasonal volume.
- The Calendar is the folio’s visual index.
- At season end, the volume closes and sits behind its finished artwork.

This provides a notebook-like sense of pages and preservation without displaying a fake bound book.

## Recommended Screen Formats

### Today: the current study

The screen resembles a well-composed editorial sheet:

- Small date and season notation
- Generous margin
- Large color field as the central material surface
- Optional note below
- “Keep this moment” as the closing action

The sheet occupies the screen rather than floating as a rounded card. The phone itself becomes the page boundary.

### Calendar: the seasonal index

Present the current season as three quiet monthly sections in one continuous view.

Recorded days contain a small pigment study. Blank days retain their date and paper surface without warnings or empty-state symbols. Today receives a positional marker rather than a success indicator.

On smaller screens, the months stack vertically. The app restores the user’s previous position after opening and closing a day.

### Past entry: a lifted sheet

Selecting a day opens its sheet above the index. The motion should feel like lifting material from a folio, while the accessible transition behaves as normal navigation with predictable focus.

The page shows the original seasonal pigment treatment, date, note, and editing controls.

### Current season: the folio edge

Today may include a restrained indication that other studies exist beneath the current one: a narrow offset edge, a small seasonal notation, or a route to “This season.”

Avoid showing a literal stack whose thickness measures compliance.

### Completed season: artwork with source volume

In the scrapbook, the artwork remains dominant. A secondary “Open this season” action reveals the folio index and original diary pages.

This gives the diary lasting value while protecting the artwork’s visual hierarchy.

## Material Language

### Paper

Use subtle paper character through color, grain, and edge behavior. Texture should be almost unnoticed at ordinary viewing distance and should disappear when it harms contrast or performance.

### Typography

Use editorial typography rather than handwriting simulation. Date notation, page hierarchy, and generous spacing can communicate a journal more effectively than a script font.

### Margins and annotations

A stable margin can hold the date, season, edit state, or small navigation marks. It should function as information architecture, not decoration.

### Pigment

The selected daily color should be the most materially expressive element on the sheet. Other interface elements remain quiet so the pigment has presence.

### Binding cues

Use page order, section labels, and closing behavior instead of literal rings or stitching. The product can feel bound by time rather than by hardware.

## Thoughtful Detail Opportunities

### The day begins as clean material

Today opens as a prepared surface, not a blank form. The date is already placed; the user only needs to locate their color.

### Pigment settling

After selection, the sample can take on a slight edge bloom or paper absorption before becoming still. This must remain brief and have a static alternative.

### Monthly section changes

Moving into a new month can introduce a small typographic divider or change in page notation without pretending a new season has begun.

### Returning to place

Closing a past entry returns to the same month and day in the index. This small continuity is more valuable than elaborate page-turning.

### Editing as reopening

Editing returns the page to its active state. The interface should not imply that the user is damaging or overwriting a precious original.

### Deletion without shame

Deleting an entry returns the day to neutral paper. Avoid torn-page imagery, empty outlines, or language suggesting loss or failure.

### Seasonal closure

The folio closes only after the user confirms what will contribute to the artwork. It should feel conclusive but not punitive or irreversible without explanation.

## Navigation Options

### Option 1: Today, Calendar, Scrapbook

Keep familiar navigation labels while expressing the folio metaphor within each screen. This is the clearest initial option.

### Option 2: Today, Season, Scrapbook

Rename Calendar to Season and make the three-month index its central view. This strengthens the concept but may make historical date lookup less obvious.

### Option 3: Folio and Scrapbook

Place Today and Calendar inside one Folio destination. This is conceptually elegant but risks hiding the most common actions.

The current recommendation is Option 1 until prototype testing shows that “Season” remains understandable as navigation.

## Format Guardrails

- Do not make users turn pages to reach today.
- Do not require swiping when visible navigation can do the same job.
- Do not represent missed days as torn, crossed out, or conspicuously blank pages.
- Do not make paper texture reduce text clarity.
- Do not animate every transition as a page turn.
- Do not use the growing folio as a disguised streak or completion meter.
- Do not let the diary pages become more visually elaborate than the seasonal artwork.
- Do not use a physical metaphor when it makes editing, search, accessibility, or recovery harder to understand.

## Prototype Comparison

Prototype two diary formats using the same color field and content:

### Variant A: Seasonal folio

- Full-screen daily sheet
- Three-month seasonal index
- Brief “place into folio” save response
- Past entries open as individual sheets

### Variant B: Pigment archive

- Material-sample daily entry
- Contact-sheet Calendar
- Direct save without a page metaphor
- Past entries open as labeled studies

Evaluate:

- Which makes a daily entry feel more personally meaningful?
- Which supports the seasonal premise without becoming theatrical?
- Which makes blank days feel neutral?
- Which makes users want to revisit their own writing?
- Which preserves the artwork as the season’s primary visual event?
- Which remains clear after the novelty of the metaphor fades?

## Decisions Needed

- Folio, Almanac, Pigment Archive, or another metaphor
- How literal the paper and page treatment should be
- One-month Calendar versus full-season index
- Whether completed artwork links back to its source diary
- Whether “Calendar” or “Season” is the clearer navigation label
- Exact save metaphor and duration
- Whether the folio is visible during daily entry or only in the seasonal index
- Whether paper treatment changes by season or only by appearance mode

## Current Recommendation

Move forward with the Seasonal Folio and Almanac Index as the primary concept. Keep the notebook influence through page structure, editorial rhythm, and seasonal closure—not through literal bindings or ornamental page effects.

The first prototype should focus on three connected states: an unsaved daily sheet, the moment it is kept, and the seasonal index after saving. If those states feel coherent, the metaphor is strong enough to extend into past entries and the seasonal close.
