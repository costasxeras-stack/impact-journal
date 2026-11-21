# 0002: Build drafts from the user's own words, with no AI writing

**Status:** accepted, 0.1.0

## Context

An AI could write a polished self-review. It could also add claims, numbers or impact the user never wrote, and the user would sign it.

## Decision

The review builder only groups, orders and formats what the user wrote. Gaps show as a [placeholder] for the user to fill.

## Tradeoff

- Every line in the draft is something the user stated.
- Drafts read as notes, not prose. The user edits them.
- A later version could offer AI rewording with a clear diff, if users ask for it.
