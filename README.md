<div align="center">

# Károly Henrik Darázsi

### Software Engineer · AI Engineering · iOS Development

I build software products and the engineering systems around them: Apple-platform apps, AI-assisted products, agent runtimes, full-stack web systems, developer tooling, reliability, automation, and production infrastructure.

<br>

<img src="https://img.shields.io/badge/Swift-111111?style=flat-square&logo=swift&logoColor=white" alt="Swift">
<img src="https://img.shields.io/badge/TypeScript-111111?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
<img src="https://img.shields.io/badge/Go-111111?style=flat-square&logo=go&logoColor=white" alt="Go">
<img src="https://img.shields.io/badge/PostgreSQL-111111?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL">
<img src="https://img.shields.io/badge/Docker-111111?style=flat-square&logo=docker&logoColor=white" alt="Docker">
<img src="https://img.shields.io/badge/Linux-111111?style=flat-square&logo=linux&logoColor=white" alt="Linux">
<img src="https://img.shields.io/badge/NVIDIA-111111?style=flat-square&logo=nvidia&logoColor=white" alt="NVIDIA">

</div>

---

I work across product engineering, AI engineering, Apple platforms, systems, reliability, and infrastructure.

The common thread is architectural rather than framework-specific: I care about how product behavior, persistence, execution authority, process lifecycle, security boundaries, deployment, recovery, and runtime evidence fit together. AI is part of my engineering environment, but engineering authority stays in explicit contracts, tests, runtime validation, deterministic evidence, and human review.

## Selected work

### [GlassBox](https://github.com/Charles-drZ/glassbox-showcase) · Apple product engineering

`Swift` `SwiftUI` `SwiftData` `CloudKit` `StoreKit 2` `HealthKit` `watchOS`

An independently developed self-care and productivity product spanning iPhone and Apple Watch.

I own the product end to end: product shaping, implementation, persistence and restore behavior, Apple-platform integrations, localization, physical-device validation, TestFlight work, release readiness, and the supporting engineering workflow.

GlassBox now also includes **Settle**, a working watchOS meditation experience with a standalone Watch target, Digital Crown duration control, extended-runtime wrist-down continuity, Mindful Minutes export, a bounded heart-rate sidecar, haptics, recovery behavior, and repeated physical Apple Watch validation.

**What it shows:** long-lived Apple-platform product ownership across iOS and watchOS, not isolated sample-app development.

