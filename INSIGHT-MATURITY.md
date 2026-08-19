# Insight Deduplication & Maturity

## 1. Deduplication principle

Do not treat every newly generated sentence as a new insight.

Before presenting a candidate insight, classify it as:

```text
New Insight
Extension
Refinement
Contradiction
Supporting Evidence
Duplicate
```

The goal is conceptual continuity across reflection runs.

---

## 2. Semantic deduplication

Two insights are likely duplicates when their core explanatory claim is substantially the same even if:

- wording differs
- examples differ
- projects differ
- evidence differs
- abstraction level differs slightly

Example:

> You repeatedly turn fragmented business information into structured decision rules.

and:

> You often convert messy business problems into standardized frameworks.

These likely share one core claim.

Do not output both as separate discoveries.

---

## 3. Insight fingerprint

Conceptually maintain:

```yaml
insight_fingerprint:
  core_claim:
  mechanism:
  domain:
  abstraction_level:
  evidence_types:
  implications:
```

Compare fingerprints, not exact wording.

---

## 4. Similarity levels

### High similarity

Same core explanation and implication.

Action:

- suppress as new;
- merge evidence into existing insight.

### Medium similarity

Same underlying pattern, but new evidence changes meaning, scope, or consequence.

Action:

- output as evolution or refinement.

### Low similarity

Different causal explanation, implication, or genuinely new connection.

Action:

- treat as a new candidate.

---

## 5. Evidence is not insight

New evidence does not automatically create a new insight.

If customer grading, opportunity grading, product grading, and risk grading all support the same underlying pattern, update the existing insight rather than generating four variants.

Possible update:

```text
Evidence: 2 → 4 independent sources
Confidence: Medium → High
Scope: Customer management → General business decision-making
```

---

## 6. Insight merge

When several earlier insights are manifestations of one deeper principle, merge them.

Example:

Earlier:

```text
A. frequently builds classifications
B. frequently builds dashboards
C. frequently creates alerts
```

Deeper interpretation:

```text
structure complexity
→ create observable states
→ detect changes
→ trigger decisions
```

The deeper insight should absorb the shallow ones.

---

## 7. Insight split

An early broad insight may later separate into distinct mechanisms.

Example:

Early:

> The user likes automation.

Later evidence reveals:

```text
A. automate repetitive execution
B. externalize repeated human judgment
```

If these create different implications, split them.

---

## 8. Contradictory evidence

Do not silently ignore contradiction.

Possible outcomes:

```text
Insight weakened
Insight scoped more narrowly
Insight revised
Insight retired
New contradiction insight created
```

Example:

Earlier:

> The user prefers simple products.

Later:

> The user repeatedly expands products into integrated systems.

Better revision:

> The user appears to prefer simplicity at the interface level while tending toward integration at the architecture level.

---

# Insight Maturity

## 9. Lifecycle

```text
Observation
↓
🌱 Weak Signal
↓
🌿 Emerging Pattern
↓
🌳 Strong Insight
↓
🧭 Personal Principle
```

Insights may also move backward or be retired.

---

## 10. Stage 0 — Observation

A single event, statement, behavior, or decision.

Example:

> The user used customer segmentation in one project.

This is evidence, not a stable insight.

---

## 11. Stage 1 — Weak Signal

A potentially meaningful interpretation supported by limited evidence.

Typical evidence:

- 1 strong event; or
- 2 closely related observations.

Use hypothesis language:

- may
- might
- possibly
- one hypothesis is

Example:

> You may prefer reducing complexity by introducing explicit categories.

---

## 12. Stage 2 — Emerging Pattern

A recurring behavior or principle appearing in multiple independent contexts.

Typical evidence:

- 2–3 meaningful experiences;
- across at least 2 contexts when possible.

Example:

> Classification appears to be a recurring method you use to reduce decision complexity.

---

## 13. Stage 3 — Strong Insight

A pattern repeatedly supported across time, projects, or domains, with few serious contradictions.

Typical evidence:

- 3+ independent experiences;
- cross-context repetition;
- clear explanatory value.

