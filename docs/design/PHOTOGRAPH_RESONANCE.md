# Personal photographs and emotional resonance

## Status

- Recorded: 2026-10-01
- Stage: tentative long-term product direction; subject to change
- Source: owner discussion following the [tentative roadmap](ROADMAP.md)
- This is a decision record, not an implementation-ready feature brief. No implementation is authorized by this document.

## Intended value

Connect the user's emotional experience with the creator's personal photographic archive. The photograph should reflect the user's feelings, while its accompanying material shares the creator's perspective and personal context.

## Owner-stated direction

- Explore a seasonal sentiment profile/graph and a longer-term yearly profile/graph that produce a meaningful output. Their representation and exact output remain undecided.
- Use a curated library of the creator's personal photographs mapped to emotional profiles.
- A photograph should reflect the user's feelings. Selecting a comforting response instead is not the stated matching intent.
- Attach personal context to each photograph: details, thoughts, advice, date, place, or similar material. Required fields and presentation remain open.
- A photograph must be within an acceptable emotional similarity radius to qualify. Do not always select the nearest photograph regardless of fit.
- If no photograph qualifies, use a different solution that has yet to be designed. Do not force a match.

These points record the owner's current direction, not a finalized release commitment. Earlier documents describing personal photos as merely an unspecified possibility predate this exploration; the broader artwork approach is still not finalized.

## Matching concept

The proposed technical interpretation is matching with a rejection threshold. In a defined emotional representation, a photograph qualifies only when its distance from the user's profile is within an accepted radius. Clustering is not required to implement that rule.

No emotional dimensions, distance function, numerical radius, embedding model, or clustering algorithm has been chosen. The rule for choosing among several eligible photographs is also unresolved.

## Input constraint

The current [daily color selection brief](../features/FEATURE_DAILY_COLOR_SELECTION.md) gives colors no fixed emotional labels. Those selections alone do not establish that a user felt a particular emotion. This discussion does not approve changing that daily interaction or silently interpreting its colors as emotion categories.

The source of the user's emotional profile must be decided before emotional distance can be meaningful. Explicit user reflection, optional emotional input, and interpretation of optional writing were discussed as possibilities; none was selected.

## Suggestions discussed, not approved

- Let users confirm a seasonal reflection as an input to matching.
- Begin with manually annotated photos and simple local matching rather than requiring a custom model or remote inference.
- Preserve mixed feelings and changes over time instead of reducing a season to a single average; treat missing days as unknown.
- Distinguish insufficient information from having enough information but no qualifying photograph.
- Let users reject a match or choose among eligible photographs.
- Present the creator's context separately from the user's experience, without implying their experiences are identical.
- Frame advice as the creator's perspective and consider making it optional.
- Preserve a useful seasonal record when no photograph qualifies, without silently expanding the radius.
- Consider a yearly collection of seasonal keepsakes rather than another single-image match. This is an alternative, not the owner's selected yearly output.
- Preserve an already selected keepsake when catalogue contents or matching rules later change.

## Open decisions

- What information represents the user's feelings, and how does the user control or confirm it?
- How are photographs annotated, including multiple or mixed emotional associations?
- What emotional dimensions and distance measure support meaningful comparisons?
- Is the radius global or specific to photographs or emotional regions, and how will its usefulness be evaluated?
- What happens when multiple photographs qualify, including previously received photographs?
- What is the no-match experience, and what is the insufficient-information experience?
- How do seasonal and yearly profiles differ, and what does each produce?
- Are graphs visible to users or only internal matching representations?
- How are advice and personal context presented without claiming certainty about the user's feelings?
- What journal information is processed locally or remotely, and what personal photo metadata is intentionally published?
- Does photography replace, supplement, or become source material for the earlier seasonal-art concept?

## Next step

Pause for the owner's reflection. Before building, resolve the profile input and output intent, then create a dedicated feature brief with states, privacy boundaries, and verifiable acceptance criteria. No prototype or emotional-matching validation has been completed for this direction.
