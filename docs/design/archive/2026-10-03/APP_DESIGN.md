> Historical specification, superseded on 2026-10-03. See [current direction](../../APP_DESIGN.md). Retained for chronology, not current requirements.

# Project Pothos — Product Design

## Document Status

- Product stage: concept development
- Platform: undecided — app or website
- Last updated: 2026-09-27
- Purpose: living record of the product vision, experience decisions, open questions, and design rationale
- Idea backlog: [IDEAS.md](IDEAS.md)

This document should evolve with the product. Confirmed decisions are distinguished from working hypotheses and open questions so early exploration does not become an accidental constraint.

## Product Concept

### Project identity

The confirmed project name is **Project Pothos**. Its intended meaning is a longing to feel whole; this is the project's interpretation, not a literal translation of the Greek word.

The platform remains undecided between an app and a website. Earlier iOS-specific architecture and interaction proposals are exploratory and do not establish a platform requirement.

### One-sentence description

A private mood journal that transforms a season of small daily reflections into a personal piece of art and preserves each piece in an evolving digital scrapbook.

### Core promise

The app helps people notice and remember the emotional texture of their lives without turning reflection into measurement, performance, or self-optimization.

### Product essence

Calm, art, and emotion cannot be rushed. The waiting period is part of the work: a piece gains meaning because it has been shaped by a lived season rather than produced on demand.

The product should not apologize for this slowness or disguise it with constant rewards. Its responsibility is to make the daily act worthwhile on its own, while allowing anticipation to develop quietly in the background.

### Intended feeling

Using the app should feel:

- Calm rather than demanding
- Personal rather than clinical
- Expressive rather than analytical
- Reflective rather than judgmental
- Special at seasonal moments without making daily use burdensome

## Product Purpose

Most mood trackers emphasize charts, scores, streaks, and trends. This product explores a different relationship with emotional data: everyday feelings become creative material.

The seasonal artwork is not a grade or diagnostic summary. It is a keepsake—an interpretation of a period of life that can be revisited without reducing that period to a number.

## Experience Principles

### 1. Reflection without judgment

The app should acknowledge every mood without labeling it as success, failure, improvement, or decline.

### 2. Art is a memory, not a score

Generated work should represent complexity. Difficult seasons can still produce beautiful, meaningful art. Visual quality must never imply that a user had a “good” or “bad” season.

### 3. Daily use stays lightweight

A check-in should be complete with one mood selection. Text adds depth but is optional. The experience should not punish missed days.

### 4. Seasonal moments feel ceremonial

The reveal should have more emotional weight than an ordinary app result. Anticipation, pacing, sound, motion, language, and composition should work together deliberately.

### 5. The collection becomes more meaningful over time

Each artwork should stand alone while also contributing to a visually coherent scrapbook. Long-term value comes from a growing personal archive.

### 6. Privacy is part of the experience

Mood entries and reflections are intimate. The interface should make ownership, storage, processing, and deletion understandable rather than hiding them in legal language.

### 7. Accessibility is designed in, not added later

Mood, navigation, and artwork meaning must never depend only on color, motion, gestures, or spatial arrangement.

### 8. Craft exists at every scale

The seasonal artwork is the culmination, not the only designed moment. Typography, language, spacing, touch response, transitions, empty states, errors, and ordinary diary interactions should all express the same care as the final artwork. Detail should improve meaning or feeling rather than become decoration for its own sake.

## Target User Hypothesis

The initial user is someone who:

- Wants a gentle reflection habit but finds traditional journaling demanding
- Is visually or emotionally drawn to art, atmosphere, and keepsakes
- Prefers personal interpretation over productivity metrics
- May use the app irregularly and should still receive a meaningful result
- Values privacy and a quiet experience over social features

This is a working hypothesis, not yet a validated audience definition.

## Core Experience Loop

1. The user arrives in a quiet space and pauses before recording anything.
2. The user names a mood and may add a short reflection.
3. The entry is placed into the current season with a small sense of closure.
4. The calendar gradually becomes a subtle record of lived moments.
5. The user can revisit recent entries without receiving a score or automated judgment.
6. At the end of the season, the app translates the accumulated material into artwork.
7. The artwork is revealed as a reflective keepsake.
8. The piece is added to the scrapbook alongside earlier seasons.
9. The user can revisit the artwork and the memories connected to it.

