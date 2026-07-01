# Swift Learning Roadmap: July 1 to August 31, 2026

The goal is to rebuild Swift fundamentals in historical order, starting with a
pre-Swift-3 baseline, then studying each Swift release as a delta from the
previous version. Everything in this roadmap should be completed before
September 1 so WWDC26 can be approached with the full Swift history already in
context.

## Assumptions

- Start date: July 1, 2026.
- Deadline: August 31, 2026.
- July and August are for Swift foundations, Swift Evolution history,
  version-by-version language changes, and era-appropriate WWDC sessions.
- September is intentionally not scheduled here. It should stay open for
  WWDC26 itself, follow-up sessions, and whatever new app work becomes relevant
  after the announcements.
- Primary resources should be official sources: Swift.org, Swift Evolution,
  Apple Developer documentation, and Apple Developer videos.

## Core Rule

For each Swift era, only study material that helps explain modern Swift and
modern app development:

1. Swift basics for that era.
2. Key Swift Evolution proposals.
3. Two to four WWDC sessions from that year.
4. One app-facing exercise.
5. Notes on what old pattern the new feature replaced.
6. A dedicated WWDC note when a year's WWDC does not line up cleanly with a
   single Swift release.

Avoid trying to master every historical iOS API. The purpose is to understand
why modern Swift looks the way it does.

## Monthly Plan

| Month | Goal | Main output |
| --- | --- | --- |
| July | Rebuild Swift fundamentals from pre-Swift-3 basics through Swift 5 | Small reference app with clean models, Codable, networking, and tests |
| August | Finish modern Swift before WWDC26: SwiftUI, concurrency, macros, Observation, SwiftData, Swift Testing, Swift 6 readiness | Modernize the reference app with SwiftUI, async/await, actors, Observation/SwiftData, stricter concurrency, tests, and a pre-WWDC26 review note |

## July: Basics to Swift 5 Foundations

| Dates | Focus | Daily plan | Output |
| --- | --- | --- | --- |
| Jul 1-5 | Pre-Swift-3 basics | Jul 1: setup notes and TSPL guided tour. Jul 2: optionals, control flow, functions. Jul 3: structs, classes, enums. Jul 4: protocols and extensions. Jul 5: build tiny model layer. | `basics.md` plus a clean model-layer baseline |
| Jul 6-12 | Swift 3 and WWDC16 | Jul 6: Swift 3 API naming. Jul 7: Foundation changes. Jul 8: Swift Evolution review. Jul 9: WWDC16 Swift session. Jul 10: UIKit or iOS 10 session. Jul 11: refactor old-style APIs. Jul 12: weekly review. | One small model layer rewritten in clean Swift |
| Jul 13-19 | Swift 4 | Jul 13: Codable basics. Jul 14: custom Codable. Jul 15: key paths. Jul 16: String changes. Jul 17: WWDC17 Swift. Jul 18: add JSON import/export. Jul 19: review. | JSON import/export using Codable |
| Jul 20-26 | Swift 4.2 | Jul 20: synthesized conformances. Jul 21: `Hashable`, `Equatable`, `CaseIterable`. Jul 22: collections and random APIs. Jul 23: WWDC18 Swift. Jul 24: testing/debugging video. Jul 25: add tests. Jul 26: review. | Refactored models with conformances and tests |
| Jul 27-31 | Swift 5 | Jul 27: ABI stability concept. Jul 28: `Result`. Jul 29: raw strings and interpolation. Jul 30: WWDC19 Swift. Jul 31: build networking/data-loading layer. | Small networking/data-loading layer |

## August: Modern Swift and Swift 6 Readiness

| Dates | Focus | Daily plan | Output |
| --- | --- | --- | --- |
| Aug 1-2 | Swift 5 wrap | Aug 1: error handling and `Result` refactor. Aug 2: review Swift 3-5 timeline. | Swift 3-5 summary notes |
| Aug 3-9 | SwiftUI start | Aug 3: property wrappers. Aug 4: opaque types and `some View`. Aug 5: WWDC19 SwiftUI intro. Aug 6: data flow in SwiftUI. Aug 7: rebuild one screen. Aug 8: polish screen. Aug 9: review. | One screen rebuilt in SwiftUI |
| Aug 10-16 | SwiftUI lifecycle and SPM | Aug 10: app/scene lifecycle. Aug 11: result builders. Aug 12: Swift Package Manager. Aug 13: WWDC20 SwiftUI lifecycle. Aug 14: extract local package. Aug 15: integrate package. Aug 16: review. | Reusable code extracted to a local package |
| Aug 17-23 | Concurrency | Aug 17: async/await. Aug 18: structured concurrency. Aug 19: actors. Aug 20: MainActor. Aug 21: WWDC21 concurrency videos. Aug 22: convert callbacks to async/await. Aug 23: review. | Async loading plus one actor-isolated service |
| Aug 24-26 | Swift 5.7/5.8 and iOS 16 | Aug 24: `any` existentials, primary associated types, and opaque parameters. Aug 25: Regex, NavigationStack, and Charts. Aug 26: WWDC22 Swift, SwiftUI navigation, and concurrency debugging sessions. | Modern navigation or chart prototype |
| Aug 27-28 | Swift 5.9/5.10 and WWDC23 | Aug 27: macros, Observation, and SwiftData. Aug 28: strict concurrency updates, parameter packs, and an Observation or SwiftData prototype. | Macros/Observation/SwiftData notes plus one prototype |
| Aug 29-30 | Swift 6.x and WWDC24/WWDC25 | Aug 29: Swift 6 language mode, data-race safety, Sendable, isolation, and Swift Testing. Aug 30: WWDC24/WWDC25 Swift, SwiftUI, App Intents, Apple Intelligence, and tooling sessions relevant before WWDC26. | Swift 6 migration checklist plus pre-WWDC26 topic map |
| Aug 31 | Pre-WWDC26 final review | Review the full Swift timeline, finish missing notes, list open questions to bring into WWDC26. | Swift history summary plus WWDC26 question list |

