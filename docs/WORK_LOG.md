# Project Pothos — work log

Repository record of non-sensitive progress and direction. Append a dated entry for each meaningful session: work completed, confirmed direction, open questions, verification, and next step. Record whether the public snapshot changed and why. Distinguish proposals from approved decisions; do not invent past progress or store secrets here.

## 2026-09-27 — Identity and public presentation

### Confirmed direction

- Name: Project Pothos.
- Public framing: my personal art project, with an emphasis on design and an eventual connection to personal material.
- The README is for visitors and must not surface indecision.
- Its approved introduction stays fixed; meaningful snapshots update the content below it.
- Progress and direction belong in this separate log.

### Work completed

- Drafted a personal introduction and a notebook-study snapshot.
- Added README editorial rules and ignore patterns for private material, working documents, credentials, caches, and builds.

### Open questions

- Introduction wording awaits approval.
- App versus website remains undecided.
- Personal source material is undecided; photos are a possibility, not a requirement.

### Verification and publication

- The local repository has no commits or tracked files.
- Remote contents could not be retrieved through the web tool; no remote audit is claimed.
- Draft remains local; no commit or push was made.

### Next step

Review the README voice and introduction before publishing the first snapshot.

## 2026-09-27 — Personal introduction and curated features

- Replaced the prior conceptual introduction with the owner's values: colours, beautiful things, and sharing life and memories. Preserved “More to come!” as part of the fixed introduction.
- Removed “On the page”; drafted a short history-grid feature description.
- Updated guidelines: one or two ranked features, no third slot, replacements must be more interesting and better designed, and future README changes require permission. This supersedes the earlier automatic-refresh direction.
- Screenshot remains pending: located the existing history-grid HTML, but local Playwright has no installed browser and Google Chrome is unavailable. No image link was added and no visual verification is claimed.
- No commit or push made. Next step: capture and inspect the actual history-grid image for this feature.

## 2026-09-27 — Name definition

- Added the definition of Pothos directly beneath the README title, distinguishing its literal meaning from the project interpretation.
- Preserved the introduction and feature description. Updated README guidelines to retain this placement.

## 2026-09-27 — Owner copy and README formatting

- Preserved the owner's new introduction verbatim and synchronized the fixed introduction in process/README_GUIDELINES.md.
- Added spacing below the title, italicized the definition, and made Feature highlight a section heading above the feature title.
- Checked screenshot status: assets/ contains no image and the README has no image reference. Screenshot publication remains pending; nothing was pushed.

## 2026-09-27 — First GitHub publication

- Published README.md and .gitignore to akaiyol/project-pothos on main, commit 523d3ca.
- Private working documents and local instructions remain ignored.
- Used a GitHub noreply commit email. Screenshot remains pending and was not published.
- Push succeeded; local tracked working tree is clean.

## 2026-09-27 — Publish non-sensitive project content

- Owner clarified that all non-sensitive project content belongs in the repository. This supersedes earlier local-only rules for working documents.
- Included design briefs, ideas, README guidelines, work log, AGENTS.md, skill inventory, and project-scoped skill resources.
- Retained exclusions for credentials, private source material, machine-local settings, dependencies, and generated build output.
- Reviewed content for credential patterns and local paths; flagged skill references were explanatory security examples rather than secrets.
- The history-grid screenshot still does not exist in the project and is not part of this publication.

## 2026-09-27 — Repository organization

- Grouped design studies, feature briefs, and process guidance into docs/design/, docs/features/, and docs/process/. Moved the work log to docs/WORK_LOG.md.
- Added docs/README.md as the contributor index and updated document references.
- Preserved the public README and kept AGENTS.md and .agents/skills/ at discovery-compatible locations.
- No production scaffold or platform commitment was introduced.
- Verified local Markdown links after the moves.

## 2026-09-27 — Routine small-change publishing

- Owner requested that small changes always be pushed after completion and verification. Recorded this standing instruction in AGENTS.md.
- Prepared the documentation reorganization and publishing rule for commit and push. README content approval rules remain unchanged.

## 2026-09-27 — README history-grid screenshot

- Captured the existing history-grid prototype using sample data and added assets/history-grid.png.
- Linked the image beneath the README feature title without changing the introduction or feature description.
- Inspected all 12 captures: long and short date ranges at 320, 390, and 430 points with light and dark host backgrounds. The exported image uses the long April–October view.
- The standalone snapshot has no visible interactive controls; no product interaction behavior was changed.
- Checked the PNG and relative image path before publication.

## 2026-09-29 — Agent skill and plugin audit

### Work completed

- Audited the latest available snapshots of `openai/plugins`, `anthropics/skills`, `anthropics/claude-code`, and `dpearson2699/swift-ios-skills` against the app's design and implementation needs.
- Confirmed that the installed Swift/iOS source is still at the latest inspected upstream commit; no existing skill required replacement.
- Added six missing Swift/iOS foundations: architecture, concurrency, navigation, gestures, performance, and simulator workflows.
- Added Anthropic's `frontend-design` skill for subject-specific visual direction and anti-template critique.
- Added third-party source, revision, and license notices.

### Plugin findings

- `build-ios-apps` is the most valuable Codex code plugin once the Xcode project exists because it adds simulator, build, debug, performance, and leak tooling through XcodeBuildMCP.
- Figma is the most useful optional design integration when editable files or collaborative handoff become necessary.
- Claude Code's `feature-dev` duplicates the repository's feature-brief workflow; its review and security plugins are deferred until production code exists.
- No plugin was installed or connected during this audit.

### Verification and publication

- Verified every added skill has a readable `SKILL.md` and that no added skill contains executable files.
- Kept the public README unchanged.
- The unfinished daily color-selector prototype remains outside this audit's publication scope.
