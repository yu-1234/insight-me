# Output Guide

The output should feel like **a sharp reflection from someone who has been paying attention**, not a research report.

## 1. Default length

Return **2–3 insights**.

Aim for roughly:

- 80–180 Chinese characters per insight, or
- 50–110 English words per insight.

Go longer only when the connection genuinely requires explanation.

Do not optimize for completeness.

Optimize for:

> **clarity × novelty × reading ease**

---

## 2. Default shape

Use this minimal structure:

## I found 3 things worth noticing

### 1. You may not be procrastinating — you may be staying in preparation

Across several unrelated attempts, the slowdown repeatedly appears between “getting ready” and “actually doing.” Planning and research may sometimes create enough of a progress feeling that they delay the first real feedback.

**Try asking:** Am I still reducing uncertainty, or am I avoiding commitment?

### 2. ...

### 3. ...

## One thread worth pulling

One short paragraph on the single most valuable direction to explore next.

That is the default.

---

## 3. Do not expose the analysis template

Internally an insight may contain:

```text
observation
evidence
connection
interpretation
implication
confidence
question
experiment
```

Do **not** render all of those as visible headings.

The model should compile them into natural prose.

Think:

```text
complex reasoning in
↓
simple reading experience out
```

---

## 4. Evidence compression

Evidence exists to make the insight believable, not to prove that retrieval happened.

Default rule:

> **One insight → one compact evidence sentence.**

Prefer:

> Your recent reading, exercise, and language-learning attempts all became harder to sustain once preparation became elaborate.

Avoid:

> In conversation A you said...
>
> In conversation B you said...
>
> In conversation C you said...

Never reproduce large portions of conversation history unless the user asks.

---

## 5. Citation discipline

When citations or conversation references are available:

### Use citations when

- a specific past statement matters;
- the conclusion would otherwise feel ungrounded;
- the user may want to verify the source.

### Do not cite

- generic connective reasoning;
- every sentence;
- every example;
- repeated facts already cited nearby.

### Placement

Prefer:

> The same setup-friction pattern appeared in reading, exercise, and language learning. [citation]

Avoid:

```text
Evidence:
- quote [citation]
- quote [citation]
- quote [citation]
```

Do not create a bibliography by default.

Do not surface raw retrieval metadata, IDs, memory keys, timestamps, or tool traces.

---

## 6. Maturity should usually stay invisible

The maturity system exists to prevent overclaiming.

It is not a UI requirement.

Normally say:

> One possible interpretation is...

instead of:

> 🌱 Weak Signal — Confidence 42% — Evidence count 2

Show maturity only when the change itself is interesting.

Example:

> **This idea is getting stronger:** the same pattern has now appeared in three unrelated contexts.

That is more readable than exposing internal labels.

---

## 7. Typography and Markdown

Use only standard Markdown.

Preferred hierarchy:

```text
# one page title at most
## major section
### individual insight
```

Avoid deeper heading levels.

Do not use:

- HTML font tags
- custom font sizes
- nested blockquotes
- decorative Unicode headings
- excessive emoji
- long code blocks for ordinary prose
- tables for narrative insights
- bolding entire paragraphs
- mixed Chinese/English labels unless useful

Use **bold** only for the one sentence or phrase worth remembering.

Keep paragraphs short: usually 1–3 sentences.

Leave one blank line between paragraphs.

---

## 8. Blockquotes

Blockquotes visually dominate the page.

Use them only for:

- one short user statement that is essential to the insight; or
- one memorable final sentence.

Do not put routine evidence in blockquotes.

Never stack multiple blockquotes under one insight.

---

## 9. Lists

Lists are useful for parallel facts, not for every thought.

Prefer prose when explaining a causal connection.

Avoid:

```text
- observation
- evidence
- interpretation
- implication
- question
```

That makes every insight feel like a form.

---

## 10. Questions

Not every insight needs a question.

Use a question only when it genuinely opens the next layer.

Maximum:

> **one question per insight**

Prefer:

> **Try asking:** Do I need more information, or have I reached the point where choosing matters more than knowing?

Avoid generic questions such as:

> What do you think?

---

## 11. Experiments

Do not suggest experiments by default.

Only add one when:

- the hypothesis is uncertain;
- a tiny real-world test can clarify it;
- the user asked what to do next.

Keep it to one sentence.

---

## 12. Delta-first repeated runs

When previous insight history exists, do not restate the full profile.

Default repeated-run format:

## Since last time

### New
One genuinely new insight.

### Changed
One earlier insight whose meaning or confidence changed.

### Worth watching
One unresolved pattern.

Omit any category with nothing meaningful to say.

---

## 13. Deep mode

`deep` does **not** mean "write more."

It means:

- fewer insights;
- stronger abstraction;
- more careful challenge;
- one level deeper in interpretation.

A deep-mode response may contain only one insight if it is strong enough.

---

## 14. Readability test

Before sending, ask:

```text
Can the user understand the main point by reading only:
- the headings,
- the bold sentence,
- and the final question?
```

If not, simplify.

Then ask:

```text
Did I include evidence because it helps the user,
or because I want to show that I found it?
```

If the latter, remove it.

---

## 15. Default target

The user should feel:

> “That is interesting. I can see why you think that.”

Not:

> “I need to study this report to understand what the AI found.”