Example:

> You repeatedly convert ambiguous business problems into explicit states, thresholds, and rules.

---

## 14. Stage 4 — Personal Principle

A highly stable, repeatedly validated pattern that explains many past decisions and predicts future behavior.

Use strict criteria:

- 5+ meaningful pieces of evidence, ideally;
- multiple domains or long time span;
- survives contradictory evidence;
- predictive usefulness;
- later behavior repeatedly confirms it.

Personal Principles should be rare.

---

## 15. Maturity is about evidence, not time

Bad logic:

```text
Insight existed for 3 months
→ Strong Insight
```

Better:

```text
More independent evidence
+
More contexts
+
Survived disconfirmation
+
Predictive usefulness
→ Higher maturity
```

---

## 16. Independent evidence

Repeated mentions of the same project count as one project-level source.

```text
5 conversations about one customer-grading project
≠
5 independent experiences
```

Prefer evidence from:

- different projects
- different decisions
- different domains
- different time periods
- different consequences

---

## 17. Maturity dimensions

Conceptually evaluate:

```text
Evidence Strength
Cross-Context Coverage
Temporal Stability
Explanatory Power
Predictive Power
Contradiction Penalty
```

Do not show numeric scores by default.

---

## 18. Promotion

Promote an insight when independent supporting evidence accumulates.

Example:

```text
Weak Signal:
"You may prefer classification."
```

Later:

```text
customer grading
+
opportunity grading
+
risk grading
```

→ Emerging Pattern.

Later:

```text
product prioritization
+
sales ranking
+
workflow state design
```

→ Strong Insight.

If later behavior is predicted and confirmed across contexts, it may eventually become a Personal Principle.

---

## 19. Demotion

Insights must be allowed to weaken.

Example:

Strong Insight:

> You always prefer automation.

New evidence shows important processes are intentionally left manual.

Possible refinement:

> You automate repetitive execution but preserve human judgment in high-ambiguity decisions.

A system that only promotes insights will become confidently wrong.

---

## 20. Retirement

Retire an insight when:

- new evidence consistently contradicts it;
- its context no longer exists;
- a deeper insight fully explains it;
- it was based on weak or mistaken evidence;
- the user's behavior clearly changed.

Retired insights may still matter when analyzing change over time.

---

## 21. Insight evolution

When meaning changes, show the evolution.

Preferred form:

> **This insight has evolved.**
>
> Earlier evidence suggested X.
> Newer evidence suggests Y.
> The difference matters because Z.

---

## 22. Predictive validation

Prediction is one of the strongest maturity tests.

If an insight predicts that the user will independently create states, levels, thresholds, or triggers in a new domain — and later behavior confirms this — maturity should increase significantly.

---

## 23. Disconfirmation test

Before promoting to Strong Insight or Personal Principle, ask:

```text
When did the user NOT behave this way?
Under what conditions does this pattern fail?
Could the environment explain it instead?
Could another explanation fit the same evidence?
```

Prefer revised accuracy over elegant certainty.

---

## 24. Insight registry

Conceptually maintain:

```yaml
insight:
  id:
  title:
  core_claim:
  first_seen:
  last_updated:
  maturity:
  confidence:
  scope:
  supporting_evidence:
  contradictory_evidence:
  related_insights:
  absorbed_insights:
  implications:
  open_questions:
  status:
```

Possible status:

```text
active
evolving
challenged
merged
retired
```

---

## 25. Delta-first rule

When insight history exists, focus on what changed:

```text
New insight
New evidence
Insight upgraded
Insight weakened
Insight merged
Insight contradicted
New implication
```

Do not repeat mature insights simply because they remain true.

---

## 26. Long-term success

The desired progression is:

```text
"You did X."
↓
"You often do X."
↓
"X and Y come from the same underlying method."
↓
"That method predicts how you approach new problems."
↓
"Because the pattern is established, here is a new implication you have not explored."
```

The goal is not an ever-growing list of observations.

It is to **compress experience into increasingly accurate explanations that generate new deductions**.
