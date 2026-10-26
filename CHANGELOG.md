# Changelog

## [1.5.0] — Smart Rank

### Added
- Free ChatGPT-assisted scoring workflow with prompt generation and optional public README retrieval.
- Scopes: all, insufficiently scored, and newly added/modified repositories.
- Five analysis objective presets and preview/copy/download of prompt.
- Validated JSON suggestions, per-criterion review, source confidence and evidence.
- Selection controls, explicit approval before applying, and preservation of manual scores by default.
- Local provenance for imported suggestions, new pre-v1.5 backup, and guided tutorial entry.

### Changed
- Ranking area now surfaces AI-assisted evaluation without altering its existing ranking formula or manual priorities.
- Updated roadmap labels; planned Project Insights moved to v1.6.0.
- Adjusted mobile screen-reader-only labels to avoid horizontal overflow.

### Preserved
- `arvak-library-v1` localStorage key and version 1 data model.
- Existing apps, custom entries, statuses, favorites, notes, bugs, issues, ideas, ChatGPT links, Github scanner, themes and backups.

### Security
- No API tokens, payment, backend, automatic AI requests or automatic score replacement.
- README fetch restricted to public GitHub repositories of the configured owner.
- Private note and ChatGPT-link fields are excluded from generated prompts by design.

## [1.4.0] — Project Ranking
- User-controlled scorecard, ranking presets, manual ordering, score coverage, backup compatibility.

## [1.3.0] — GitHub Discovery
- GitHub repository suggestion scanner and add/ignore flow.

## [1.2.0] — Project Workflow
- ChatGPT conversation links, in-progress status, fixes, ideas and guided tour.
