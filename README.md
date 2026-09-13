<div align="center">

# Károly Henrik Darázsi

### Software Engineer

**iOS · Automation · Infrastructure**

I build products where the app, the infrastructure, and the proof that it works all matter.

<br>

<img src="https://img.shields.io/badge/Swift-111111?style=flat-square&logo=swift&logoColor=white" alt="Swift">
<img src="https://img.shields.io/badge/Go-111111?style=flat-square&logo=go&logoColor=white" alt="Go">
<img src="https://img.shields.io/badge/Docker-111111?style=flat-square&logo=docker&logoColor=white" alt="Docker">
<img src="https://img.shields.io/badge/Linux-111111?style=flat-square&logo=linux&logoColor=white" alt="Linux">
<img src="https://img.shields.io/badge/GitHub_Actions-111111?style=flat-square&logo=githubactions&logoColor=white" alt="GitHub Actions">
<img src="https://img.shields.io/badge/n8n-111111?style=flat-square&logo=n8n&logoColor=white" alt="n8n">

</div>

---

I work across product engineering, automation, infrastructure, and reliability.

My main product is **GlassBox**, an independent Apple-platform self-care and productivity app. Alongside it I build **NodeMedic**, a Go-based diagnostics and reliability product, and **Raspberry Home**, a production homelab platform where I develop guarded operations and rollback-aware infrastructure tooling.

The common thread is not a particular framework. I like systems where product behavior, implementation, operations, and evidence all have to agree.

## Selected work

### [GlassBox](https://github.com/Charles-drZ/glassbox-showcase) · Apple product engineering

`Swift` `SwiftUI` `SwiftData` `CloudKit` `StoreKit 2` `HealthKit` `watchOS`

An independently developed self-care and productivity product built around the idea that productivity should create clarity rather than guilt.

I own the product end to end: product shaping, implementation, persistence and restore behavior, Apple-platform integrations, localization, physical-device validation, TestFlight work, and release readiness. A watchOS meditation experience is now moving through real-device prototyping.

**What it shows:** long-lived Apple-platform product ownership rather than isolated sample-app development.

[Explore GlassBox →](https://github.com/Charles-drZ/glassbox-showcase)

---

### [NodeMedic](https://github.com/Charles-drZ/nodemedic-showcase) · Reliability product

`Go` `SQLite` `HTTP API` `systemd` `Linux` `Release Engineering`

A local-first diagnostics and reliability toolkit for Pi Network Node operators. It turns host, Docker, Pi Node, network, and resource observations into deterministic findings with evidence, confidence, and a useful next step.

The working system includes terminal and JSON reports, sanitized support bundles, SQLite-backed history, a local API and embedded dashboard, scheduled health checks, health-transition tracking, rootless Linux service operation, and deterministic multi-platform release packaging. Cloud/agent foundations use explicit identity, credential, enrollment, and trust boundaries.

**What it shows:** product architecture, systems programming, persistence, security boundaries, service lifecycle, and release engineering in one system.

[Explore NodeMedic →](https://github.com/Charles-drZ/nodemedic-showcase)

---

### [Raspberry Home](https://github.com/Charles-drZ/raspberry-home-showcase) · Infrastructure & operations

`Raspberry Pi 5` `Docker` `Home Assistant` `Python` `Bash` `GitHub Actions`

A real home platform treated as an engineering system rather than a collection of containers.

The project combines responsive Home Assistant product work with backup and rollback, repository safety checks, guarded updates, transactional recovery, fail-closed operational behavior, constrained privileged boundaries, and validation against the real running environment.

**What it shows:** infrastructure and reliability engineering with real operational consequences, not a disposable lab setup.

[Explore Raspberry Home →](https://github.com/Charles-drZ/raspberry-home-showcase)

## Currently building

> **GlassBox** — release hardening and watchOS meditation prototyping  
> **NodeMedic** — authenticated Agent/Cloud state synchronization foundation  
> **Raspberry Home** — guarded operations and updater hardening

## Engineering systems

The products above are backed by a workflow that keeps scope, implementation evidence, runtime validation, and durable knowledge separate instead of treating chat history or task status as truth.

**[Development workflow](https://github.com/Charles-drZ/glassbox-development-workflow)** — scoped delivery, source-of-truth boundaries, runtime evidence, review, and durable engineering knowledge.

**[Automation workflow](https://github.com/Charles-drZ/automation-workflow-showcase)** — deterministic evidence collection, integrity checks, bounded semantic review, and review-gated project-memory synchronization.

These systems support the engineering work. They are not substitutes for implementation or runtime acceptance.

## Technical range

**Apple platforms**  
Swift · SwiftUI · SwiftData · CloudKit · StoreKit 2 · HealthKit · Sign in with Apple · watchOS · XCTest · Xcode · TestFlight

**Systems & reliability**  
Go · Linux · Docker · SQLite · systemd · Raspberry Pi · Home Assistant · networking · HTTP APIs · service lifecycle · backup/restore · rollback · runtime diagnostics

**Automation & delivery**  
Git · GitHub · GitHub Actions · Linear · n8n · Python · Bash · YAML · JSON · OpenAI API · deterministic evidence pipelines · review-gated automation

## How I engineer

I prefer explicit boundaries over hidden assumptions: scoped changes, deterministic behavior where possible, fail-closed handling when evidence is incomplete, recovery paths before risky mutation, and validation against the real runtime or device when the result is user-facing.

AI tools are part of my development environment. Product decisions, security boundaries, publication decisions, and final runtime acceptance are not delegated to them.

## Background

I work in broadband critical communications, contributing to provisioning, device management, system integration, Linux-based troubleshooting, technical documentation, and automation. It is an environment where evidence, recovery, repeatable procedures, and clear operational boundaries matter.

## Public portfolio boundary

The core product and operations repositories remain private where publishing implementation would expose proprietary logic, unreleased material, credentials, network details, or operational controls. The public repositories are independently written engineering case studies with sanitized architecture, privacy-reviewed visuals, and verified outcomes.

<div align="center">

### Contact

[LinkedIn](https://linkedin.com/in/charles-drzs) · [GitHub](https://github.com/Charles-drZ)

<sub>Technical profile last reviewed: September 2026.</sub>

</div>
