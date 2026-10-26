# Arvak Library v1.6.0 — Idea Vault

**Save the idea now. Build it when you're ready.**

This release introduces **Idea Vault**, a dedicated home for project concepts that you want to keep without starting development right away.

## What's new

- **Project prompt storage:** save the full ChatGPT prompt inside the project (up to 40,000 characters).
- **Personal context:** keep the original motivation, intended final experience, and additional references or brainstorming notes.
- **Readiness stages:** Draft, Structured, and Ready to Start — separate from the project's development status.
- **A dedicated Idea Vault:** browse ideas, see which have prompts, search across notes, sort by recent edits, and filter incomplete concepts.
- **Easy reuse:** copy prompts, download them as TXT, or import existing TXT prompts into an idea.
- **Autosave:** edits are stored in your browser with manual save available at any time.
- **Guided workflow:** create a new idea from the Vault and open its editor immediately.
- **Safer backups:** Idea Vault data is included in JSON exports/imports; compatible with older Arvak Library data.

## Compatibility

The app stays a standalone `index.html` and retains its existing local-storage key. Existing favorites, projects, ChatGPT links, bugs, future-feature lists, and project ranking data remain intact.

## Upgrade instructions

**Export a JSON backup first.** Replace your repository's root `index.html`, commit to `main`, and open GitHub Pages. No build step required.

> Your prompts and notes are stored locally in the current browser. They do not sync to other devices or get sent to AI services automatically.
