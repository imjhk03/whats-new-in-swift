# AGENTS.md

This file provides guidance to Codex when working with code in this repository.

## Project Overview

This is a documentation repository tracking Swift language changes across versions.
Core baseline Swift should live in `basics.md`. Each Swift version should have a
dedicated markdown file, such as `swift-3_0.md`, documenting only the new
features, syntax changes, and migration notes for that version.

See `ROADMAP.md` for the current Swift learning roadmap.

## Document Structure

Each version file follows this format:

- Header: release date and Xcode version requirement
- Major theme or focus of the release
- What's New section with before/after Swift code examples
- Migration notes from the previous version
- Key Takeaways
- Resources section with links

## File Naming Convention

Use `swift-X_Y.md`, with an underscore for the minor version.

Examples:

- `swift-4_0.md`
- `swift-5_10.md`

Use `wwdc-YYYY.md` for dedicated yearly WWDC notes.

## Writing Guidelines

When creating or editing version documentation:

- Include release date and minimum Xcode version in the header.
- Keep `basics.md` limited to language features that existed before Swift 3.0.
- Keep version files focused on deltas from the previous baseline or version.
- Provide Swift code examples showing before/after comparisons.
- Reference Swift Evolution proposals, such as `SE-XXXX`, when documenting features.
- Link to official Swift blog posts, Apple Developer documentation, Apple Developer videos, and WWDC sessions.
- Keep examples practical and focused on what changed from the previous Swift era.

## Workflow

1. Reference `ROADMAP.md` for the Swift version roadmap and features to document.
2. Keep commits scoped to one version file or one roadmap update.
3. Use concise documentation commit messages, for example:
   `docs(swift-4.0): add Codable, key paths, and String changes`
