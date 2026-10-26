# Arvak Library v1.5.0 — Smart Rank (Free AI Workflow)

## Highlights

Smart Rank lets you evaluate and prioritize multiple personal projects without manually filling every score. It uses a free, review-first ChatGPT workflow: generate a structured prompt, analyze it in ChatGPT, and import suggested ratings as JSON.

### New features

- Generate structured analysis prompts for all projects, insufficiently evaluated items or projects modified since the last accepted analysis.
- Optional public GitHub README retrieval (up to 10,000 characters per project); gracefully handles missing files and API limits.
- Five perspectives: balanced, commercial, social, portfolio and quick execution.
- Preview the prompt, copy it or download it as a TXT file.
- Import suggested evaluations by pasting JSON or selecting a file.
- Validate project IDs, missing/unknown projects and scores in the 0–10 range.
- Review scores side by side with existing ratings, explanations, evidence and confidence.
- Existing scores are not selected for overwrite by default. Subjective criteria such as personal meaning, motivation and urgency are also not selected automatically.
- Apply only selected suggestions after explicit confirmation. Save the origin, date and confidence of accepted AI suggestions.
- Preserves all v1.4 data, backups, GitHub discovery, links, tasks and ranking settings.

### Privacy and limitations

- No paid API, token, server, auto-sharing or autonomous ChatGPT connection. You paste the prompt and the returned JSON yourself.
- Personal notes, favorites, bugs, tasks and ChatGPT links are excluded from generated project records.
- Public READMEs may contain additional information; review prompts before sharing.
- AI evaluations are hypotheses based on available evidence, not definitive facts. Missing ratings remain missing.
- Public GitHub requests are rate limited and the README does not constitute a code audit.

### Deployment

1. Export your current JSON backup in Arvak Library.
2. Replace the repository root `index.html` using GitHub's web interface.
3. Commit to `main`; your existing GitHub Pages branch deployment serves the updated site.
4. Check your data before running Smart Rank.

**Tag:** `v1.5.0`
**Commit:** `feat: add free AI-assisted Smart Rank with JSON review`
