<div align="center">

# Károly Henrik Darázsi

### Software Engineer | iOS, Automation & Infrastructure

I build Apple-platform products and the engineering systems that make them reliable.

Swift · SwiftUI · Go · Linux · Docker · Automation · Reliability

</div>

---

I am a software engineer working across product development, automation, infrastructure, and reliability.

My main product is **GlassBox**, an independent iPhone self-care and productivity app. Around it I have built the engineering systems needed to develop and operate a real product: persistence and restore validation, Apple-platform integrations, release workflows, project-memory automation, production infrastructure, and physical-device testing.

Alongside GlassBox I build **NodeMedic**, a Go-based diagnostics and reliability product for Pi Network node operators, and **Raspberry Home**, a production homelab platform where I develop guarded operations, rollback-aware deployment tooling, Home Assistant interfaces, and runtime validation.

The common thread is simple: I like systems where product behavior, implementation, operations, and evidence all have to agree.

## Selected engineering work

### [GlassBox](https://github.com/Charles-drZ/glassbox-showcase)

An independently developed iPhone productivity and self-care product built with SwiftUI, SwiftData, CloudKit, StoreKit 2, HealthKit, and Sign in with Apple.

I own the product end to end: product shaping, implementation, persistence and restore behavior, Apple-platform integrations, localization, physical-device validation, TestFlight work, and release readiness. A watchOS meditation experience is now being explored through a real-device prototype path.

**Engineering signal:** long-lived Apple-platform product ownership rather than isolated sample-app development.

### [NodeMedic](https://github.com/Charles-drZ/nodemedic-showcase)

A local-first diagnostics and reliability toolkit for Pi Network Nodes, implemented in Go.

The working system includes deterministic diagnostics, structured evidence, terminal and JSON reporting, sanitized support bundles, SQLite-backed scan history, a local API and embedded dashboard, scheduled health checks, health-transition tracking, rootless Linux service operation, and deterministic multi-platform release packaging. Cloud/agent foundations are being developed with explicit identity, credential, enrollment, and trust boundaries.

**Engineering signal:** systems programming, product architecture, persistence, security boundaries, service lifecycle, and release engineering in one product.

### [Raspberry Home](https://github.com/Charles-drZ/raspberry-home-showcase)

A Raspberry Pi 5 / Docker / Home Assistant platform treated as an engineering system rather than an ad-hoc homelab.

The project covers responsive Home Assistant UI work, cross-client validation, backup and rollback, repository safety checks, guarded updates, transactional recovery, fail-closed operational behavior, and tightly constrained privileged boundaries.

**Engineering signal:** infrastructure and reliability work validated against a real running environment.

### Engineering systems

My supporting engineering workflow separates product intent, implementation evidence, runtime validation, and durable knowledge instead of treating chat history or task status as truth.

- [Development workflow](https://github.com/Charles-drZ/glassbox-development-workflow) — scoped delivery, evidence, review, and durable project memory.
- [Automation workflow](https://github.com/Charles-drZ/automation-workflow-showcase) — n8n-based deterministic evidence collection and review-gated project-memory synchronization.

These systems support the products above; they are not substitutes for implementation or runtime acceptance.

## Technical scope

### Apple platforms

Swift · SwiftUI · SwiftData · CloudKit · StoreKit 2 · HealthKit · Sign in with Apple · watchOS prototyping · XCTest · Xcode · TestFlight · localization

### Systems and reliability

Go · Linux · Docker · SQLite · systemd · Raspberry Pi 5 · Home Assistant · networking · HTTP APIs · service lifecycle · backup/restore · rollback · runtime diagnostics

### Automation and delivery

Git · GitHub · GitHub Actions · Linear · n8n · Python · Bash · YAML · JSON · OpenAI API · structured evidence pipelines · review-gated automation

## Engineering approach

I prefer explicit boundaries over hidden assumptions: scoped changes, deterministic behavior where possible, fail-closed handling when evidence is incomplete, rollback before risky mutation, and validation against the real runtime or device when the result is user-facing.

AI tools are part of my development environment, but product decisions, security boundaries, publication decisions, and final runtime acceptance remain human responsibilities.

## Professional background

I work in broadband critical communications, contributing to provisioning, device management, system integration, Linux-based troubleshooting, technical documentation, and automation. That environment has reinforced habits around evidence, recovery, repeatable procedures, and clear operational boundaries.

## Public portfolio boundary

The core product and operations repositories remain private where publishing implementation would expose proprietary logic, unreleased product material, credentials, network details, or operational controls. Public repositories contain independently written case studies, sanitized architecture, privacy-reviewed visuals, and verified outcomes.

## Contact

- [LinkedIn](https://linkedin.com/in/charles-drzs)
- [GitHub](https://github.com/Charles-drZ)

<sub>Technical profile last reviewed: September 2026.</sub>
