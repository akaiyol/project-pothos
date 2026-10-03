# Version 1 static material review

2026-10-03. [Brief](../../../features/FEATURE_FIGMA_V1_MATERIAL.md).

Changed the Figma background to cool grey with a slight blue tone, white edge highlights, separation shadow and a soft diagonal reflection. Randomized 182 opaque sample diary cells using the original prototype gold, blue, peach and mauve anchors with interpolated shades and varied depth. Preserved the existing composition and copy.

Inspected [six static renders](static-widths.png): left to right 320, 390, 430 points; light surroundings above, dark below. Width fixtures adapt calendar geometry and picker containers without shrinking text. No overlap or clipping observed. Reflection remains below content and opaque diary colours. Small existing labels and secondary copy remain for this scoped pass; accessibility completion is not claimed.

These temporary Figma width fixtures do not prove automatic responsiveness. Removed fixtures after capture. No interactions or state transitions were implemented or tested. Complex UX, motion, physical refraction and native accessibility remain deferred.

Next: owner reviews glass appearance and graph palette; incorporate explicit feedback within the simple mockup scope.

## Owner correction: simple gradient and wheel palette

Owner rejected the sheen as silk-like and deferred glass work. Replaced it with light blue to white, removed reflection and bevel effects. Recoloured all 182 cells by sampling the current wheel gradient directly, without extra darkening or unrelated anchors. Current wheel stops are pink and pale green with intermediate shades.

Inspected [updated six static fixtures](simple-gradient-widths.png) at 320/390/430 against light/dark surroundings. No overlap or clipping observed. Existing small labels remain a legibility limitation. Original layout/wheel/copy preserved; temporary fixtures removed. Earlier screenshot is historical evidence only. Next: owner reviews this simpler mock; glass and complex UX remain deferred.