The loop should work even if the user records only a small number of entries.

## Daily Value Model

The daily experience should provide three kinds of value without competing with the seasonal reveal.

### Immediate value: a pause

The check-in creates a brief transition out of the day. Naming a feeling and optionally writing one line can be useful even if no artwork were ever produced.

### Near-term value: a memory

The calendar lets the user recover what a day or week felt like. Its value is recall, not performance analysis.

### Long-term value: a contribution

Each entry becomes material for the seasonal piece. The interface should acknowledge that contribution without showing an unfinished version of the final artwork.

The design should be evaluated in that order. If the daily pause has no independent value, anticipation alone is unlikely to sustain use for an entire season.

## Recommended Daily Workflow

The detailed interaction specification is maintained in [DAILY_DIARY.md](DAILY_DIARY.md).

### 1. Arrive

The Today screen opens with visual quiet: the date, a restrained seasonal atmosphere, and one invitation such as “What is present today?” It should not open on statistics, a streak, or a countdown.

The arrival may use a short ambient transition or gentle haptic, but the main action must be immediately available and Reduce Motion must be respected.

### 2. Name the feeling

The user chooses a broad mood. If desired, they can add a second feeling or a more specific word. This supports emotional ambiguity without making every check-in a classification exercise.

The first choice should take only a few seconds. Color, texture, and shape can make the interaction expressive, but every option also needs a clear text label.

### 3. Leave a trace

The user may write a sentence, phrase, or single word. The field should feel intentionally small rather than like an empty page the user is expected to fill.

Prompts can rotate occasionally, but they should remain optional and concrete. The default experience should not require the user to explain or justify a mood.

### 4. Place it into the season

Saving should feel like placing something into a collection rather than submitting a form. A short closing interaction—a soft fold, settling mark, quiet sound, or haptic—can signal that the moment has been kept.

The app should not reveal a miniature artwork after every entry. That would turn the seasonal piece into an incremental progress graphic and weaken the idea that art needs time to form.

### 5. Receive closure

The response should be brief and non-evaluative: confirmation that the moment was kept, not advice or an AI interpretation. The user can leave immediately or open the calendar.

### 6. Revisit when useful

The calendar supports reading past entries and noticing personal context. It should not automatically label trends as positive or negative. Optional reflection should be initiated by the user.

## Supporting Cadences

### Weekly: a quiet look back

Once a week, the app can offer an optional review of that week’s entries. The user scrolls through their own words and moods and may choose one word or moment to carry forward.

This is not a weekly report. It should avoid generated summaries, mood scores, and claims about behavioral patterns. Its purpose is memory consolidation and personal authorship.

### Through the season: a sealed work in progress

The current season can be represented as a closed portfolio, vessel, or other contained object. Its surface may change subtly as time passes or entries accumulate, but it should not preview the final composition.

Useful information may include the season’s name, dates, and a neutral phrase such as “18 moments kept.” Avoid completion percentages, daily quotas, and a countdown that dominates the screen.

### End of season: invitation rather than automatic reward

When the season has matured, the app invites the user to create the piece. Before generation, the user can review what will be included and exclude private entries if that control is offered. The artwork is then revealed in a dedicated ceremony and placed in the scrapbook.

## Daily Navigation Hypothesis

A focused initial structure is:

- Today: the current check-in and entry point to the current season
- Calendar: recent memory and entry history
- Scrapbook: completed seasonal work

The current season should be present from Today without requiring a fourth primary destination. This keeps the everyday interface simple while maintaining a quiet sense of continuity.

## Daily Experience Guardrails

Avoid features that manufacture urgency or dilute the seasonal payoff:

- Streaks, badges, points, or missed-day warnings
- Daily AI advice or personality interpretations
- A live preview of the unfinished seasonal artwork
- Mood scores and improvement targets
- Excessive prompts or required writing
- Push notifications framed as obligation
- Surprise visual rewards after every entry
- A prominent day-by-day countdown to the reveal

Daily value should come from attention, expression, recall, and the act of preserving—not from variable rewards.

## Core Product Objects

### Mood Entry

A single reflection associated with a calendar date.

Potential fields:

- Date and time
- Primary mood
- Optional mood intensity or nuance
- Optional short text
- Optional user-selected visual cue
- Creation and edit timestamps

The minimum useful entry is still undecided. The current assumption is one mood plus optional text.

