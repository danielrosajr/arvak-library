# Arvak Library v1.3.0 — GitHub Project Discovery

This release turns Arvak Library into a smarter personal project collection with opt-in GitHub repository suggestions.

## Added

- Discover public repositories from the owner's GitHub account using the official REST API.
- Suggest repositories that are not already in the library.
- Review each suggestion and choose to **Add** or **Ignore** it.
- Display repository name, description, primary language, last push, archive/fork indicators, and GitHub Pages metadata.
- Optional GitHub Pages URL suggestion (requires manual verification).
- Automatic discovery at most once every 24 hours, with an on/off setting.
- Restore ignored suggestions through a filter.
- New guided tutorial step explaining discovery.
- Pre-upgrade local backup for v1.3 and support for old JSON backups.

## Improved

- Avoid duplicates by matching GitHub repository URLs and names, including manually added projects with repository links.
- Refresh known projects' push activity during repository discovery.
- Keep favorite flags, status, notes, ChatGPT links, bug lists and future ideas unchanged when scanning.
- Improved small-screen toolbar layout.

## Important

- Repositories are **never added automatically**; you must confirm each import.
- GitHub discovery only works with **public repositories**, needs an internet connection, and may be rate-limited by GitHub.
- GitHub Pages being enabled does not guarantee that its URL is deployed or reachable.
- Existing personalized project data remains browser-local. **Export a JSON backup before updating.**
- No backend, API key, authentication or new dependencies required.
