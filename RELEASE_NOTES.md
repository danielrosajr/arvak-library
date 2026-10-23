# Arvak Library v1.1.0 — Testing & Bug Tracking

## What's New

- Added **Testing (Em testes)** as a project lifecycle status.
- Added an independent **Has Bugs (Com bug)** flag with optional issue notes.
- Added dedicated filters, sidebar sections, counters, and status badges.
- Both properties can be combined on the same project.
- Extended the project creation form with testing and bug options.
- Preserved compatibility with the v1.0 localStorage key and existing JSON backup format.
- Added a pre-upgrade local backup snapshot and a reminder to download a portable backup.
- Added safety snapshots before importing backups and resetting the collection.

## Upgrade Notes

**Export a JSON backup before upgrading.** Personal projects, notes, and favorites are stored locally in the browser, not in GitHub. Updating `index.html` on the same website and using the same browser retains existing data. Different browsers or devices require manual export/import.

## GitHub Release Metadata

Tag: `v1.1.0`  
Release title: `Arvak Library v1.1.0 — Testing & Bug Tracking`  
Commit: `feat: add testing status, bug flags and safer backups`  
