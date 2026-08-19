# insight-me

> Memory tells you what happened.  
> Reflection tells you what it meant.  
> Insight reveals what you still haven't noticed.

**insight-me** is an Agent Skill that turns your past conversations and experiences into **new insights you have not explicitly stated before**.

It is not a conversation summarizer, memory retriever, or simple experience-reuse prompt.

Its core question is:

> **What new idea becomes visible when your past experiences are viewed together?**

## What it looks for

- Hidden recurring patterns
- Unexpected connections across projects
- Contradictions between goals and behavior
- Unconscious problem-solving methods
- Missing implications of past decisions
- Abandoned ideas worth revisiting
- Repeated pain points
- Second-order effects
- Counterfactual possibilities
- Blind spots
- Emerging capabilities
- New hypotheses and directions

## The difference

### Memory

> You previously built a customer segmentation system.

### Reuse

> You could reuse customer segmentation in another project.

### insight-me

> Customer segmentation, opportunity funnels, relationship graphs, churn alerts, and 360° profiles may be different dimensions of one underlying **Customer State Model**.

That creates a new direction:

```text
Customer
├── Value State
├── Relationship State
├── Opportunity State
├── Risk State
├── Engagement State
└── Lifecycle State
```

The goal is not to remember more.

The goal is to **connect things from your past that you had never connected yourself**.

---

## Insight lifecycle

insight-me does not treat every observation as truth.

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

Insights can also be:

- strengthened
- refined
- merged
- split
- challenged
- demoted
- retired

More conversations should not produce more repetitive insights.

They should produce **fewer, deeper, better-supported insights**.

---

## Repository structure

```text
insight-me/
├── README.md
├── README.zh-CN.md
├── LICENSE
├── insight-me/
│   ├── SKILL.md
│   └── references/
│       ├── INSIGHT-ENGINES.md
│       ├── INSIGHT-MATURITY.md
│       ├── OUTPUT-GUIDE.md
│       └── EXAMPLES.md
└── tests/
    ├── cross-project-connection.md
    ├── contradiction-detection.md
    ├── deduplication.md
    ├── maturity-evolution.md
    └── false-pattern.md
```

## Usage

Typical invocations:

```text
/insight-me
/insight-me last 30 days
/insight-me career
/insight-me product ideas
/insight-me what am I missing?
/insight-me challenge my thinking
/insight-me connect things I've discussed separately
/insight-me find unfinished ideas worth revisiting
/insight-me deep
```

Default time window: **the most recent 90 days**, unless the user specifies another scope.

## Design principles

1. Do not merely summarize.
2. Do not present memory retrieval as insight.
3. Connect multiple independent experiences whenever possible.
4. Separate evidence from hypothesis.
5. Suppress duplicate insights.
6. Track insight maturity over time.
7. Actively search for contradictory evidence.
8. Prefer 3–5 high-value insights over long lists.
9. Do not overgeneralize work patterns into personality claims.
10. The ideal reaction is: **“I hadn't thought about it that way.”**

## License

MIT