### Season

A bounded period containing mood entries and an associated artwork.

Questions remain around whether seasons should follow astronomical dates, meteorological dates, fixed three-month periods, or the user’s local cultural context.

### Artwork

The permanent visual artifact created from a season.

Potential fields:

- Finished image or procedural composition
- Season and year
- Title
- Short interpretive description
- Accessible visual description
- Generation recipe or seed
- Source-data summary
- Creation state and failure state

### Scrapbook

The collection of completed seasonal artworks. It is both the long-term archive and the clearest expression of the product’s value over time.

## Minimum Viable Experience

### Included

- Simple onboarding and privacy explanation
- Daily mood selection
- Optional short text reflection
- Calendar-based history
- Editing or deleting an entry
- Seasonal artwork creation
- Artwork reveal
- Scrapbook of completed pieces
- Artwork detail view
- Local notifications as an optional, gentle reminder
- Export and deletion controls appropriate to the stored data

### Excluded from the initial product

- Social feed or public profiles
- Mood comparison with other users
- Competitive streaks or punitive missed-day messaging
- Clinical diagnosis, treatment claims, or crisis interpretation
- General-purpose AI chat
- Dense analytics dashboards
- User-authored image prompts requiring prompt-writing skill
- Likes, rankings, or engagement-based recommendations

These exclusions protect the product’s focus. They can be revisited only if they support the core emotional experience.

## Initial Screen Map

### Today

The primary entry point. It should answer two questions immediately:

- How do I feel today?
- What, if anything, would I like to remember?

The screen should feel complete before the user enters text.

### Entry Composer

The focused check-in experience. It may be embedded in Today or presented as a separate moment depending on the desired pacing.

### Calendar

A chronological view of recorded and unrecorded days. It should support memory and navigation without turning gaps into failure states.

### Entry Detail

A quiet view for reading, editing, or deleting a past reflection.

### Seasonal Transition

A short experience explaining that the season is complete and the artwork is ready—or ready to be created. It should set expectations about what information is used.

### Artwork Reveal

A dedicated, low-distraction presentation of the completed piece. The experience should provide enough time and space for the user to form their own response before offering interpretation.

### Scrapbook

A collection view organized chronologically. It should feel tactile and personal rather than like a generic image grid.

### Artwork Detail

Displays the piece, season, title, accessible description, and selected context. The extent to which source entries are exposed here remains open.

### Settings and Privacy

Controls for reminders, data processing, export, deletion, accessibility preferences, and any cloud or model features.

## Key Experience Moments

### First launch

The app should explain its value quickly: small reflections become seasonal art. It should also establish that the user owns their private entries and can begin without completing a long setup flow.

### First check-in

The first entry should teach the interaction through use. Avoid a tutorial that explains every future feature before the user has emotional context for it.

### Missed days

Blank days are neutral. The app should not use broken streaks, warning colors, guilt-oriented copy, or fabricated entries to fill gaps.

### Returning after an absence

The product should welcome the user back without calling attention to how long they were away unless that information is directly useful.

### End of season

The app should make the transition feel earned even when there are few entries. It should communicate how limited data affects the artwork without devaluing the result.

### Generation delay or failure

The user should never lose their seasonal record because generation fails. A retry, fallback artwork, or deferred creation path must preserve the ceremony and the underlying data.

### Artwork reveal

The piece should appear before charts or explanations. Supporting language should be interpretive and tentative, avoiding claims that the system fully understands the user.

### Revisiting the scrapbook

Browsing should support both visual discovery and chronological memory. A piece should be understandable without requiring the user to remember the exact generation process.

## Mood Input System

The mood input determines the emotional vocabulary, accessibility, data quality, and visual material available to the artwork system. The current direction is a two-dimensional color field whose pigments change each season while its underlying emotional dimensions remain stable.

The system should:

- Be fast enough for everyday use
- Allow mixed or ambiguous feelings
- Avoid implying that every emotion fits a rigid category
- Pair visual encoding with readable labels
- Remain usable without color perception or precise gestures
- Produce data consistent enough to inform seasonal art

The final dimensions and seasonal mappings have not been selected. The concept is specified in [MOOD_INPUT.md](MOOD_INPUT.md).

## Seasonal Art System

### Purpose

The art system should translate patterns and memories into a unique artifact without pretending to objectively depict the user’s mental state.

