<div align="center">

# Károly Henrik Darázsi

### Software Engineer

**iOS · Automation · Infrastructure**

I build product software and the systems around it: Apple apps, macOS developer tooling, reliability products, infrastructure, automation, and bounded AI-agent execution.

<br>

<img src="https://img.shields.io/badge/Swift-111111?style=flat-square&logo=swift&logoColor=white" alt="Swift">
<img src="https://img.shields.io/badge/Go-111111?style=flat-square&logo=go&logoColor=white" alt="Go">
<img src="https://img.shields.io/badge/Docker-111111?style=flat-square&logo=docker&logoColor=white" alt="Docker">
<img src="https://img.shields.io/badge/Linux-111111?style=flat-square&logo=linux&logoColor=white" alt="Linux">
<img src="https://img.shields.io/badge/GitHub_Actions-111111?style=flat-square&logo=githubactions&logoColor=white" alt="GitHub Actions">
<img src="https://img.shields.io/badge/n8n-111111?style=flat-square&logo=n8n&logoColor=white" alt="n8n">

</div>

---

I work across product engineering, systems and reliability, automation, and infrastructure.

The common thread is architectural rather than framework-specific: I care about how product behavior, persistence, process lifecycle, security boundaries, deployment, recovery, and runtime evidence fit together. I use AI-assisted development heavily, but I keep engineering authority in explicit contracts, tests, runtime validation, and human review.

## Selected work

### [GlassBox](https://github.com/Charles-drZ/glassbox-showcase) · Apple product engineering

`Swift` `SwiftUI` `SwiftData` `CloudKit` `StoreKit 2` `HealthKit` `watchOS`

An independently developed self-care and productivity product in active TestFlight hardening.

I own the product end to end: product shaping, implementation, persistence and restore behavior, Apple-platform integrations, localization, physical-device validation, TestFlight work, release readiness, and the supporting engineering workflow.

**What it shows:** long-lived Apple-platform product ownership, not isolated sample-app development.

[Explore GlassBox →](https://github.com/Charles-drZ/glassbox-showcase)

---

### [GlassPort](https://github.com/Charles-drZ/glassport-showcase) · Native macOS developer tooling

`Swift` `AppKit` `SwiftTerm` `PTY` `OpenSSH` `Xcode`

A native macOS workspace for local and remote development environments.

The validated foundation includes a real local zsh terminal over PTY, system OpenSSH sessions, safe host discovery from `~/.ssh/config`, durable workspace persistence, workspace switching and lifecycle management, and native macOS validation.

**What it shows:** developer-tool architecture, process/session lifecycle design, native macOS engineering, persistence boundaries, and integration with trusted system tools.

[Explore GlassPort →](https://github.com/Charles-drZ/glassport-showcase)

---

### [NodeMedic](https://github.com/Charles-drZ/nodemedic-showcase) · Reliability product

`Go` `SQLite` `HTTP API` `systemd` `Linux` `Release Engineering`

A local-first diagnostics and reliability toolkit that turns host, container, network, and resource observations into deterministic findings with evidence, confidence, and a useful next step.

The working system includes terminal and JSON reports, sanitized support bundles, SQLite-backed history, a local API and embedded dashboard, scheduled health checks, health-transition tracking, rootless Linux service operation, and deterministic multi-platform release packaging.

**What it shows:** product architecture, systems programming, persistence, security boundaries, service lifecycle, and release engineering in one system.

[Explore NodeMedic →](https://github.com/Charles-drZ/nodemedic-showcase)

---

### [Glassoft Agent Runtime](https://github.com/Charles-drZ/glassoft-agent-runtime-showcase) · AI-agent infrastructure

`Go` `Linux` `OpenCode` `OpenShell` `NVIDIA Nemotron` `GitHub`

An engineering runtime for bounded, reviewable AI-agent execution across non-iOS Glassoft projects.

The current pilot includes deterministic GitHub-Issue execution packets, worker preflight, durable job-state foundations, an agent supervisor foundation, and an explicit provider-neutral backend contract. Hard sandbox qualification, scheduling, and full autonomous execution remain deliberately gated until their runtime boundaries are proven.

**What it shows:** agent orchestration as a systems problem — scope contracts, execution boundaries, capability declarations, evidence, failure handling, and human gates rather than unconstrained code generation.

[Explore GAR →](https://github.com/Charles-drZ/glassoft-agent-runtime-showcase)

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

The production infrastructure behind GlassBox: deliberately small public ingress, private administration, explicit deployment contracts, independent recovery design, and monitoring that cannot become a serving dependency.

**What it shows:** network and trust boundaries, deployment discipline, disaster-recovery design, and infrastructure decisions driven by failure modes rather than novelty.

[Explore Glassoft Infrastructure →](case-studies/glassoft-infrastructure.md)

## Currently building

> **GlassBox** — release hardening and watchOS meditation prototyping  
> **GlassPort** — native macOS workspace and developer-tool workflow  
> **NodeMedic** — authenticated Agent/Cloud synchronization foundations  
> **Glassoft Agent Runtime** — bounded issue-driven agent execution and orchestration  
> **Raspberry Home** — guarded operations and deployment hardening

## Engineering systems

The products above are backed by workflows that keep scope, implementation evidence, runtime validation, and durable knowledge separate instead of treating chat history or task status as truth.

**[Development workflow](https://github.com/Charles-drZ/glassbox-development-workflow)** — scoped delivery, source-of-truth boundaries, runtime evidence, review, and durable engineering knowledge.

**[Automation workflow](https://github.com/Charles-drZ/automation-workflow-showcase)** — deterministic evidence collection, integrity checks, bounded semantic review, and review-gated project-memory synchronization.

## Technical range

**Apple & macOS**  
Swift · SwiftUI · AppKit · SwiftData · CloudKit · StoreKit 2 · HealthKit · Sign in with Apple · watchOS · SwiftTerm · PTY/process lifecycle · OpenSSH · XCTest · Xcode · TestFlight

**Systems & reliability**  
Go · Linux · Docker · SQLite · systemd · Caddy · TLS · Tailscale · Raspberry Pi · Home Assistant · networking · HTTP APIs · service lifecycle · backup/restore · rollback · runtime diagnostics

**Automation & agent infrastructure**  
Git · GitHub · GitHub Actions · n8n · Python · Bash · YAML · JSON · OpenCode · OpenShell · NVIDIA Nemotron · deterministic evidence pipelines · review-gated automation · execution contracts

## How I engineer

I prefer explicit boundaries over hidden assumptions: scoped changes, deterministic behavior where possible, fail-closed handling when evidence is incomplete, recovery paths before risky mutation, and validation against the real runtime or device when the result is user-facing.

AI tools are part of my engineering environment. Product decisions, security boundaries, publication decisions, and final runtime acceptance are not delegated to them.

## Background

I work in broadband critical communications, contributing to provisioning, device management, system integration, Linux-based troubleshooting, technical documentation, and automation. It is an environment where evidence, recovery, repeatable procedures, and clear operational boundaries matter.

## Public portfolio boundary

Core product and operations source stays private where publishing it would expose proprietary logic or operational controls. The public portfolio focuses on sanitized architecture, engineering decisions, visuals, and verified outcomes.

<div align="center">

### Contact

[LinkedIn](https://linkedin.com/in/charles-drzs) · [GitHub](https://github.com/Charles-drZ)

<sub>Technical profile last reviewed: September 2026.</sub>

</div>
