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

The system now spans both product logic and deployable application infrastructure.

### Application

- Next.js / React application architecture;
- TypeScript and Node.js server runtime;
- PostgreSQL-backed product state;
- Drizzle-based data access and reviewed migrations;
- REST/OpenAPI boundaries for externally useful operations;
- structured tutor/provider abstraction;
- OpenAI Responses provider integration;
- learner evidence and mastery contracts.

### Learning and AI

- a defined first sellable curriculum;
- structured evidence taxonomy and mastery states;
- tutor decision contracts;
- evaluation/golden-suite work;
- source-grounded retrieval rather than unsupported model recall;
- provider abstraction so tutor behavior is not coupled to one model vendor.

### Swift/iOS knowledge system

The learning system is backed by an immutable, provenance-aware Swift/iOS corpus built from legally usable primary and open-source material.

The source system includes current Swift language and ecosystem material, licensed Apple sample-code sources where redistribution is permitted, selected independent open-source references, freshness classification, legacy recognition, and traceable retrieval releases.

The intent is to keep technical truth grounded in source evidence while authoring the actual Hungarian learning experience separately.

### Deployment and operations

The current deployment foundation includes:

- isolated staging and production Compose environments;
- PostgreSQL role and migration boundaries;
- non-root application runtime;
- immutable application image publication;
- Caddy ingress;
- explicit secret transport;
- database-backed readiness;
- manual production promotion;
- previous-release rollback;
- encrypted off-host backup;
- restore drills and disaster-recovery documentation.

Infrastructure behavior is treated as part of product reliability rather than an afterthought.

## Engineering principles

**Evidence before confidence.** Tutor output does not become learning truth simply because a model produced it.

**Provider independence.** Product and learning contracts sit above individual LLM providers.

**Small sellable loop first.** The first goal is a usable learning loop, not a giant content library.

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
