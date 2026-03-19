[2026-03-19 · 00:10 UTC]
Added

Circle of 5ths tab (6th module) with 5-tier progression

Tier 1: circle navigation — 5th above, 4th above, identify highlighted key
Tier 2: accidental counts in both directions
Tier 3: name accidentals in order, name the last accidental added
Tier 4: reverse lookup — identify key from accidental count or specific list
Tier 5: relative minors, both directions


Circle: tappable SVG-style canvas showing all 12 positions with active/inactive states and accidental count hints
Circle: SR + unlock progression starting from C/G/F, expanding outward symmetrically (C→G+F→D+Bb→A+Eb→E+Ab→B+Db→F#), tiers 2–5 unlock as key pool grows
Circle: per-card timer (15s default), 12 hits to unlock, 5 misses to drop
Circle: 5th-above and 4th-above questions highlight the answer node as a muted ? so spatial context is visible without revealing the answer

Changed

Triads: white-key unlock order randomized on every session start and reset — begins on 1 random white key, unlocks remaining 6 in a new random sequence each time; accidentals remain in fixed order at the end
Nashville Numbers: button layout shuffles once per deck cycle to prevent positional memory replacing actual recall
Notation: note name badge now shows ? until the player answers — was incorrectly revealing the answer on card load
Notation: fret 0 tap detection fixed — Math.round replaced with Math.floor for column calculation, eliminating dead zone across right half of the (wide) open-string fret cell
Notation: NT.redrawStaff reference error fixed — settings checkbox now correctly calls NT.redraw()
All modules: unlock toast repositioned to top banner (was center-screen), duration reduced to 800ms, layout changed to single horizontal row
All modules: timers and progression drain now pause on browser tab switch and window hide via visibilitychange
Guitar/Steel: progression timer stops when switching away from those tabs, resumes on return

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
