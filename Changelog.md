# NKB Trainer Changelog

## 2026-03-12 (build 1200MDT)

### Added
- High score system (Best streak, persisted to localStorage, per-module)
- Separate Reset Best Streak button in each module's settings
- NKB Trainer title bar with MDT build timestamp

### Changed
- Triads module renamed from "Missing Note / Triad Drill"
- Diatonic module renamed to "Nashville #s"
- Nashville #s: degrees now use plain numbers (1–7°), not Roman numerals
- Nashville #s: progression tiers start at 4·5 instead of I·IV·V
- Nashville #s: key pool now G-first
- AudioContext deferred until first user gesture

### Fixed
- Deprecated apple-mobile-web-app-capable meta tag
- Stale Roman numeral in Nashville #s initial prompt
- High score system writing to localStorage on streak ties (now strict improvement only)
- levelUpSound / levelDropSound missing null guard before first user gesture
- Four repeated inline styles on Reset Best buttons replaced with .subdued CSS class