## September Boundary

Do not pre-plan September in this roadmap.

By September 1, the goal is to have already learned the important Swift language
and ecosystem changes from the pre-Swift-3 baseline through the current Swift 6
era. September should be used after WWDC26 starts, based on the actual sessions,
announcements, and app opportunities from that conference.

## Version Documentation Plan

Use this repository's version-file convention:

```text
swift-X_Y.md
```

| Version | File | Focus | Status |
| --- | --- | --- | --- |
| Baseline | `basics.md` | Core Swift language features before Swift 3.0 | In progress |
| Swift 3.0 | `swift-3_0.md` | API Design Guidelines, Grand Rename, Swift 3.0 deltas only | Planned |
| Swift 3.1 | `swift-3_1.md` | Incremental generics and sequence improvements | Done |
| Swift 4.0 | `swift-4_0.md` | Codable, key paths, String overhaul | Planned |
| Swift 4.1 | `swift-4_1.md` | Conditional conformance, synthesized Equatable/Hashable | Planned |
| Swift 4.2 | `swift-4_2.md` | CaseIterable, random APIs, dynamic member lookup | Planned |
| Swift 5.0 | `swift-5_0.md` | ABI stability, Result, raw strings | Planned |
| Swift 5.1 | `swift-5_1.md` | Opaque types, property wrappers, SwiftUI foundation | Planned |
| Swift 5.2 | `swift-5_2.md` | `callAsFunction`, key-path expressions | Planned |
| Swift 5.3 | `swift-5_3.md` | Multiple trailing closures, `@main`, enum synthesis | Planned |
| Swift 5.4 | `swift-5_4.md` | Result builders and closure ergonomics | Planned |
| Swift 5.5 | `swift-5_5.md` | async/await, actors, structured concurrency | Planned |
| Swift 5.6 | `swift-5_6.md` | Concurrency refinements and early migration support | Planned |
| Swift 5.7 | `swift-5_7.md` | `any`, primary associated types, regex | Planned |
| Swift 5.8 | `swift-5_8.md` | Upcoming feature flags, back deployment, type placeholders | Planned |
| Swift 5.9 | `swift-5_9.md` | Macros, Observation, SwiftData era | Planned |
| Swift 5.10 | `swift-5_10.md` | Strict concurrency preparation and language refinements | Planned |
| Swift 6.0 | `swift-6_0.md` | Swift 6 language mode and data-race safety | Planned |
| Swift 6.1 | `swift-6_1.md` | Swift 6 refinements | Planned |
| Swift 6.2 | `swift-6_2.md` | Current Swift 6 updates | Planned |
| Swift 6.3 | `swift-6_3.md` | Current Swift 6 updates and ecosystem changes | Planned |

## WWDC Documentation Plan

Create a dedicated WWDC note for each year when the conference material is
broader than one Swift release or lands between releases.

Use this naming convention:

```text
wwdc-YYYY.md
```

Examples:

- `wwdc-2016.md`: Swift 3, API design direction, iOS 10-era context.
- `wwdc-2017.md`: Codable demos, Foundation, iOS 11-era context.
- `wwdc-2018.md`: Swift 4.2 direction, testing/debugging, iOS 12-era context.

Each WWDC note should include:

1. Sessions watched.
2. Swift language or tooling changes explained at the conference.
3. Platform changes that matter for app work.
4. What should be documented in version files.
5. What should be tried in code.

## Per-Version Document Template

Each version file should include:

1. Release date and minimum Xcode version.
2. Major theme or focus of the release.
3. What's New section with before/after Swift examples.
4. Swift Evolution proposal references such as `SE-XXXX`.
5. Migration notes from the previous version.
6. Key takeaways:
   - What became easier?
   - What old pattern changed?
   - What still feels missing?
7. Resources:
   - Swift.org release notes or blog posts.
   - Swift Evolution proposals.
   - Apple Developer documentation.
   - WWDC or Apple Developer videos.

## Official Resource Index

- Swift documentation: <https://www.swift.org/documentation/>
- Swift Evolution: <https://www.swift.org/swift-evolution/>
- Swift blog: <https://www.swift.org/blog/>
- Apple Developer videos: <https://developer.apple.com/videos/>
- Apple Developer documentation: <https://developer.apple.com/documentation/>
- Apple iOS developer page: <https://developer.apple.com/ios/>

## Commit Strategy

Keep commits scoped to one version or one roadmap update.

Example:

```bash
git add swift-4_0.md
git commit -m "docs(swift-4.0): add Codable, key paths, and String changes"
```
