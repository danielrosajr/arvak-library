# Arvak Library v1.7.0 — Project Insights & Priority Duel

## Highlights

Transform your personal library into a more practical project decision dashboard — without losing quick access to your apps, mods, or saved ideas.

### Added

- **Project Insights:** activity and evaluation summary, rule-based recommendations, and a configurable **Impact × Effort matrix**.
- **Side-by-side comparisons:** compare two or three projects across existing rating criteria, preserving blank values rather than inventing scores.
- **Scenario simulator:** see how alternative prioritization presets change the computed order without editing any stored weights or personal rankings.
- **Priority Duel (1×1):** quickly build a personal ranking by choosing between two projects per round. Uses binary insertion to reduce the number of comparisons.
- **Pause / Complete during duels:** remove a project from further rounds and place it at the bottom of the manual priority list. Reactivation is supported.
- **Undo, resume and review:** comparison progress persists locally, and the final order is only applied after confirmation.
- **Pre-v1.7 backup:** an automatic local snapshot is saved when previous data exists, with manual JSON export still strongly recommended.

### Kept unchanged

- Existing `arvak-library-v1` storage key and backup schema version.
- GitHub repository discovery and optional activity queries.
- Smart Rank AI-assisted prompt/JSON workflow.
- Idea Vault, saved prompts, app links, ChatGPT links, notes, fixes, future ideas, favorites, statuses, and theme.
- Static single-file deployment through GitHub Pages.

### Notes

- **No paid AI API, backend or account is needed.** Insights and duels run entirely in the browser.
- Matrix placement requires sufficient rated criteria. Missing evaluations stay missing.
- Changing a project status in a duel saves that status immediately even if you later discard the duel order.
- Back up your library JSON before replacing `index.html`.

### Version

- **Tag:** `v1.7.0`
- **Commit:** `feat: add Project Insights and pairwise manual ranking`
