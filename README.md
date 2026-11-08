<div align="center">

# Károly Henrik Darázsi

### Apple Platform Developer · Swift / SwiftUI · iOS, watchOS & macOS

I build native Apple-platform products — and an evidence-driven development workflow around them.

<br>

<img src="https://img.shields.io/badge/Swift-111111?style=flat-square&logo=swift&logoColor=white" alt="Swift">
<img src="https://img.shields.io/badge/SwiftUI-111111?style=flat-square&logo=apple&logoColor=white" alt="SwiftUI">
<img src="https://img.shields.io/badge/iOS-111111?style=flat-square&logo=apple&logoColor=white" alt="iOS">
<img src="https://img.shields.io/badge/watchOS-111111?style=flat-square&logo=apple&logoColor=white" alt="watchOS">
<img src="https://img.shields.io/badge/macOS-111111?style=flat-square&logo=apple&logoColor=white" alt="macOS">
<img src="https://img.shields.io/badge/Xcode-111111?style=flat-square&logo=xcode&logoColor=white" alt="Xcode">

</div>

---

I'm a software engineer focusing my independent product work on **Apple's ecosystem**: native iPhone and Apple Watch experiences, macOS developer tools, platform frameworks, persistence, lifecycle and real-device validation.

I use AI coding agents and task-specific Codex skills to support the work — not as a substitute for understanding Swift, testing with Xcode or making engineering decisions.

## Apple-platform work

### [GlassBox](https://github.com/Charles-drZ/glassbox-showcase) · iOS & watchOS

`Swift` `SwiftUI` `SwiftData` `CloudKit` `HealthKit` `StoreKit 2` `watchOS`

My long-running iPhone wellbeing/productivity product, built around habits, tasks, mood, journaling and gentle progression. Its **Settle** companion is a native, standalone Apple Watch meditation experience with physically exercised session continuity, Digital Crown interaction and HealthKit integration.

Current iPhone engineering includes source-aware wellbeing history and careful Habit scheduling/persistence. Recent merged work adds a seven-day Habits overview and read-first Habit Detail while preserving honest pending/unknown states. The app remains in **TestFlight and product hardening**, not an App Store-shipped claim.

**What this demonstrates:** native Apple product ownership, SwiftUI state and interaction design, persistence/recovery, Apple frameworks, device-specific behavior and disciplined validation.

