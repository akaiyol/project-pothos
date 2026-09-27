# Daily Landing Page Exploration

## Document Status

- Feature: first screen of the daily experience
- Product stage: concept exploration
- Last updated: 2026-09-19
- Status: landing-page concepts under consideration
- Related format exploration: [DIARY_FORMATS.md](DIARY_FORMATS.md)
- Related daily specification: [DAILY_DIARY.md](DAILY_DIARY.md)
- Uncommitted interaction ideas: [IDEAS.md](IDEAS.md)

## Current V1 Revision — 2026-09-14

The current V1 direction removes the separate landing-page step. The date, optional location, short daily quotation, mood field, and optional note share one minimal notebook page. This reduces friction and keeps the quote present without making the user open a second page before recording.

Visual constraints:

- White page with softly curved notebook edges
- One simple red margin line
- No ruled paper, decorative book cover, page-turn controls, or visible navigation metaphor
- Small typography with generous spacing
- One highly legible primary typeface and one wispy italic accent face
- Quotation set in the accent face; controls and entry text remain in the primary face

Location is a contextual memory detail, not a required part of the diary. If retained, the page shows a quiet city-level label only after explicit permission or manual selection. Continuous location tracking is not part of the V1 concept.

The location label belongs with the date metadata. The prompt “Where are you today?” should not be used on the same page because it ambiguously refers to physical location. Current prompt candidates are documented in [DAILY_DIARY.md](DAILY_DIARY.md).

This revision supersedes the separate frontispiece recommendation below for the initial prototype. The concepts remain documented as prior exploration.

## Clarified Product Structure

Books provide the shared interaction theme, but each part of the product should remain its own object.

- The daily diary is a folio or daybook.
- The Calendar is the index inside that folio.
- Seasonal images live in a separately designed scrapbook.
- Page turning may become a shared navigation behavior.
- The folio’s paper system should not be copied directly into the scrapbook.

This prevents one metaphor from flattening the entire app into the same visual treatment.

Page-flipping behavior remains an idea only. Its motion, gestures, navigation rules, and implementation are intentionally deferred.

## Landing Page Purpose

The landing page is the threshold to today’s diary page. It should create a small pause before asking the user to record anything.

It should answer only:

- What day is this?
- What line accompanies today?
- How do I open today’s page?

The color selector should not appear here. It belongs inside the opened diary page and should be reduced in scale there as well.

## Content Budget

Recommended visible content:

1. Date
2. Optional season notation
3. One short reflective quotation
4. One primary action
5. Minimal navigation

Avoid:

- Explanatory product copy
- Seasonal countdown
- Entry count
- Streak or completion language
- Mood analytics
- Artwork progress
- Multiple prompts
- A large color field
- Decorative controls without a task

## Concept A: Daily Frontispiece

### Idea

Treat the landing page like the title page at the beginning of a book or chapter. It is mostly typography and space.

### Composition

- Small date at the top
- Season as quiet metadata
- One quote centered vertically
- Attribution directly below
- “Open today’s page” near the bottom
- A narrow seasonal page edge or bookmark color

### Character

Editorial, calm, and direct. The page feels considered without becoming ornamental.

### Strengths

- Supports very few words
- Gives the quote enough space to matter
- Creates a clear threshold before diary input
- Works naturally with a page-turn transition
- Leaves seasonal color present but secondary

### Risks

- Too much empty space may feel unfinished if typography is weak.
- A quote-centered page can resemble a generic wellness app.
- Repeated use may make the opening step feel unnecessary.

### Response to the risks

Use exceptional typography, a stable layout, concise editorial selection, and a direct open action. Allow returning users to bypass the pause quickly.

## Concept B: Seasonal Bookplate

### Idea

Treat the landing page as the identifying page inside the current seasonal volume.

### Composition

- “Spring · Volume 01” as a small bookplate
- Date as the main typographic element
- Short quote beneath
- One understated action to enter today’s page
- Two seasonal pigments visible only in an edge, rule, or small printed device

### Character

Archival and collected. The user feels that today belongs to a larger seasonal volume.

### Strengths

- Establishes the folio object clearly
- Connects each day to its season
- Gives volume and season naming a place
- Can develop a strong identity over time

### Risks

- Volume numbers may feel mechanical or pretentious.
- The bookplate can become a decorative badge rather than useful orientation.
- It emphasizes the container more than the daily pause.

## Concept C: Margin Epigraph

### Idea

Use the page margin as the main compositional device. The quote appears like a note found at the edge of a manuscript rather than centered like motivational content.

### Composition

- Large date occupying the page body
- Short quote aligned to the folio margin
- Small “Today” notation
- “Turn to today” at the lower edge

### Character

Quiet, literary, and slightly unexpected.

### Strengths

- Feels less like a quotation app
- Makes the folio margin functional
- Creates a distinctive editorial composition
- Preserves substantial negative space

### Risks

- Small marginal text can become inaccessible.
- The primary action may be too easy to miss.
- Long quotes do not fit the format.

## Concept D: Seasonal Endpaper

### Idea

Use a restrained pattern made from the season’s two pigments as an endpaper behind a very small amount of text.

### Composition

- Soft two-color material pattern covering part of the page
- Date and quote placed on a clear paper area
- “Open today’s page” as the only control within the composition

### Character

More visual and atmospheric than the Frontispiece. The season is felt before it is named.

### Strengths

- Gives the seasonal palette a non-interactive role
- Makes each seasonal landing page immediately distinct
- Connects book design with the color system
- Can make opening the app feel special without showing the final artwork

### Risks

- The pattern may compete with the quote.
- It can feel like an unfinished artwork preview.
- Pattern and transparency can reduce legibility.
- Daily repetition may make it visually loud.

