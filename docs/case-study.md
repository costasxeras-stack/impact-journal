# Case study: Impact Journal

## The problem

Review season comes and nobody remembers March. Most people write their self-review from memory the night before, so it is thin, recent and missing the numbers. A brag document helps, but a blank document gets abandoned. This app makes the entry small, asks for the result every time, and shows the gaps while there is still time to fill them.

## From a small tool to an app

Version 0 was a one-screen tool on my portfolio site, picked because it was quick to build. It worked, but it only stored data. For 0.1.0 I asked what a user would need to come back every week, and what the app should show them that they could not see before. The answer shaped three decisions.

## Decisions

### 1. Keep everything in the browser, with no account

Career notes are personal. Some mention colleagues, numbers or problems at work that should not sit on someone else's server.

**Decision:** All data stays in the browser's local storage. Backup is a JSON file the user downloads.

Full record: [docs/decisions/0001-browser-storage-only.md](decisions/0001-browser-storage-only.md)

### 2. Build drafts from the user's own words, with no AI writing

An AI could write a polished self-review. It could also add claims, numbers or impact the user never wrote, and the user would sign it.

**Decision:** The review builder only groups, orders and formats what the user wrote. Gaps show as a [placeholder] for the user to fill.

Full record: [docs/decisions/0002-drafts-from-your-own-words.md](decisions/0002-drafts-from-your-own-words.md)

### 3. Show skill gaps first, keep streaks small

Habit apps lean on streaks. For a review, the more useful signal is what the record is missing.

**Decision:** The dashboard leads with skills and reach, marks skills with no entry in 6 months in red, and shows weeks in a row as one small number.

Full record: [docs/decisions/0003-gaps-over-streaks.md](decisions/0003-gaps-over-streaks.md)

## What it does now

- **Journal:** one line for what you did, one for what changed, plus type, reach (my team, other teams, whole company, customers), skills, an optional number, proof link and feedback. Star your best entries.
- **Filters:** search, by skill, starred only, and "missing a number" or "missing a result" to fix weak entries.
- **Dashboard:** entries per month, weeks in a row, skills covered in the last 6 months with gaps in red, reach beyond your own team, and record quality.
- **Review builder:** turns a period (last 3, 6 or 12 months, a quarter or a year) into a self-review by skill (with a "where I want to grow" section for skills with no entries), a summary by type, ranked CV bullets or a one-page brag document. Copy or download as Markdown.
- **Nudge:** after 14 days without an entry, a banner asks if anything is worth a line.
- **Data:** JSON backup and restore, CSV export, your own skill list, and 14 example entries (clearly marked) to try it out.

## What I would measure

There is no usage data yet, so there are no findings. These are hypotheses to test with real users.

| Measure | Definition | Target |
|---|---|---|
| Weekly active writers | Share of users who add at least one entry in 3 of the last 4 weeks | [x]% |
| Entry strength | Share of entries with a result and a number | [x]% |
| Draft use | Share of users who copy or download a draft in review season | [x]% |

## What I would do next

1. Reminders by calendar (once a week, at a time the user picks)
2. Import from a calendar or task tool to suggest entries
3. Optional AI rewording of a draft, shown as a diff against the user's words

## My role

I defined the problem, the users, the features and the decisions, and tested every flow on desktop and phone widths. Claude (Anthropic) wrote the code with me.
