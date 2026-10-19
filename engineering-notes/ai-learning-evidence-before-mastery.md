# A tutor proposal is not mastery

An AI tutor saying "correct" is not enough evidence to update a learner's mastery state.

The Swift learning platform I am building treats model output as one part of an assessment pipeline rather than as the source of truth.

## The learning problem

For a beginner, two answers can produce the same visible result while representing very different understanding.

For example, an exercise may require the learner to update an existing Swift variable.

A hard-coded final value might print the expected output, but it does not demonstrate the intended operation.

That is why the current product uses bounded deterministic checks where possible and structured tutor evidence where semantic explanation is required.

## Own-words EXPLAIN

The current accepted flow includes a guarded own-words EXPLAIN interaction.

A learner can submit an answer tied to a versioned learning objective.

The system can persist the Attempt and later expose a private account-scoped status such as saved or evaluating.

What it deliberately does **not** do is turn HTTP 202 or a model response into:

- approved mastery;
- XP;
- a final grade;
- an authoritative tutor verdict.

## PRIMARY and independent JUDGE

A default-off qualification path exercises two distinct evaluation roles:

```text
learner Attempt
      ↓
PRIMARY evaluation
      ↓
independent JUDGE
      ↓
reconciliation proposal
      ↓
future adjudication / mastery boundary
```

The roles use separate model/provider identities in the qualification harness and persist structured invocation, usage and cost evidence.

The important word is **proposal**.

The PostgreSQL-backed integration proof intentionally ends with:

- two model-role invocations;
- usage/cost evidence;
- one append-only reconciliation proposal;
- **zero TutorReview**;
- **zero mastery update**;
- **zero fake learner grade**.

A negative source-validation fixture fails before final adjudication instead of allowing fabricated evidence to become a learner outcome.

## Why this boundary matters

LLMs are useful for semantic evaluation, but their output should not silently collapse several product concepts into one boolean.

The system keeps these separate:

- content progress;
- learner evidence;
- technical source evidence;
- tutor evaluation;
- adjudication;
- mastery state;
- longitudinal confidence.

That makes it possible to improve the tutor without rewriting what "mastery" means.

## The wider lesson

AI products become easier to trust when the model is not the database, the policy engine and the authority at the same time.

For this learning system, the rule is simple:

> **Model output can contribute evidence. Product state changes require a separate contract.**

---

[AI-assisted Swift learning platform case study →](../case-studies/ai-learning-platform.md)  
[Developer profile →](https://github.com/Charles-drZ)