[Explore GlassBox →](https://github.com/Charles-drZ/glassbox-showcase)

---

### [GlassPort](https://github.com/Charles-drZ/glassport-showcase) · Native macOS developer tooling

`Swift` `AppKit` `SwiftTerm` `PTY` `OpenSSH` `XCTest`

A native macOS workspace for local shells and SSH-based development, built around durable Workspaces, Ports, terminal tabs and independently live Sessions.

Its accepted foundation includes system OpenSSH, a focused companion terminal pane, per-session local launch directories and restoration of workspace/tab/layout intent across relaunch — without claiming that dead PTYs or SSH processes survive. Newer command, theme and SSH tooling remains under qualification.

**What this demonstrates:** AppKit engineering, macOS UX, native process lifecycle, security boundaries and persistent-vs-ephemeral state modeling.

[Explore GlassPort →](https://github.com/Charles-drZ/glassport-showcase)

---

### [Skill-guided Apple development workflow](https://github.com/Charles-drZ/glassbox-development-workflow) · Codex, SwiftUI & Xcode

`Codex` `Build iOS Apps` `SwiftUI Expert` `Xcode` `XCTest` `AGENTS.md`

The workflow behind GlassBox now routes Codex to **relevant specialist skills**: the official Build iOS Apps plugin, a pinned SwiftUI Expert reference, and custom native Xcode-diagnosis and test-evidence skills.

The project records a successful bounded, read-only skill/subagent pilot. Skills do not grant build, device, protected-data, merge or release authority. Xcode output, physical-device observations and human Product acceptance remain separate evidence classes.

**What this demonstrates:** practical use of coding agents in an actual Apple project, specialized tool routing, careful source validation and explicit engineering boundaries — rather than a claim that AI automatically writes verified apps.

[Read the Apple skill-routing case study →](https://github.com/Charles-drZ/glassbox-development-workflow/blob/main/docs/skill-guided-apple-development.md)

## Swift education & learning tooling

### [AI-assisted Swift learning platform](case-studies/ai-learning-platform.md)

A private, Hungarian-language **web learning product for Swift and iOS development**. It uses an editable Swift exercise, an `edit → predict → feedback` loop, guarded own-words explanations and source-grounded assessment contracts. A default-off mock PRIMARY/JUDGE evaluation path has PostgreSQL integration evidence, but it is not presented as a qualified live tutor or automatic mastery system.

This is a *Swift education project built with web technologies*, not a native iOS app.

[Read the case study →](case-studies/ai-learning-platform.md)

## How I work

- **Native-first:** Swift, SwiftUI and AppKit where they fit; Xcode and Apple platform behavior are the reference points.
- **Skills for the task:** focused Codex/SwiftUI/Xcode guidance instead of blindly loading every installed skill.
- **Evidence over output:** source review, builds, XCTest, runtime checks and physical-device acceptance answer different questions.
- **Safe persistence:** pay attention to restoration, lifecycle, data authority and failure states — especially in CloudKit, HealthKit and app-owned state.
- **Human ownership:** agents assist implementation and investigation; product scope, risky operations and release acceptance remain explicit.

## Engineering writing

- **[Skill-guided Codex for Apple development](https://github.com/Charles-drZ/glassbox-development-workflow/blob/main/docs/skill-guided-apple-development.md)** — task-specific skills, a verified bounded pilot and native validation boundaries.
- **[Durable intent is not runtime state](engineering-notes/glassport-durable-intent-vs-runtime-state.md)** — the macOS terminal state model behind GlassPort.
- **[A tutor proposal is not mastery](engineering-notes/ai-learning-evidence-before-mastery.md)** — evidence boundaries in a Swift education product.

[All engineering notes →](engineering-notes/README.md)

## Other engineering work

My earlier and parallel work also includes Go/Linux systems, full-stack development and AI-agent runtime experiments. They show technical breadth, but **Apple-platform development is my primary direction**.

- **[Glassoft Agent Runtime](https://github.com/Charles-drZ/glassoft-agent-runtime-showcase)** — experimental Go agent execution, lifecycle and failure/reconciliation engineering; not my current portfolio focus.
- **[NodeMedic](https://github.com/Charles-drZ/nodemedic-showcase)** — local-first Go/Linux diagnostics and a privacy-bounded remote monitoring product.
- **[GlasSoft Web](case-studies/glassoft-web.md)** — bilingual Next.js/React portfolio product, accessibility and browser QA.
- **[Raspberry Home](https://github.com/Charles-drZ/raspberry-home-showcase)** — Raspberry Pi / Home Assistant operation and recovery.
- **[Glassoft Infrastructure](case-studies/glassoft-infrastructure.md)** and **[Automation workflow](https://github.com/Charles-drZ/automation-workflow-showcase)** — supporting infrastructure and evidence workflows.

## Technical focus

**Apple platforms**  
Swift · SwiftUI · AppKit · iOS · watchOS · macOS · Xcode · XCTest · SwiftData · CloudKit · HealthKit · StoreKit 2 · Sign in with Apple · TestFlight

**Apple developer tooling**  
SwiftTerm · PTY/process lifecycle · system OpenSSH · native macOS interaction · persistence/relaunch

**Development workflow**  
Codex · task-specific agent skills · AGENTS.md · native Xcode validation · GitHub PR review · evidence-based acceptance

**Supporting experience**  
TypeScript · React · Next.js · PostgreSQL · Go · Linux · Docker · GitHub Actions · system integration

## Background

My professional background is in critical communications, provisioning, device management, Linux troubleshooting and system integration. That work reinforced the engineering habits I bring to Apple products: traceability, repeatability, data safety and recovery.

## Public source boundary

GlassBox, GlassPort and the Swift learning platform have private implementation repositories. Public case studies describe verified behavior, engineering choices and limitations without exposing proprietary code, private configurations or user data.

<div align="center">

### Contact

[LinkedIn](https://linkedin.com/in/charles-drzs) · [GitHub](https://github.com/Charles-drZ)

<sub>Portfolio focus reviewed: November 2026.</sub>

</div>
