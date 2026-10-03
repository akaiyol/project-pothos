# Feature Brief: Seasonal Ecosystem

Updated: 2026-10-03. Status: concept definition before screen-map and visual prototyping. Direction is owner-confirmed; detailed behaviour below is proposed or unresolved. Platform and first-release scope are undecided. Documentation only; no implementation authorization.

## Problem and user value

A traditional diary does not express the owner's intended experience. Daily colour contributions should form a personal seasonal environment; emotional patterns may bring symbolic visitors into that environment. History supports recall, while the ecosystem makes accumulated contributions visible.

## Goals and non-goals

Goals: retain lightweight colour entry, contribution history, and thoughts input; translate contributions into seasonal foliage; define a sentiment graph and pattern-driven bug/animal visitors; record visitors in a catalogue; explore a 5% shiny colour variant.

Non-goals: revive seasonal artwork reveals, scrapbook/photo matching, or mandatory notebook styling; implement production behaviour; diagnose emotions; assign fixed mood labels to colours; add scores, streaks, social features, or unrequested effects.

## Confirmed requirements

- Screen one contains colour selection, contribution history, and thoughts/feelings input.
- Compare rim wheel, 2D colour field, and two-colour gradient; selector remains unresolved.
- Colour selection leads to a history contribution; one contribution corresponds to one leaf cluster.
- Screen two contains a cyber-nature tree using contribution colours for leaves and flowers.
- Four seasonal sections/branches; spring has leaves and flowers, other seasons have differing foliage to design.
- Bugs represent simple emotions; animals represent complex emotions; visitors have a catalogue.
- Sentiment patterns can cause ecosystem life to appear. Graph is desired; placement and dimensions remain open.
- Requested shiny probability is 5%, producing a different colour; event semantics remain open.

## Information hierarchy and flow

Screen one: daily colour action, thoughts input, chronological history, one clear persistence state. Exact layout is unresolved.

Screen two: tree and seasonal sections, contribution-derived leaf clusters, visitors. Catalogue entry point and graph location require review; no new navigation is selected.

Intended loop: choose colour → record in history → add corresponding leaf cluster → evaluate eligible emotional evidence over time → show a qualifying visitor → preserve visit in catalogue. The final three steps cannot be specified as deterministic behaviour until sentiment and visitor rules are agreed. Colour-only entries still contribute foliage without requiring emotional inference.

## Data and meaning

| Object | Meaning | Decisions needed |
| --- | --- | --- |
| Contribution | A recorded daily colour and optional thought | Save boundary, date/timezone, single/two-colour representation, edits/deletion. |
| Leaf cluster | One contribution's tree representation | Stable association, position, size, colour transfer, seasonal foliage. |
| Season section | A seasonal group of branches | Regional dates, hemisphere, year rollover and multi-year display. |
| Sentiment evidence | Tentative emotional information separate from chosen colour | Source, consent, dimensions, confidence and correction. |
| Pattern | A temporal condition over usable evidence | Window, thresholds, gaps, mixed signals and repeat triggers. |
| Visit | A symbolic bug or animal appearance | Species mapping, duration, repeat visits, retention and correction. |
| Shiny variant | Alternate creature colour | Whether per spawn/visit/species; draw persistence and reroll policy. |
| Catalogue record | A creature that has visited | Fields, grouping, variant display and deletion rules. |

Five generally happy days is an illustrative trigger. Candidate mappings are ladybug—happy-go-lucky, butterfly—sadness, rabbit—turmoil, hedgehog—uncertainty. These are authored metaphors to review, not validated psychological classifications. Polarity alone is insufficient for the complex-emotion taxonomy.

## States to specify before implementation

- Empty: no contributions, no inferred sentiment, no fabricated visits; initial tree appearance unresolved.
- Partial: sparse history generates only actual contribution clusters; insufficient evidence does not imply a negative emotion.
- Recorded: history and tree refer to the same contribution and saved colour.
- Loading/processing: recorded entries remain visible while inference or rendering is pending; no duplicate events.
- Error/offline: preserve input; distinguish persistence failure from unavailable inference. Recovery design depends on platform/storage.
- Uncertain/mixed evidence: avoid a definitive emotion claim or forced creature assignment; user correction path unresolved.
- Edit/delete: define linked cluster, graph, inferred pattern, visit and catalogue effects before building.
- No visitors: catalogue and ecosystem remain meaningful without eligible sentiment patterns.

These are specification obligations, not verified product states.

## Layout, appearance and accessibility

Seasonal nature and glassmorphism define the direction. Obsidian-like dark glass trunk/branches are proposed. Foliage and creature designs, typography, composition, and the fuller cyber treatment remain open. The thoughts interaction will be ideated later.

Future mockups must render at 320, 390, and 430 points; inspect all supported appearances, variants, controls and transitions. Provide a non-dragging colour input path, non-colour history/season/visitor descriptions, navigable tree/catalogue equivalents, legible contrast, and Dynamic Type/Reduce Motion plans. Do not make rare variants identifiable by colour alone.

## Privacy

Thoughts and inferred sentiment are private emotional data. Define processing location, consent, retention, user correction, export/deletion and downstream effects before implementation. No cloud analysis or model is selected. Use synthetic entries for studies. Catalogue and visitor explanations must not unintentionally expose private writing.

## Acceptance criteria for future design verification

- [ ] Reviewed screen/state map distinguishes confirmed direction, candidates and deferred scope.
- [ ] Selector alternatives appear one at a time and have an equivalent accessible path.
- [ ] One persisted contribution updates the correct history date and exactly one associated cluster; drafts do not duplicate either.
- [ ] Leaves/flowers retain recorded colours without sentiment-driven recolouring.
- [ ] Four seasonal sections and differentiated foliage are understandable, including sparse seasons.
- [ ] Sentiment source, graph dimensions, confidence, time-window and gap rules are documented and tested against reviewed synthetic cases.
- [ ] Bug/animal taxonomy and trigger/lifecycle rules are approved; difficult or uncertain emotions are not treated as failure.
- [ ] Shiny eligibility event is defined as 5%; persistence prevents unintended repeat rolls, and the variant is accessible.
- [ ] Catalogue records actual visits according to approved edit/delete and repeat-visit rules.
- [ ] Empty, partial, recorded, processing, failure, uncertain and edit/delete states are specified.
- [ ] Affected mockups pass rendered review at 320/390/430 and supported appearances; controls and alternative input are exercised.
- [ ] Platform, release scope, processing/privacy boundaries and implementation authorization precede production work.

All criteria are unchecked. This document does not establish visual or algorithmic validation.

## Open decisions

Priority for the next map: save boundary; season/year organization; catalogue and graph placement; sentiment evidence source. Later studies resolve selector form, richer thoughts interaction, foliage/material design, complete creature taxonomy, thresholds, visitor lifecycle, and shiny roll semantics.

See [direction](../design/APP_DESIGN.md), [roadmap](../design/ROADMAP.md), and [timeline](../design/DIRECTION_TIMELINE.md).
