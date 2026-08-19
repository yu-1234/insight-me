---
name: insight-me
description: >
  Analyze the user's past conversations, projects, decisions, successes,
  failures, recurring patterns, contradictions, unfinished ideas, and
  changing beliefs to generate new evidence-based insights the user has
  not explicitly stated before. Use when the user wants reflection,
  hidden-pattern discovery, cross-project connections, blind spots,
  assumption challenges, idea generation from personal history, or
  deeper deductions from prior conversations and experiences.
license: MIT
metadata:
  version: "0.1.0"
---

# insight-me

Turn past conversations and experiences into ideas the user has not thought of yet.

## 1. Mission

Do **not** merely summarize the user's history.

Do **not** treat memory retrieval as insight.

Do **not** stop at simple experience reuse.

The central question is:

> What new idea becomes visible when the user's past experiences are viewed together?

The desired progression is:

```text
Past Experiences
        ↓
Connections
        ↓
Patterns
        ↓
Abstraction
        ↓
New Insight
        ↓
Question / Hypothesis / Direction
```

## 2. Default scope

Unless the user specifies otherwise:

- analyze the most recent 90 days;
- prioritize newer evidence when older and newer evidence conflict;
- treat repeated discussion of the same project as one project-level evidence source rather than many independent sources.

Possible scopes include:

- last 7 / 30 / 90 days
- last 6 months
- last year
- all available history
- a specific project
- a specific topic
- career
- product ideas
- blind spots
- unfinished ideas

## 3. Evidence extraction

Silently build an experience map from meaningful evidence such as:

- project
- decision
- problem
- goal
- failure
- success
- experiment
- question
- opinion
- assumption
- method
- habit
- recurring complaint
- abandoned idea
- unfinished thread
- unexpected outcome
- change of mind
- external feedback

Never invent missing experiences, motives, outcomes, emotions, or opinions.

For each important item, reason conceptually about:

```yaml
experience:
  context:
  time:
  problem:
  action:
  reasoning:
  outcome:
  reaction:
  lesson:
  unresolved_question:
```

Not every field must be present.

## 4. Build an experience graph

Do not analyze each conversation in isolation.

Connect experiences using relations such as:

```text
similar_to
contradicts
caused_by
followed_by
reuses
evolved_into
failed_because
solves_same_problem_as
shares_method_with
depends_on
could_combine_with
reveals_pattern_with
```

Use the graph to search for higher-order explanations.

## 5. What counts as a good insight

A strong insight should satisfy at least 3 of these 5 conditions:

1. **Novel** — the user has not explicitly stated the conclusion before.
2. **Evidence-based** — grounded in meaningful past evidence.
3. **Cross-context** — connects different projects, domains, or time periods.
4. **Explanatory** — explains why something keeps happening.
5. **Generative** — creates a new question, hypothesis, framework, strategy, experiment, product idea, or direction.

## 6. What is not insight

Do not output these as insights:

### Summary

> You discussed Project A, Project B, and Project C.

### Memory retrieval

> You previously mentioned customer segmentation.

### Simple transfer only

> You used customer segmentation in A, so you could reuse it in B.

### Generic advice

> You should communicate more.
> You should keep learning.
> You should focus on your strengths.

If a candidate is obvious, go one abstraction level deeper.

## 7. Core reasoning modes

Use multiple reasoning modes. Do not rely on only one.

At minimum consider:

- recurring pattern detection
- cross-project connection
- contradiction detection
- unconscious method detection
- abstraction ladder
- missing implication detection
- abandoned-thread detection
- repeated-pain detection
- second-order thinking
- counterfactual reasoning
- capability / identity pattern
- opportunity collision

Detailed instructions: `references/INSIGHT-ENGINES.md`

## 8. Novelty filter

Before presenting any insight, ask:

> Has the user already explicitly said this?

If yes:

- discard it, or
- go one abstraction level deeper, or
- show only the new implication created by fresh evidence.

Do not relabel known user beliefs as discoveries.

## 9. Deduplication

Before outputting a candidate insight, compare it with previously identified insights.

Classify it as one of:

```text
New Insight
Extension
Refinement
Contradiction
Supporting Evidence
Duplicate
```

New evidence does not automatically create a new insight.

When several observations share the same core explanation, merge them into a deeper insight.

When one broad insight later separates into distinct mechanisms, split it.

When new evidence conflicts with an existing insight, re-evaluate rather than silently ignoring the contradiction.

Detailed rules: `references/INSIGHT-MATURITY.md`

## 10. Insight maturity

Use this lifecycle:

```text
Observation
↓
Weak Signal
↓
Emerging Pattern
↓
Strong Insight
↓
Personal Principle
```

Maturity depends on **independent evidence**, cross-context support, explanatory power, predictive usefulness, and survival of contradictory evidence — not on time alone.

Insights may also be:

- promoted
- demoted
- refined
- merged
- split
- challenged
- retired

Personal Principles should be rare.

Detailed rules: `references/INSIGHT-MATURITY.md`

## 11. Evidence threshold

Use these defaults:

### Weak Signal
- 1 strong clue, or
- 2 closely related observations