### Best use

Use only as a narrow band, page edge, or low-contrast print—not as a full-screen illustration.

## Concept E: The Bookmark

### Idea

The landing page is nearly blank except for a vertical bookmark that holds the date and marks the route to today’s page.

### Composition

- Quote in the page body
- Date set into a colored bookmark or edge tab
- Tapping “Open today” moves from the marker into the page
- After saving, the bookmark subtly changes position or notation

### Character

Minimal, tactile, and strongly connected to page navigation.

### Strengths

- Gives the date and entry state a consistent home
- Uses seasonal color sparingly
- Can support the future page-turning concept
- Makes the landing page feel like a place within a book

### Risks

- A bookmark can become a disguised progress indicator.
- Gesture-based interaction may be unclear.
- Decorative motion could slow the flow.

The bookmark must have a visible button equivalent; pulling or dragging cannot be the only way to enter.

## Recommended Direction: Frontispiece with a Seasonal Bookmark

Combine the clarity of the Daily Frontispiece with the restrained physical cue of the Bookmark.

### Initial hierarchy

At the top:

> Saturday · 18 April  
> Spring

At the center:

> One short reflective line  
> Attribution

At the bottom:

> Open today’s page

A narrow bookmark or page edge carries one of the current season’s pigments. It provides atmosphere and future page-turn context without making color selection the landing page’s subject.

## Entry-State Variations

### No entry today

- Primary action: “Open today’s page”
- Bookmark rests at today’s position.
- No reminder or incomplete indicator appears.

### Draft exists

- Primary action: “Continue today’s page”
- A small neutral draft notation is available.
- The quote and page composition remain unchanged.

### Entry saved

- Primary action: “Return to today”
- Optional secondary line: “Today’s page is kept.”
- The bookmark can show a small pigment edge from the saved selection.
- No checkmark, celebration, or completion score is necessary.

### Returning after an absence

- The landing page always opens on today.
- It does not mention missed days.
- Previous pages remain available through the folio index.

## Quote Direction

A daily quote can add immediate value, but it should feel like an epigraph rather than motivational content.

### Editorial principles

- Reflective rather than instructive
- Calm without insisting on positivity
- Emotionally open enough to coexist with a difficult day
- Short enough to read at a glance
- Stable for the entire day
- Unrelated to the mood the user later selects
- Carefully attributed when attribution is required

Avoid:

- “You’ve got this” language
- Productivity advice
- Claims about healing or mental health
- Quotes selected to correct or reframe the user’s mood
- Long passages
- Automatically generated imitations of living writers
- Unverified quotations or unclear usage rights

### Working label

The interface does not need to call it an “inspirational quote.” It can simply appear as the page’s epigraph or use a quiet label such as “A line for today.”

### Source strategy

Potential sources include:

- Properly licensed short quotations
- Public-domain literature and poetry
- Original editorial lines written specifically for the product
- Optional lines saved by the user in a later version

Source rights and attribution requirements must be verified before release.

### User control

Allow the daily line to be hidden if users find quotations distracting or emotionally mismatched. The landing page should remain intentionally composed without it.

## Relationship to the Diary Page

Opening today’s page should shift from contemplation to expression.

- The date remains in the same relative place to maintain continuity.
- The quote does not need to repeat inside the diary.
- The seasonal bookmark or page edge continues across the transition.
- The color field appears at a smaller scale than in the first mockup.
- Optional writing receives more space and visual emphasis.
- Navigation remains available without requiring a page-turn gesture.

The future page-turn transition should express moving from frontispiece to content, not imitate paper physics for its own sake.

## Reduced Color-Field Direction

The color selector should become one component of the diary page rather than its dominant object.

Potential treatments:

- A compact horizontal field that expands only when touched
- A small current sample with “Choose a color” opening a dedicated selection page
- A shallow pigment strip positioned between the date and writing area
- A foldout field that occupies more space only during selection

The dedicated selection page offers the cleanest landing and writing layouts, but it adds an extra page turn. The compact expanding field is the strongest initial option to prototype.

## Page-Turning Idea for Later

Page turning can unify movement between:

- Landing page and today’s diary page
- Today and adjacent diary days
- Calendar index and an individual page
- Scrapbook index and a seasonal artwork

It should not be used for every modal, setting, or utility action.

Future requirements:

- Visible tap controls in addition to swiping
- Predictable forward and backward direction
- Immediate navigation when Reduce Motion is enabled
- No long animation before interaction becomes available
- VoiceOver focus moves to the new page heading
- Interactive controls never move underneath an active finger during a page turn

No page-turn behavior is selected or implemented at this stage.

## Working Names for the Daily Diary

| Name | Character | Concern |
| --- | --- | --- |
| Daybook | Concise, bookish, historically connected to daily records | Some users may not know the term |
| Daily Folio | Clear connection to the object metaphor | Slightly formal |
| Book of Days | Poetic and memorable | May carry cultural or religious associations |
| The Folio | Minimal and distinctive | Does not immediately communicate diary |
| Daily Pages | Clear and approachable | Less ownable or distinctive |
| Field Notes | Observational and seasonal | Can feel outdoors-focused and is strongly associated with existing stationery branding |

The strongest working name is **Daybook**, while **folio** describes the object and interaction model. User testing should confirm whether the term is understandable without explanation.

## Prototype Recommendation

Prototype three landing states using the same Frontispiece with Seasonal Bookmark composition:

1. No entry
2. Draft waiting
3. Entry kept

Then test the transition into a diary page with a compact, expandable color field. This isolates whether the landing page adds a meaningful pause or merely creates an extra tap.
