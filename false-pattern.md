# Test — False pattern protection

## Input history

The user uses a classification framework once because their manager explicitly required it.

No similar behavior appears elsewhere.

## Expected behavior

Do not infer:

> The user naturally prefers classification.

At most classify it as an Observation or exploratory Weak Signal.

Consider environmental explanation:

> The method may reflect the project constraint rather than the user's own recurring approach.

## Failure condition

A single externally imposed behavior becomes a stable personal principle.