Phrase as hypothesis.

### Emerging Pattern
- 2–3 meaningful experiences
- preferably across 2 contexts

### Strong Insight
- 3+ independent experiences
- cross-context repetition
- clear explanatory value
- few serious contradictions

### Personal Principle
- repeated evidence across multiple contexts or a long time span
- survives attempts to disconfirm
- has predictive usefulness
- repeatedly confirmed by later behavior

Never inflate evidence counts by counting repeated discussion of one event multiple times.

## 12. Disconfirmation

Before promoting an insight to Strong Insight or Personal Principle, actively search for:

- counterexamples
- contexts where the pattern fails
- alternative explanations
- environmental causes
- newer behavior that contradicts older behavior

A system that only confirms its earlier ideas will become confidently wrong.

## 13. Scope control

Keep each insight scoped to the evidence.

Prefer:

> In business-analysis and system-design work, you repeatedly reduce ambiguity through explicit categories and rules.

Avoid:

> You are a person who needs everything structured.

Do not generalize professional patterns into personality or life-wide claims without evidence.

## 14. Delta-first reflection

If previous insight history is available, prioritize:

> What changed since the last reflection?

Prefer:

- new insight
- new evidence
- maturity upgrade
- maturity downgrade
- insight merge
- contradiction
- changed meaning
- new implication

Suppress mature insights that remain unchanged.

An existing insight should reappear only when:

1. its maturity meaningfully changed;
2. its meaning changed;
3. contradictory evidence appeared;
4. it combined with another insight;
5. it now generates a new implication;
6. the user explicitly asks to revisit it.

## 15. Surprise test

Before outputting an insight, ask:

> Would the user reasonably respond: “I hadn't thought about it that way”?

If not, it may be too obvious.

Prefer fewer high-value insights over many predictable observations.

## 16. Compression test

Strong insights compress many experiences into one explanation.

Weak:

> You built segmentation, dashboards, alerts, and profiles.

Strong:

> Across several projects, you repeatedly turn fragmented information into explicit decision states and triggers. The recurring product may be the decision logic underneath the dashboards, not the dashboards themselves.

## 17. Default output

Return **3–5 insights maximum**.

Rank candidates by:

```text
Novelty
× Evidence Strength
× Potential Impact
```

For each insight use:

### Insight — [short title]

**What I noticed**  
Concrete supporting evidence or pattern.

**The new interpretation**  
The conclusion that was not explicitly stated before.

**Why it matters**  
The consequence or new implication.

**Question for you**  
One question that opens a genuinely new direction.

Optional:

**Small experiment**  
A low-cost test of the hypothesis.

Detailed output rules: `references/OUTPUT-GUIDE.md`

## 18. Interaction modes

### Default

When invoked as:

```text
/insight-me
```

analyze the default 90-day window and return the 3 most interesting insights.

Finish with:

> **One thread worth pulling**

Choose the idea with the highest combination of novelty and potential impact.

### Deep mode

Triggered by phrases such as:

```text
go deeper
继续
再深一点
deep insight
challenge me
```

Revisit the strongest insight and reason through:

```text
Observation
↓
Pattern
↓
Principle
↓
Underlying Assumption
↓
Alternative Interpretation
↓
New Direction
```

Prefer fewer, deeper insights.

### Collision mode

Triggered by:

```text
combine my past ideas
idea collision
碰撞一下
把以前的东西组合起来
```

Prioritize combinations such as:

```text
Project A + Project B
Problem A + Method B
Old Failure + New Technology
Existing Asset + New Market
Personal Interest + Professional Capability
```

### Blind-spot mode

Triggered by:

```text
what am I missing?
我的盲点是什么？
哪里想错了？
challenge my thinking
```

Prioritize:

- repeated assumptions
- contradictions
- avoided decisions
- complexity growth
- missing feedback loops
- selection bias
- overengineering
- underused assets
- ignored constraints

Separate evidence from hypothesis.

### Opportunity mode

Triggered by:

```text
有什么机会？
what opportunities am I overlooking?
```

Search intersections among:

```text
Repeated Pain
+
Existing Capability
+
Existing Asset
+
Emerging Need
```

## 19. Privacy

Use only personal history necessary for the insight.

Avoid resurfacing sensitive or intimate details unless directly necessary.

Prefer abstraction over unnecessary exposure.

## 20. Final quality check

Before responding, silently verify:

```text
□ Did I do more than summarize?
□ Did I connect multiple experiences?
□ Is each insight grounded in evidence?
□ Did I avoid repeating something the user already knows?
□ Is there at least one non-obvious interpretation?
□ Did I distinguish evidence from hypothesis?
□ Did I search for counterexamples?
□ Did I avoid generic advice?
□ Did I avoid overgeneralizing scope?
□ Are there only a few high-value insights?
□ Would at least one insight plausibly make the user think:
  "I hadn't thought about it that way"?
```

If not, reason again.

## 21. Success criterion

The success metric is not:

> The AI remembered me.

It is:

> The AI connected things from my past that I had never connected myself.

And ideally:

> That connection changed how I see a problem, project, opportunity, or myself.
