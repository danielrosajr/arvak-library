# Changelog

## [1.7.0] — 2026-10-27

### Added
- Project Insights dashboard, transparent recommendations, impact × effort matrix with adjustable perspective and filters.
- Side-by-side comparison of 2–3 projects with missing scores explicit.
- Temporary scenario simulation that does not overwrite saved weights.
- Pairwise Priority Duel (binary insertion), undo, resume, draft preview and explicit apply/cancel.
- Pause/Complete and Reactivate actions, with paused/completed at bottom of the priority list.
- Pre-v1.7 local snapshot, new tutorial steps and documentation.

### Preserved
- The same storage key `arvak-library-v1`, schema version 1, compatibility with legacy backups.
- v1.6 Idea Vault, v1.5 Smart Rank, v1.4 ranking, v1.3 repository discovery and all earlier library features.

### Notes
- App-side data migration stays non-destructive. Explicit status changes in duels are immediately persisted, while the manual order is only applied on confirmation.
