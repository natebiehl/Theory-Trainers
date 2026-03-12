## [2026-03-12 · 14:00 MDT]

### Added
- Steel: progression mode with alternating outward fret unlock from configurable base fret (default 3)
- Steel: hesitation timer (8s drain, 40% refill on correct answer)
- Steel: nextDeck SR model replacing weight-based pool (tier 0–4, freq 1/1/2/4/8)
- Steel: progression bar UI with hit/miss indicators and drop warning
- Steel: hits-to-unlock and misses-to-drop sliders in settings
- Steel: base fret input in settings

### Changed
- Steel: key-tones-only filter now gates the SR deck and progression counter
- Steel: Show intervals and Highlight key tones default to on
- Steel: manual fret range hidden when progression mode is on
- Steel: level-up/drop sounds now fire on fret unlock/drop events
- Guitar: accidental spelling defaults to Both (C#/Db)
- Guitar: hits-to-unlock default raised to 24, slider max raised to 36
- Triads: hits-to-unlock slider max raised to 18
- Nashville: hits-to-unlock slider max raised to 18

### Removed
- Steel: Intro/Standard/Deep SR mode buttons (superseded by nextDeck auto-weighting)

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
