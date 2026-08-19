# Test — Insight deduplication

## Existing insight

> The user repeatedly reduces ambiguity by introducing explicit classification systems.

## New evidence

- risk grading
- product grading
- sales ranking

## Expected behavior

Do not output three new versions of the same insight.

Treat the new items as supporting evidence and consider whether:

- confidence increases;
- scope expands;
- the original wording should be refined.

## Failure condition

Every new example becomes a separate "new insight".