[Explore GlassBox →](https://github.com/Charles-drZ/glassbox-showcase)

---

### [Glassoft Agent Runtime](https://github.com/Charles-drZ/glassoft-agent-runtime-showcase) · AI engineering / agent runtime

`Go` `Linux` `NVIDIA` `Nemotron` `OpenCode` `OpenShell` `Agent Orchestration`

GAR is a developer-facing runtime for bounded, reviewable AI-assisted software engineering. Its current inference lane uses **NVIDIA hosted inference with the Nemotron model family**, while GAR itself remains provider- and model-neutral by design.

The system compiles GitHub Issue contracts into deterministic execution context, runs managed agent jobs on a dedicated Linux worker, preserves durable lifecycle state, keeps backend/provider/model/runtime identities separate, and exposes execution through a GAR-owned CLI rather than treating an agent terminal as lifecycle authority.

Current work includes runtime qualification, explicit authority boundaries, durable execution state, worker/backend orchestration, execution feedback, evidence capture, and fail-closed handling when required guarantees are unavailable.

**What it shows:** AI engineering as a systems problem — orchestration, security boundaries, lifecycle ownership, capability contracts, evidence, failure handling, and human gates rather than unconstrained code generation.

[Explore GAR →](https://github.com/Charles-drZ/glassoft-agent-runtime-showcase)

---

### [AI-assisted Swift learning platform](case-studies/ai-learning-platform.md) · Full-stack & AI product engineering

`Next.js` `React` `TypeScript` `Node.js` `PostgreSQL` `Drizzle` `LLM` `Docker`

A private product in active development for teaching Swift, SwiftUI, and iOS through an evidence-based learning loop rather than passive content consumption.

The current system spans curriculum and mastery contracts, a source-grounded Swift/iOS retrieval corpus, tutor-provider abstraction, structured learner evidence, PostgreSQL-backed application infrastructure, staging/production deployment boundaries, immutable releases, rollback, backup, and restore drills.

The public product name is intentionally withheld while naming work remains open.

**What it shows:** end-to-end full-stack product engineering combined with AI tutor architecture, retrieval/evaluation thinking, production deployment, and operational recovery.

[Explore the case study →](case-studies/ai-learning-platform.md)

---

### [NodeMedic](https://github.com/Charles-drZ/nodemedic-showcase) · Reliability product

`Go` `SQLite` `HTTP API` `systemd` `Linux` `Release Engineering`

A local-first diagnostics and reliability toolkit that turns host, container, network, and resource observations into deterministic findings with evidence, confidence, and a useful next step.

The working system includes terminal and JSON reports, sanitized support bundles, SQLite-backed history, a local API and embedded dashboard, scheduled health checks, health-transition tracking, rootless Linux service operation, and deterministic multi-platform release packaging.

**What it shows:** product architecture, systems programming, persistence, security boundaries, service lifecycle, and release engineering in one system.

[Explore NodeMedic →](https://github.com/Charles-drZ/nodemedic-showcase)

---

### [GlassPort](https://github.com/Charles-drZ/glassport-showcase) · Native macOS developer tooling

`Swift` `AppKit` `SwiftTerm` `PTY` `OpenSSH` `Xcode`

A native macOS workspace for local and remote development environments.

The validated foundation includes a real local zsh terminal over PTY, system OpenSSH sessions, safe host discovery from `~/.ssh/config`, durable workspace persistence, workspace switching and lifecycle management, and native macOS validation.

**What it shows:** developer-tool architecture, process/session lifecycle design, native macOS engineering, persistence boundaries, and integration with trusted system tools.

[Explore GlassPort →](https://github.com/Charles-drZ/glassport-showcase)

---

### [Raspberry Home](https://github.com/Charles-drZ/raspberry-home-showcase) · Infrastructure & operations

`Raspberry Pi` `Docker` `Home Assistant` `Python` `Bash` `GitHub Actions`

A real home platform treated as an engineering system rather than a collection of containers.

The project combines responsive Home Assistant product work with backup and rollback, repository safety checks, guarded updates, transactional recovery, fail-closed operational behavior, constrained privileged boundaries, and validation against the real running environment.

**What it shows:** infrastructure and reliability engineering with real operational consequences, not a disposable lab setup.

[Explore Raspberry Home →](https://github.com/Charles-drZ/raspberry-home-showcase)

---

### [Glassoft Infrastructure](case-studies/glassoft-infrastructure.md) · Production infrastructure

`Linux` `Docker` `Caddy` `TLS` `Tailscale` `Backup / Restore` `Observability`

Production infrastructure behind private Glassoft products: deliberately small public ingress, private administration, explicit deployment contracts, independent recovery design, and monitoring that cannot become a serving dependency.

**What it shows:** network and trust boundaries, deployment discipline, disaster-recovery design, and infrastructure decisions driven by failure modes rather than novelty.

[Explore Glassoft Infrastructure →](case-studies/glassoft-infrastructure.md)

## Currently building

> **GlassBox / Settle** — iPhone release hardening and a physically validated standalone watchOS meditation experience  
> **Glassoft Agent Runtime** — NVIDIA/Nemotron-backed AI engineering runtime, bounded execution, durable jobs, and richer execution feedback  
> **AI-assisted Swift learning platform** — tutor vertical slice, retrieval/evaluation system, and production deployment foundation  
> **NodeMedic** — reliability and diagnostics tooling  
> **GlassPort** — native macOS developer workspace

## Engineering systems

The products above are backed by workflows that keep scope, implementation evidence, runtime validation, and durable knowledge separate instead of treating chat history or task status as truth.

**[Development workflow](https://github.com/Charles-drZ/glassbox-development-workflow)** — scoped delivery, source-of-truth boundaries, runtime evidence, review, and durable engineering knowledge.

**[Automation workflow](https://github.com/Charles-drZ/automation-workflow-showcase)** — deterministic evidence collection, integrity checks, bounded semantic review, and review-gated project-memory synchronization.

## Technical range

**Apple platforms**  
Swift · SwiftUI · AppKit · SwiftData · CloudKit · StoreKit 2 · HealthKit · watchOS · WKExtendedRuntimeSession · Sign in with Apple · SwiftTerm · XCTest · Xcode · TestFlight

**AI & full-stack engineering**  
Next.js · React · TypeScript · Node.js · PostgreSQL · Drizzle · REST/OpenAPI · retrieval systems · tutor/provider abstraction · structured evaluation · OpenAI Responses · Docker Compose

**Systems & reliability**  
Go · Linux · Docker · SQLite · systemd · Caddy · TLS · Tailscale · Raspberry Pi · Home Assistant · networking · HTTP APIs · service lifecycle · backup/restore · rollback · runtime diagnostics

**Automation & agent infrastructure**  
Git · GitHub · GitHub Actions · n8n · Python · Bash · YAML · JSON · NVIDIA hosted inference · Nemotron · OpenCode · OpenShell · agent orchestration · deterministic evidence pipelines · review-gated automation · execution contracts

## How I engineer

I prefer explicit boundaries over hidden assumptions: scoped changes, deterministic behavior where possible, fail-closed handling when evidence is incomplete, recovery paths before risky mutation, and validation against the real runtime or physical device when the result is user-facing.

AI tools can propose, implement, investigate, and review. Product decisions, security boundaries, merge authority, publication decisions, and final runtime acceptance remain explicit engineering responsibilities.

## Background

I work in broadband critical communications, contributing to provisioning, device management, system integration, Linux-based troubleshooting, technical documentation, and automation. It is an environment where evidence, recovery, repeatable procedures, and clear operational boundaries matter.

## Public portfolio boundary

Core product and operations source stays private where publishing it would expose proprietary logic, private product work, or operational controls. The public portfolio focuses on sanitized architecture, engineering decisions, visuals, and verified outcomes.

<div align="center">

### Contact

[LinkedIn](https://linkedin.com/in/charles-drzs) · [GitHub](https://github.com/Charles-drZ)

<sub>Technical profile last reviewed: October 2026.</sub>

</div>
