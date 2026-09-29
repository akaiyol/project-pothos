# Project Skills

This file records the agent skills intentionally installed for Project Pothos. Skills are project-scoped under the repository-root `.agents/skills/` and should be added only when the product or implementation needs them.

## Installed source snapshots

| Source | Version or commit | Installed content | License | Executable files |
| --- | --- | --- | --- | --- |
| [dpearson2699/swift-ios-skills](https://github.com/dpearson2699/swift-ios-skills) | `3.9.1`, commit [`8d90fd1`](https://github.com/dpearson2699/swift-ios-skills/commit/8d90fd121a263355a4fb44fd082af1416a5c1c2a) | Sixteen Swift and iOS skills | PolyForm Perimeter 1.0.0; see [third-party notices](../../.agents/skills/THIRD_PARTY_NOTICES.md) | None |
| [anthropics/skills](https://github.com/anthropics/skills) | commit [`8a1541c`](https://github.com/anthropics/skills/commit/8a1541c4a3ffa5a20a5a91de0dcf3f0bab1d1ef4) | `frontend-design` | Apache 2.0; bundled in the skill directory | None |

All skills are installed at project scope. The original ten Swift/iOS skills were installed on 2026-09-12; the audited additions were installed on 2026-09-29.

## Installed skills

| Skill | Role in this app | Use when | Status |
| --- | --- | --- | --- |
| `swiftui-patterns` | Establishes modern state ownership, view composition, dependency injection, previews, and loading/error states. | Structuring or reviewing SwiftUI screens and shared state. | Installed |
| `swiftui-layout-components` | Guides grids, lists, forms, scroll views, controls, and adaptive layouts. | Building the mood entry, calendar, and scrapbook interfaces. | Installed |
| `swiftui-animation` | Provides motion patterns with accessibility-aware fallbacks. | Designing seasonal artwork reveals, transitions, or interaction feedback. | Installed |
| `swiftdata` | Defines persistence, queries, relationships, migrations, and optional CloudKit synchronization. | Storing mood entries, notes, seasons, artwork metadata, and scrapbook records. | Installed |
| `natural-language` | Covers local language identification, sentiment, tokenization, tagging, and embeddings. | Evaluating whether journal text can be summarized locally without sending raw entries to a server. | Installed |
| `apple-on-device-ai` | Provides a decision framework for Foundation Models, Core ML, MLX Swift, and local fallbacks. | Selecting or implementing the seasonal art-recipe model path. | Installed |
| `ios-accessibility` | Covers VoiceOver, Dynamic Type, contrast, reduced motion, focus, and accessibility testing. | Designing, implementing, or auditing any user-facing experience. | Installed |
| `swift-testing` | Establishes unit and integration testing patterns using Swift Testing and appropriate XCTest boundaries. | Testing seasonal aggregation, persistence, model output validation, and failure behavior. | Installed |
| `ios-networking` | Guides `URLSession`, async networking, retries, caching, errors, and background transfers. | Connecting to a hosted model or synchronization service. | Installed |
| `swift-security` | Covers Keychain, CryptoKit, secrets, authentication, certificate trust, and mobile security review. | Handling credentials, private journal data, authentication, or a hosted-model connection. | Installed |
| `swift-architecture` | Selects the smallest maintainable architecture and defines state, dependency, and test boundaries. | Establishing the app structure or deciding when a feature has outgrown simple SwiftUI MV. | Installed |
| `swift-concurrency` | Covers actor isolation, `Sendable`, structured concurrency, cancellation, and Swift 6 diagnostics. | Implementing background work, model calls, persistence coordination, or resolving data-race warnings. | Installed |
| `swiftui-navigation` | Defines `NavigationStack`, tabs, sheets, routing, and deep-link patterns. | Connecting the daily diary, calendar, seasonal artwork, and scrapbook without ad hoc navigation state. | Installed |
| `swiftui-gestures` | Covers accessible tap and drag interactions, gesture state, composition, and conflict resolution. | Implementing the two-dimensional color selector and later user-approved page interactions. | Installed |
| `swiftui-performance` | Provides code-first performance review, Instruments guidance, and measured remediation. | Preventing slow grids, broad view invalidation, expensive rendering, or animation hitches. | Installed |
| `ios-simulator` | Covers repeatable simulator setup, app launch, permissions, screenshots, logs, and device boundaries. | Building and visually verifying supported iPhone sizes and interaction states. | Installed |
| `frontend-design` | Adds subject-specific art direction, typographic discipline, restraint, and anti-template critique. | Ideating or reviewing visual directions before a native implementation is approved. | Installed |

## External audit — 2026-09-29

| Source | Finding | Decision |
| --- | --- | --- |
| [openai/skills](https://github.com/openai/skills) | The repository is deprecated and redirects current Codex skill and plugin examples to `openai/plugins`. | Do not add new project skills from the deprecated catalog. |
| [openai/plugins](https://github.com/openai/plugins), commit [`5fd93af`](https://github.com/openai/plugins/commit/5fd93af4cd0c623e020d0cc7e9ce178b4ac1f70f) | `build-ios-apps` is directly useful once an Xcode project exists because it adds XcodeBuildMCP-backed build, simulator, profiling, leak, and debugging workflows. Its overlapping SwiftUI reference skills are narrower than the current standalone Swift set. | Recommend the complete plugin at implementation time; do not detach or duplicate its overlapping skills now. |
| [openai/plugins](https://github.com/openai/plugins), same snapshot | Figma is useful when Project Pothos needs editable design files, collaboration, and design-to-SwiftUI handoff. `superpowers` substantially duplicates the repository's required feature and verification workflow. | Use the connected Figma plugin for approved design-file work; do not add `superpowers`. |
| [anthropics/skills](https://github.com/anthropics/skills), commit [`8a1541c`](https://github.com/anthropics/skills/commit/8a1541c4a3ffa5a20a5a91de0dcf3f0bab1d1ef4) | `frontend-design` adds a strong anti-generic design critique that complements the project rules. `doc-coauthoring` duplicates the feature-brief workflow. `algorithmic-art` and `canvas-design` are tied to web/static-art artifact workflows rather than native iOS rendering. | Install only `frontend-design`. |
| [anthropics/claude-code](https://github.com/anthropics/claude-code), commit [`684800b`](https://github.com/anthropics/claude-code/commit/684800b206824dfd0cc8a876e8604b20f72c3617) | The `frontend-design` plugin contains the same skill already installed from `anthropics/skills`. `feature-dev` duplicates the repository's brief-first workflow. Code-review and security plugins become useful after production code and pull requests exist; security guidance also sends diffs to a configured model endpoint. | Do not install a Claude Code plugin now. Re-evaluate review tooling after the production project exists. |

No installed skill was replaced. The existing Swift skills match the latest inspected upstream commit and remain the stronger standalone source for the areas they cover.

## Connected design tooling

| Tool | Project role | Boundary |
| --- | --- | --- |
| Figma plugin | Creates and edits approved Figma design files, supports design-system work, and provides SwiftUI handoff workflows. | Use only when a task calls for Figma output or design-to-code translation. Keep product decisions and feature briefs in the repository as the source of truth. |

Figma's plugin-provided skills remain managed by the plugin and are not copied into `.agents/skills/`.

## Selection policy

- Use the fewest skills needed for the current task.
- Treat Apple documentation and the local Xcode toolchain as authoritative for API availability.
- Check deployment-target compatibility before adopting iOS 26 or Swift 6.3-only guidance.
- Keep journal content local unless the product explicitly requires remote processing.
- Audit a third-party skill's `SKILL.md`, references, scripts, license, and source revision before adding it.
- Record every addition, update, disablement, or removal in this file.

## Deferred skills

These areas may justify additional skills or plugins after the app's deployment target and first implementation scope are approved:

- Debugging, Instruments, and MetricKit
- Localization
- App Store review and release readiness
- CloudKit synchronization
- Core ML implementation if the chosen model path requires it
- XcodeBuildMCP workflows through the complete `build-ios-apps` plugin

## Change log

| Date | Change |
| --- | --- |
| 2026-09-12 | Added the initial ten Swift/iOS skills from `swift-ios-skills` version 3.9.1. |
| 2026-09-29 | Audited current OpenAI, Anthropic, Claude Code, and Swift iOS sources. Added six missing Swift/iOS foundations and Anthropic's `frontend-design`; retained all existing skills and deferred plugin installation. |
| 2026-09-29 | Connected the Figma plugin for optional design-file creation, design-system work, and SwiftUI handoff. Kept its managed skills separate from the project-scoped skill set. |
