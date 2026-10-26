# Changelog — Arvak Library

## [1.4.0] — 2026-10-25 — Project Ranking

### Added
- Project Ranking tab with optional evaluations for ten criteria plus maintenance effort.
- Configurable weighted priority index, coverage tracking and provisional-score separation.
- General, commercial, social, personal, quick-execution, portfolio and opportunity presets.
- Create/delete user weight presets without overwriting project evaluations.
- Separate manual order with keyboard/mobile-friendly up/down controls.
- Instant scoring, quick evaluation in the project drawer and individual reasoning notes.
- Filters for category, development status, query and incomplete evaluations.
- Deterministic recommendations, explicit scoring documentation and a future roadmap.
- Pre-v1.4 local backup and preview before importing a JSON backup.

### Changed
- Preserve version-1 `localStorage` schema; add ranking as an optional root property and evaluation on existing project overrides.
- Ensure elements marked hidden remain hidden even when CSS defines a layout display property.

### Preserved
- Existing GitHub project discovery, app/ChatGPT links, status, favorites, bug reports, fixes, future ideas, statistics, tutorial, mobile layout and theme switching.

### Limitations
- All data remains local to the browser; cloud synchronization is not available.
- Project comparison, charts, impact-effort matrix and cycle planning remain planned for later versions.
