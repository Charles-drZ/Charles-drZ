# Glassoft Infrastructure

**Production infrastructure, deployment boundaries, recovery, and observability for an independent Apple-platform product.**

`Linux` `Docker` `Caddy` `TLS` `Tailscale` `Backup/Restore` `Observability`

Glassoft Infrastructure is the operational layer behind GlassBox. The application source stays in its own private repository; this system defines how the production backend is exposed, administered, recovered, and observed.

The interesting part is not that a VPS exists. It is the set of boundaries around it.

## Production shape

```text
Internet
   │
   ▼
HTTPS / Caddy
   │
   ▼
loopback-only application backend
   │
   ▼
server-side integrations and protected state
```

The first production architecture is deliberately small: one VPS, one public HTTPS edge, a private application listener, and explicit operational contracts.

There is no Kubernetes cluster, no invented microservice split, and no scaling claim without measurements. The system is designed so that the public API contract can remain stable while the infrastructure underneath it evolves.

## Network and trust boundaries

The backend is not exposed directly to the internet. Caddy owns the public HTTP/TLS edge while the application listens only on loopback.

Administrative access is private rather than part of the serving path. Tailscale is used as an operations transport, but production availability must not depend on Tailscale, my home network, or the Raspberry Pi operations node.

That distinction is intentional:

- the public service should keep running when the home environment is offline;
- administration and monitoring should not silently become production dependencies;
- privileged access stays separate from application traffic;
- only the minimum public surface is exposed.

## Deployment discipline

Application and infrastructure ownership are separated.

The product repository owns application behavior. The infrastructure repository owns deployment contracts, public ingress, host security, secret-handling boundaries, backup/restore, monitoring, and recovery documentation.

Deployments are built around reviewed configuration and immutable release identity rather than treating a production host checkout as the source of truth.

A change is not considered complete merely because a container starts. The validation path checks the private application boundary first and the public HTTPS path second.

## Backup and recovery

Backup design starts by classifying what is actually unique state and what can be reconstructed from reviewed source or immutable artifacts.

That prevents two common mistakes: backing up huge amounts of replaceable data, and assuming a provider snapshot is the same thing as independent disaster recovery.

The recovery model distinguishes between:

- protected configuration and secret state that must survive host loss;
- application/deployment material that should be reconstructed from reviewed source and immutable releases;
- ephemeral logs, caches, certificates, and host identity that should not simply be cloned onto a replacement machine;
- provider-managed backups, which are useful but remain inside the provider failure domain.

Restore procedures are designed to be tested in isolation before they can touch live production state.

## Observability without turning monitoring into the product

The current stage does not justify a public metrics stack or a large monitoring platform.

Useful signals are deliberately small and operational: public HTTPS health, service state, restart behavior, coarse host resource pressure, certificate expiry, and backup freshness.

External observation may run from private operations infrastructure, but losing that observer must never affect the production API itself.

This keeps observability proportional to the system instead of introducing infrastructure for its own sake.

## Security posture

The infrastructure is designed around explicit invariants:

- HTTPS-only public traffic;
- minimum public ports;
- private administrative access;
- no production secrets or private keys in Git;
- no secret material baked into container images;
- server-side provider credentials remain server-side;
- operational logging avoids user-content analytics and sensitive payloads;
- recovery procedures do not copy host identity or broad privileged state blindly.

These are engineering constraints, not aspirational checklist items; they are part of how production changes are reviewed.

## The home Pi boundary

A Raspberry Pi can provide useful private operations capabilities such as external health checks, automation, or encrypted off-host backup.

It is explicitly **not** allowed to become the primary public backend or a hidden availability dependency.

That boundary matters because a home ISP outage, router restart, Pi failure, or private-overlay outage should degrade operations visibility at most — not take the product offline.

## What this work demonstrates

This project is my infrastructure counterpart to the product work in GlassBox:

- production topology design;
- Linux and container operations;
- reverse-proxy and TLS boundaries;
- private administration design;
- deployment and release contracts;
- least-privilege thinking;
- backup classification and deterministic recovery;
- proportional observability;
- disaster-recovery planning without pretending untested recovery is proven.

The private infrastructure repository contains the executable contracts, operational documentation, and production-specific details. This public case study intentionally leaves out credentials, addresses, secret paths, host identities, and deployable production configuration.

---

[← Back to profile](../README.md)
