# Project Skills

This file records the agent skills intentionally installed for this iOS app. Skills are project-scoped under `.agents/skills/` and should be added only when the product or implementation needs them.

## Source snapshot

- Repository: [dpearson2699/swift-ios-skills](https://github.com/dpearson2699/swift-ios-skills)
- Source version: `3.9.1`
- Source branch: `main`
- Source commit at installation: [`8d90fd121a263355a4fb44fd082af1416a5c1c2a`](https://github.com/dpearson2699/swift-ios-skills/commit/8d90fd121a263355a4fb44fd082af1416a5c1c2a)
- Installed: 2026-09-12
- Installation scope: project
- Executable files included: none

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

## Selection policy

- Use the fewest skills needed for the current task.
- Treat Apple documentation and the local Xcode toolchain as authoritative for API availability.
- Check deployment-target compatibility before adopting iOS 26 or Swift 6.3-only guidance.
- Keep journal content local unless the product explicitly requires remote processing.
- Audit a third-party skill's `SKILL.md`, references, scripts, license, and source revision before adding it.
- Record every addition, update, disablement, or removal in this file.

## Deferred skills

These areas may justify additional skills after the app's deployment target and first feature scope are approved:

- Architecture and concurrency
- Debugging, Instruments, and MetricKit
- Localization
- App Store review and release readiness
- CloudKit synchronization
- Visual and product design

## Change log

| Date | Change |
| --- | --- |
| 2026-09-12 | Added the initial ten Swift/iOS skills from `swift-ios-skills` version 3.9.1. |
