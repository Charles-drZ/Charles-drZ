# Durable intent is not runtime state

One of the most important design decisions in GlassPort is also one of the least visually obvious:

> **A workspace layout can survive relaunch. A live terminal process cannot.**

GlassPort is a native macOS developer workspace built around Local Shell and SSH Ports, tabs, terminal Sessions and an optional right-side companion pane.

The temptation in a terminal-style product is to persist whatever the UI currently shows and treat that as application state. That breaks down quickly once the UI owns real PTYs and system OpenSSH processes.

## The boundary

GlassPort separates two kinds of state.

### Durable intent

This describes what the user expects to come back after relaunch:

- Workspace identity;
- tab order;
- active tab;
- primary and companion pane structure;
- Local vs SSH Port identity;
- Local Shell launch directory.

### Ephemeral runtime state

This only exists while the processes exist:

- Session IDs;
- PTYs;
- PIDs;
- terminal scrollback;
- SSH authentication state;
- remote working directory;
- process liveness.

Persisting the first group is useful.

Persisting the second group would create a lie.

## Relaunch means reconstruction

When GlassPort starts again, it reads the durable layout blueprint and creates **fresh runtime Sessions**.

A restored SSH tab is not represented as an old SSH process that somehow survived application termination. It is a new OpenSSH process launched from the saved Port intent.

A restored Local Shell starts from the saved launch directory, but GlassPort does not claim to know the shell's previous live working directory after arbitrary user `cd` commands.

If an SSH alias disappeared from the user's config, the stale pane can be discarded safely rather than corrupting the Workspace.

## Why this matters

This split makes several behaviors easier to reason about:

- process teardown can remain strict;
- persistence does not depend on serializing implementation objects;
- schema migration stays focused on product intent;
- restart behavior is testable;
- stale external configuration fails safely;
- the UI never pretends that a dead process is alive.

It also creates a cleaner product contract:

```text
saved layout
    ↓
validated intent
    ↓
fresh Session
    ↓
fresh PTY / system OpenSSH process
```

## The wider lesson

This is not only a terminal-app problem.

Many applications accidentally persist **runtime accidents** instead of **user intent**.

The more external resources a product owns — processes, sockets, devices, sessions, model calls, jobs — the more useful it becomes to ask:

> What should survive, and what should be reconstructed?

GlassPort's current answer is deliberately conservative: **persist the workspace the user designed; rebuild the machinery that executes it.**

---

[GlassPort public engineering case study →](https://github.com/Charles-drZ/glassport-showcase)  
[Developer profile →](https://github.com/Charles-drZ)
