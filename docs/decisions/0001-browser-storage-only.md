# 0001: Keep everything in the browser, with no account

**Status:** accepted, 0.1.0

## Context

Career notes are personal. Some mention colleagues, numbers or problems at work that should not sit on someone else's server.

## Decision

All data stays in the browser's local storage. Backup is a JSON file the user downloads.

## Tradeoff

- No sign-up, nothing to trust, works offline once loaded.
- No sync between phone and laptop. A backup file moves the data, and the app shows when the last backup was taken.
- Clearing browser data deletes the journal. The Data tab says so.
