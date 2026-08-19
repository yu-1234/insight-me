# Examples

## Example 1 — Summary vs Insight

Past experiences:

```text
Customer segmentation
Opportunity funnel
Relationship graph
Churn alert
360° customer profile
```

### Bad

> You have built several customer-analysis tools.

Why bad:

- summary only
- no new connection
- no new implication

### Better

> These systems could potentially be integrated.

Why still weak:

- obvious
- solution-first
- does not explain the deeper common structure

### Good insight

> These five projects may not actually be five separate tools. Each describes a different dimension of one underlying object: **customer state**.

Possible model:

```text
Customer
├── Value State
├── Relationship State
├── Opportunity State
├── Risk State
├── Engagement State
└── Lifecycle State
```

Second-order implication:

```text
Customer State
↓
State Change
↓
Trigger
↓
Recommended Action
```

Question:

> If every customer had one dynamically changing state model, which decisions could be triggered automatically without requiring a person to inspect five separate dashboards?

---

## Example 2 — Contradiction

Past evidence:

```text
Goal:
launch a product quickly

Behavior:
continuously adding finance, inventory, CRM, OCR,
salary, logistics, dashboard and workflow modules
```

Weak output:

> The product has many features.

Good insight:

> There is a tension between commercialization speed and product scope. The product may be drifting from a focused painkiller into a general ERP-style platform.

Question:

> If you had to sell the product tomorrow and could keep only one painful business problem, which problem would still justify buying it?

---

## Example 3 — Unconscious method

Independent past projects repeatedly show:

```text
collect
→ structure
→ classify
→ measure
→ detect
→ act
```

Weak output:

> You like structured analysis.

Better:

> Across unrelated projects, you repeatedly externalize fuzzy judgment into explicit states, thresholds, and triggers. The repeated capability may be **decision-system design**, not merely BI or reporting.

Question:

> What would change if you designed your future projects around the reusable decision logic first, and treated dashboards as only one interface?

---

## Example 4 — Deduplication

Existing insight:

> You repeatedly reduce ambiguity through classification.

New evidence:

- risk grading
- product grading

Bad:

> New insight: you also like grading risks and products.

Good:

> The existing classification insight is strengthened by two independent contexts. Its scope may now extend from customer management to a broader decision-design method.

---

## Example 5 — Maturity evolution

### First occurrence

> The user uses customer grading.

Classification:

```text
Observation
```

### Later

Customer grading + opportunity grading.

Possible:

```text
🌱 Weak Signal
```

> You may prefer reducing ambiguity through explicit categories.

### Later

Risk grading + product prioritization + sales ranking.

Possible:

```text
🌳 Strong Insight
```

> You repeatedly convert fuzzy business judgment into explicit states, thresholds, and prioritization rules.

### Later predictive confirmation

A new project independently introduces:

- states
- thresholds
- triggers

Possible:

```text
🧭 Personal Principle
```

> When complexity rises, you tend to externalize repeated judgment into systems rather than asking people to make the same decision from scratch.

---

## Example 6 — Repeated pain

Past complaints:

```text
too much reporting
can't see the priority
not actionable
too fragmented
```

Weak:

> You dislike complicated dashboards.

Better:

> The recurring pain may not be dashboard design. It may be **attention allocation**: information is increasing faster than the organization's ability to decide what deserves action.

Second-order implication:

> As AI makes report generation cheaper, prioritization and next-action recommendation may become more valuable than reporting itself.

---

## Example 7 — Counterfactual

Past work is customer-centered.

Counterfactual question:

> What if the customer is not the main object?

Alternative:

```text
Event
├── financing
├── IND / clinical progress
├── executive change
├── visit
├── opportunity
├── order
└── after-sales issue
```

Possible insight:

> A customer system could be reinterpreted as an event-driven commercial intelligence system: events change customer state, which triggers recommended actions.

This insight does not simply reuse a prior method; it changes the system's organizing principle.
