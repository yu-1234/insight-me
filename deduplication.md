# Test — Insight deduplication

## Existing insight

> The user becomes more consistent when the first action is tiny and obvious.

## New evidence

- meal preparation works better when ingredients are already visible
- household paperwork gets done when the document is already open
- stretching happens more often when the mat is left out

## Expected behavior

Do not output three new versions of the same insight.

Treat the new items as supporting evidence and consider whether:

- confidence increases;
- scope expands;
- the original wording should be refined.

## Failure condition

Every new example becomes a separate "new insight".