### Potential inputs

- Mood distribution
- Mood intensity or energy, if collected
- Change and repetition over time
- Frequency and spacing of entries
- Words, themes, or imagery from optional text
- Seasonal context
- A stable personal style preference, if introduced later

Absence of entries should be treated as absence of information, not as a negative mood.

### Potential transformations

- Color palette
- Shape language
- Density and negative space
- Texture
- Rhythm and repetition
- Layering
- Direction and movement
- Organic versus geometric form

Each transformation needs an understandable design rationale. The mapping does not need to be shown constantly, but it should be documented and consistent enough to maintain trust.

### Output requirements

Each seasonal result should be:

- Visually compelling on its own
- Distinct from earlier pieces
- Cohesive with the wider scrapbook
- Reproducible or safely stored
- Exportable at useful quality
- Accompanied by meaningful alternative text
- Free of unsafe or unwanted imagery
- Successful with sparse, ordinary, or emotionally difficult data

### Candidate generation approaches

- On-device procedural art
- Hosted generative-image model
- Hybrid system: a model creates a structured art direction or recipe, then the app renders the final piece

The current cost-oriented hypothesis is the hybrid system because model use occurs only once per season and final rendering can remain controlled and consistent. This is not yet a final technical decision.

## Scrapbook Experience

The scrapbook should feel collected rather than populated. Its design should communicate time, continuity, and ownership.

Areas to explore:

- Chronological book, gallery wall, stack, or material archive metaphor
- Portrait, square, or flexible artwork format
- Whether every season has a dedicated page
- How unfinished or current seasons appear
- How titles, dates, and reflection text coexist with the art
- Whether the scrapbook has a cover or evolves visually over time
- Exporting one piece versus exporting a collection

The metaphor should guide interaction and motion without becoming decorative friction.

## Tone and Language

The voice should be:

- Warm but not sentimental
- Poetic in small amounts, especially around reveals
- Direct when explaining privacy, errors, and controls
- Non-clinical and non-diagnostic
- Nonjudgmental about moods, frequency, and gaps
- Careful not to claim that generated art reveals a hidden truth

Interpretive language should use framing such as “inspired by” or “reflecting patterns in” rather than declaring what a season meant.

## Accessibility Foundations

- Mood choices require text labels or equivalent semantic names; color and shape may reinforce meaning but cannot carry it alone.
- Interactive targets should be at least 44 by 44 points.
- Core flows must support VoiceOver, Voice Control, Dynamic Type, and keyboard or switch-based navigation where applicable.
- Layout must remain understandable at large text sizes without clipping or hiding actions.
- Reveal animations need a Reduce Motion alternative that preserves emotional pacing without large movement.
- Materials and overlays need usable Reduce Transparency and Increased Contrast behavior.
- Generated artwork needs a concise visual description and should allow the user to inspect any accompanying interpretation as text.
- Calendar state cannot rely only on dots, hues, or spatial position.
- Custom gestures must have visible or accessible alternatives.
- Accessibility claims will be tested on real screens before they are treated as complete.

## Privacy and Trust

### Current principles

- Store daily entries locally by default where practical.
- Send only the minimum information required if a remote model is used.
- Do not embed secret API credentials in the iOS application.
- Explain whether text leaves the device before the user enables remote processing.
- Give the user control over deletion and export.
- Avoid using private reflections to train external models unless the user gives informed, explicit consent.
- Keep generated artwork available even if the original generation service later changes.

### Open privacy decisions

- Whether an account is needed at launch
- Whether optional sync uses iCloud or another backend
- Whether raw journal text is ever sent to a model
- Whether local text processing can extract themes before a smaller summary is sent
- Retention policy for remote requests and generated assets
- Whether sensitive-entry filtering or exclusions are user-controlled

## Product Tensions to Resolve

### Routine versus ceremony

Daily interaction must be quick, while the seasonal reveal needs emotional weight. The product should not make every action theatrical or make the central ceremony feel ordinary.

### Interpretation versus projection

The art should feel connected to the user’s season without claiming a level of psychological understanding the system does not possess.

### Variety versus continuity

Each piece needs surprise, but the scrapbook should still look like one personal collection rather than unrelated model outputs.

### Abstraction versus recognizability

Abstract work may protect privacy and support emotional complexity. More recognizable imagery may create stronger immediate attachment but can feel overly literal or introduce unwanted associations.

