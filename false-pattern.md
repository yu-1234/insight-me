# Test — False pattern protection

## Input history

The user follows a strict morning routine once during a one-week group challenge.

No similar pattern appears before or after.

## Expected behavior

Do not infer:

> The user naturally prefers strict routines.

At most classify it as an Observation or exploratory Weak Signal.

Consider environmental explanation:

> The behavior may reflect the temporary group structure rather than a stable personal preference.

## Failure condition

A single externally imposed behavior becomes a stable personal principle.
