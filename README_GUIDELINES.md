# README guidelines

## Purpose and voice

The README introduces Project Pothos to someone discovering it for the first time. It is a personal art project, centred on the owner's love of colours, beautiful things, and sharing pieces of life and memory. Write warmly, simply, and with restrained whimsy. Do not invent personal stories or use product-marketing language.

Keep it short. The scope can change at any time, so do not define a fixed product, platform, roadmap, or detailed feature inventory. Keep indecision, internal planning, and progress history out of the README.

## Definition beneath the title

Keep this line directly beneath the project title, before the fixed introduction:

*Pothos (πόθος): longing or yearning. Here, a longing to feel whole.*

The first sentence defines the word; the second gives the project’s interpretation.

## Fixed introduction

Preserve the following introduction verbatim in future updates. Change it only if the owner explicitly requests an introduction revision:

Some emotions can't be described with words but only with the colours of the changing seasons.

More to come.

## Featured work

- Put one or two interesting features directly beneath the introduction. Do not add an “On the page” section.
- Give each feature a short title, a real screenshot, and one or two brief sentences about what makes it interesting.
- Present the strongest feature first. Rank candidates by how interesting they are and how well they are designed; recency alone does not earn a place.
- A second feature may be added with the owner's permission.
- Never grow the list to three. A third candidate can replace an existing feature only if it is more interesting AND better designed than that feature, and the owner approves the replacement.
- Describe a study as a study, without implying that it is a shipped product.
- Do not add placeholder images, broken links, or invented screenshots. If an image cannot be captured and checked, record that gap in the work log and report it to the owner.

## Permission and timing

- Updates are ad hoc, not automatic or scheduled.
- When a worthwhile snapshot emerges, propose the exact image, short description, and any replacement to the owner. Obtain permission before changing the public README feature selection or copy.
- An explicit request to update the README authorizes that requested edit; it does not authorize future updates or publishing.
- Preserve the introduction during feature updates. Do not silently rewrite it for a new scope.
- Record routine progress, direction changes, alternatives, and proposed README candidates in WORK_LOG.md without turning them into public copy.

## Images and publication

- Use actual rendered screenshots of the feature. Follow AGENTS.md visual verification requirements for mockups and report any incomplete verification.
- Use repository-relative image paths and useful alt text. Keep approved public exports in assets/.
- Review images for private content and metadata, and review staged files and diffs before publishing.
- Keep credentials, personal originals, local absolute paths, out of public content. Non-sensitive working documents belong in the repository, separate from the visitor-facing README.
- Commit these guidelines and the non-sensitive work log so they accompany a clone. Gitignore does not protect arbitrary content or remove already tracked files.