### Simplicity versus emotional nuance

The input must remain lightweight without flattening feelings into a small set of simplistic labels.

### Personalization versus control

Personalized artwork can feel intimate, but too much opaque adaptation may reduce trust and visual coherence.

## Success Criteria

Initial success should be assessed through experience quality, not maximum engagement.

- A user understands the premise without a lengthy explanation.
- A check-in feels easy on both simple and emotionally complicated days.
- Missing days do not make the user feel punished.
- The user recognizes a meaningful connection between a season and its artwork.
- The artwork feels worth keeping or revisiting.
- The scrapbook becomes more valuable as pieces accumulate.
- The user understands what data is stored and where model processing occurs.
- Core interactions remain usable with relevant accessibility settings enabled.
- The experience remains coherent when the network or generation service is unavailable.

## Confirmed Decisions

- The project is named Project Pothos.
- App versus website remains an open platform decision.
- The core daily content is mood plus optional simple text.
- A calendar provides access to the user’s history.
- Collected data produces one artwork per season.
- Completed artwork is kept in a scrapbook.
- Design and user experience are primary product concerns.
- Model usage is infrequent, so the architecture should avoid unnecessary recurring inference cost.
- The initial product should remain simple and focused.
- Calm and creative maturation are central to the product; the seasonal wait is intentional.
- The seasonal artwork remains the primary reveal rather than being previewed through daily mini-artworks.
- Thoughtful and detailed design should be visible throughout the product, including ordinary and non-ideal states.
- Books provide a shared interaction theme, while the daily folio and image scrapbook remain distinct designed objects.

## Working Hypotheses

- Daily data should be local-first.
- Text should remain optional.
- There should be no punitive streak mechanic.
- Artwork should be presented as an interpretation, not an emotional diagnosis.
- A hybrid art system may offer the best balance of cost, consistency, privacy, and uniqueness.
- Users should be able to receive a meaningful seasonal artifact even with sparse data.
- The scrapbook should be a first-class experience rather than a utility gallery.
- Daily value should come from a calming pause, emotional naming, and memory—not gamification.
- Saving an entry should feel like placing a small contribution into a sealed seasonal collection.
- An optional weekly review may add near-term value without producing an automated summary.
- A two-dimensional field built from two season-specific pigments may be more distinctive and better connected to the art system than a conventional list of mood words.
- A seasonal folio with an almanac-style index may give the diary notebook-like care without literal skeuomorphism.
- A short daily epigraph may add reflective value if it remains curated, optional, and emotionally non-prescriptive.
- The seasonal color field should be secondary to the diary page rather than dominating the landing experience.

## Open Questions

### Product identity

- What exact emotional need should the app own?
- Is the app primarily a journal, an art experience, a keepsake, or a ritual?
- What should a user say when describing it to a friend?
- Is “season” literal, symbolic, or customizable?

### Daily interaction

- What is the right emotional vocabulary?
- Can a user select more than one mood?
- Should mood intensity be collected?
- How short should text be encouraged to remain?
- Can users add entries retroactively?
- How should edits affect already generated artwork?

### Calendar

- What information should be visible before opening a day?
- How should days with mixed moods appear?
- Should current-season progress be visible?
- How can the calendar feel expressive without becoming visually noisy?

### Seasonal timing

- What defines a season and its boundaries?
- Should the first season last a complete fixed period from the first entry, or end at the next natural seasonal boundary?
- Does art generate automatically or after user confirmation?
- What happens when a user joins near the end of a season?
- Can the user postpone or regenerate a piece?
- Is one final artwork immutable, or can variants exist?

### Artwork

- What visual medium best fits the product: painting, collage, printmaking, textile, generative geometry, or another system?
- Should users choose an art style or should the product have one strong art direction?
- How directly should journal text influence imagery?
- How can difficult text be handled respectfully?
- How much explanation should accompany each piece?
- Should the user be able to hide specific entries from generation?

### Scrapbook

- What material or spatial metaphor should organize the collection?
- Can users add their own captions after a reveal?
- Should entries be accessible from the finished artwork?
- How should artwork be exported, printed, or shared?
- Should sharing exclude all underlying mood data by default?

### Privacy and data

- Is the app usable without an account?
- Is cross-device synchronization necessary for the first release?
- Can the art pipeline avoid sending raw text off-device?
- What exactly is retained by any model provider?
- What happens to past pieces if the user deletes source entries?

