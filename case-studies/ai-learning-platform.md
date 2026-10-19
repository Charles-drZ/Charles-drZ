# AI-assisted Swift learning platform

**A private full-stack product for teaching Swift, SwiftUI, and iOS through structured evidence of understanding.**

The product is in active development. Its internal working name is intentionally not used as the public commercial brand while naming work remains open.

## Product thesis

The platform is not designed as a video catalogue with an AI chat box attached.

The learning loop is built around proving understanding:

```text
learn
→ explain it back
→ solve / trace / debug
→ tutor challenges the mental model
→ evidence is evaluated
→ mastery state changes
→ next learning step
```

The goal is to help learners understand, review, and debug Swift/iOS code — including code produced with AI tools — rather than merely complete content.

## Current engineering scope

The system now spans product UX, bounded interactive learning, assessment logic, AI/retrieval architecture, and deployable application infrastructure.

### Application and learning UX

- Next.js / React application architecture;
- TypeScript and Node.js server runtime;
- PostgreSQL-backed product state;
- Drizzle-based data access and reviewed migrations;
- REST/OpenAPI boundaries for externally useful operations;
- an editable, Xcode-inspired Swift exercise surface with syntax highlighting and line numbers;
- step-based **edit → predict → feedback** beginner interaction;
- deterministic bounded code checking instead of arbitrary Swift execution;
- explicit positive/needs-work/prediction feedback states;
- staged challenge design that can require use of the learner's existing variable rather than accepting a hard-coded final result;
- a guarded own-words **EXPLAIN** answer form for a versioned Objective 1.1 question;
- honest saved/pending status rather than presenting submission as approval;
- account-scoped, private per-attempt status retrieval with manual refresh and no polling.

### Learning and AI

- a defined first sellable curriculum;
- structured evidence taxonomy and mastery states;
- deterministic assessment for the currently bounded coding exercises;
- tutor decision contracts;
- a default-disabled one-shot mock evaluation coordinator;
- distinct **PRIMARY** and independent **JUDGE** model roles with separate provider instances and cost/token bounds;
- a disposable-PostgreSQL integration proof of the complete PRIMARY → JUDGE → reconciliation-proposal path;
- explicit separation between a proposal and a final TutorReview/mastery decision;
- evaluation/golden-suite work;
- source-grounded retrieval rather than unsupported model recall;
- structured tutor/provider abstraction;
- OpenAI Responses provider integration;
- provider independence so product learning contracts are not coupled to one model vendor.

### Swift/iOS knowledge system

The learning system is backed by an immutable, provenance-aware Swift/iOS corpus built from legally usable primary and open-source material.

The source system includes current Swift language and ecosystem material, licensed Apple sample-code sources where redistribution is permitted, selected independent open-source references, freshness classification, legacy recognition, and traceable retrieval releases.

The intent is to keep technical truth grounded in source evidence while authoring the actual Hungarian learning experience separately.

### Deployment and operations

The current delivery foundation is exercised through immutable staging release candidates and includes:

- isolated staging and production Compose environments;
- PostgreSQL role and migration boundaries;
- non-root application runtime;
- immutable application image publication;
- Caddy ingress;
- explicit secret transport;
- database-backed readiness;
- release-lock metadata and immutable GHCR image candidates;
- rootless self-hosted Linux runner publication for main-branch release images;
- explicit staging promotion and browser product review;
- manual production promotion;
- previous-release rollback;
- encrypted off-host backup;
- restore drills and disaster-recovery documentation.

Infrastructure behavior is treated as part of product reliability rather than an afterthought.

## Engineering principles

**Evidence before confidence.** Tutor output does not become learning truth simply because a model produced it.

**Provider independence.** Product and learning contracts sit above individual LLM providers.

**Small sellable loop first.** The first goal is a usable learning loop that teaches through doing, not a giant content library.

**Immutable deployment evidence.** Releases, corpus versions, and retrieval artifacts are pinned and validated rather than inferred from mutable state.

**Fail closed.** Missing source evidence, invalid release identity, broken readiness, or incomplete operational guarantees should block progression instead of being silently ignored.

**Recovery is a feature.** Backup, rollback, and restore are designed alongside deployment.

## Technology

Next.js · React · TypeScript · Node.js · PostgreSQL · Drizzle · REST/OpenAPI · Zod · Vitest · Playwright · Docker · Docker Compose · Caddy · GitHub Actions · LLM provider APIs · retrieval systems

## What this project demonstrates

This project combines several engineering surfaces in one product:

- full-stack web product development;
- AI-assisted product architecture;
- tutor and evaluation contracts;
- retrieval and source provenance;
- curriculum and mastery modeling;
- relational data design;
- production deployment and rollback;
- backup and disaster recovery;
- security and secret boundaries;
- evidence-driven delivery.

## Public boundary

The implementation repository is private.

This case study intentionally omits:

- the current internal product codename as a public brand claim;
- private application source;
- provider credentials;
- deployment secrets;
- learner data;
- private prompts and evaluation fixtures;
- reusable operational access details.

Public material focuses on architecture, verified capability, engineering decisions, and current product scope.


## Current October 2026 product slice

The learner-facing slice is intentionally small but real.

A beginner receives a short Swift program, edits code in an accessible browser-native editor, predicts the output, and receives deterministic feedback. The exercise can reject a hard-coded final result when the learning objective is the operation and mental model rather than accidental output equivalence.

A second, merge-accepted slice now asks the learner to explain a Swift concept in their own words. The answer can be saved through the guarded EXPLAIN Attempt API and later queried through a private, account-scoped status endpoint. The UI remains explicit that **saved / evaluating / proposed** is not the same as approved.

Behind that surface, a default-off mock tutor path has been exercised end-to-end against disposable PostgreSQL using two distinct roles: PRIMARY and an independent JUDGE. The successful integration records model invocations, usage/cost evidence and an append-only reconciliation proposal while producing **zero TutorReview, zero mastery update and zero fake learner grade**. A deliberately wrong/source-inconsistent fixture fails closed before independent judgment.

### Current qualification frontier

A newer Module 1 learning stack is still in draft qualification rather than accepted product state. It includes:

- local `@State` practice;
- Binding trace/repair work;
- ungraded transfer practice;
- a reducer-owned guided flow that prevents advancing on wrong/missing answers and invalidates stale approval when an earlier answer changes;
- rendered lesson/navigation safety contracts;
- CI-green transition and production-build checks;
- an operator-run Xcode 27 source/typecheck verifier reporting **8/8 expected outcomes**, including one deliberate compile-failure lesson.

Those draft slices are not presented as deployed learner behavior until browser, accessibility and human pedagogical acceptance are complete.

The product is still **not** presented as arbitrary Swift execution, a complete mastery system, or a fully qualified live AI tutor. Those boundaries remain explicit while the smallest useful proof-of-understanding loop is hardened.