### Business model

- Is the app paid once, subscription-based, or free with paid seasonal creation?
- Does payment fund model generation, premium scrapbook features, physical prints, or style collections?
- How can monetization avoid distorting the reflective experience?

### Validation

- Which assumptions require interviews before interface design begins?
- What should be tested with a paper or interactive prototype?
- What makes an artwork feel personally connected rather than randomly attractive?
- How many seasons must be represented in a prototype to evaluate the scrapbook concept?

## Decision Log

| Date | Decision | Status | Rationale |
| --- | --- | --- | --- |
| 2026-09-27 | Name the project Project Pothos | Confirmed | Expresses the intended theme of longing to feel whole |
| 2026-09-27 | Reopen the platform choice between an app and a website | Open | User has not selected a platform |
| 2026-09-12 | Begin with a focused iOS mood, text, calendar, seasonal art, and scrapbook experience | Platform decision superseded 2026-09-27 | Product concept remains under exploration; iOS is no longer a confirmed requirement |
| 2026-09-12 | Treat design exploration as a documented phase before implementation | Confirmed | Core emotional and interaction decisions will shape the technical system |
| 2026-09-12 | Consider local-first storage and infrequent model use | Working hypothesis | Supports privacy and a cost-effective usage pattern |
| 2026-09-12 | Include accessibility constraints in early concept development | Confirmed | Color, motion, mood semantics, and generated art are fundamental to the experience |
| 2026-09-12 | Treat craft at every scale as a product principle | Confirmed | The diary must provide a considered experience long before the first seasonal artwork exists |
| 2026-09-12 | Explore color and material as the primary mood language | Working hypothesis | A visual-first input may feel more personal, artistic, and connected to seasonal creation than generic mood labels |
| 2026-09-12 | Explore one stable two-dimensional emotional field rendered through a different palette each season | Working hypothesis | Preserves a learnable interaction while making the seasons materially present in daily use |
| 2026-09-12 | Define each seasonal field through two related pigments | Working hypothesis | Creates a stronger seasonal identity and a more disciplined field than a multicolor gradient |
| 2026-09-12 | Refine the seasonal anchors toward pea green, baby blue, red-orange, and a lighter mulberry | Working hypothesis | Brings each pair closer to the intended seasonal character while preserving the two-pigment system |
| 2026-09-12 | Give light and dark appearances separate tonal variants of each seasonal pair | Working hypothesis | Allows pastel pigment-on-paper fields in light mode and richer luminous fields in dark mode while preserving hue identity |
| 2026-09-12 | Explore a Seasonal Folio with an Almanac Index as the diary format | Working hypothesis | Connects daily studies, calendar history, seasonal closure, and finished artwork through one material metaphor |
| 2026-09-12 | Use a minimal daily frontispiece before opening the diary page | Working hypothesis | Creates a calm threshold while moving color selection out of the landing-page hierarchy |
| 2026-09-12 | Treat the folio and scrapbook as distinct books connected by page-based navigation | Working hypothesis | Preserves thematic unity without applying one visual treatment to every part of the app |
| 2026-09-12 | Explore a short daily epigraph on the landing page | Working hypothesis | Adds an immediate contemplative reason to open the app without turning the page into a dashboard |
| 2026-09-12 | Make creative slowness and a season-long wait part of the product essence | Confirmed | The artwork should represent a lived period rather than instant generation |
| 2026-09-12 | Preserve one major seasonal reveal instead of showing daily artwork previews | Confirmed | Protects anticipation and keeps daily use focused on reflection |
| 2026-09-12 | Explore a pause, mood, optional trace, and closing ritual as the daily loop | Working hypothesis | Provides immediate value without relying on rewards or analysis |

## Next Design Focus

The product essence is now clearer: calm, emotional attention, creative maturation, and a reveal that cannot be rushed. The current mood-input direction is a season-specific two-dimensional color field. The next useful decisions are:

- The two stable emotional dimensions
- The field’s interaction and accessible equivalent
- The art direction for the first seasonal palette
- The optional writing prompt and length
- The exact save or “place into season” interaction
- What the Today screen shows before and after an entry

This flow should be prototyped before the calendar and seasonal reveal are visually finalized because it establishes the app’s most frequent interaction language.
