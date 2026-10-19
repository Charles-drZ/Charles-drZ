# Unknown is a valid engineering state

A local cancellation is not proof that a remote or sandboxed execution stopped.

That sounds obvious, but agent runtimes can easily erase this distinction if their state machine is built around optimistic terminal semantics.

GAR — Glassoft Agent Runtime — treats **unknown outcome** as a first-class state.

## The failure mode

In the current GAR qualification line, a managed OpenCode execution runs inside a bounded OpenShell sandbox while GAR owns durable lifecycle state.

A bounded live qualification exposed this sequence:

```text
GAR starts managed execution
        ↓
OpenCode sandbox process exists
        ↓
local operator timeout / abort
        ↓
local request stops
        ↓
remote process state is still not proven
```

The unsafe interpretation would be:

> "The abort returned, therefore the execution was aborted."

GAR does not make that claim.

## Local intent vs verified remote outcome

The runtime records separate facts:

- the operator requested abort;
- the local dispatch stopped;
- managed execution had previously entered running state;
- no trustworthy remote completion/termination evidence was available.

The correct resulting state is therefore closer to:

```text
abort_intent = true
remote_outcome = unknown
reconciliation_required = true
```

That is less convenient than a green terminal message, but it is more truthful.

## Why blind retry is dangerous

If a model/backend call may already have produced side effects, an automatic retry can duplicate work.

Examples include:

- creating a second commit;
- pushing twice;
- opening duplicate PRs;
- repeating a tool action;
- paying for or replaying an inference;
- producing two conflicting durable records.

GAR therefore prefers reconciliation over replay when execution certainty is missing.

## Final-response recovery has the same problem

A related issue appears when the managed backend finishes but the GAR-facing final answer is missing or incomplete.

The current GAR-036 branch uses:

1. JSONL-first extraction;
2. bounded same-sandbox recovery only when the actual run provides a unique OpenCode session identity;
3. validation of provider/model/session/final assistant state;
4. text-only extraction with reasoning/tool output excluded;
5. byte/safety bounds and SHA-256 integrity;
6. durable response staging;
7. no inference replay on uncertainty.

If GAR cannot bind the recovered response to the specific run, it fails closed.

It does **not** select "the newest session" and hope.

## The wider lesson

Distributed systems, CI/CD systems and AI agents all share a dangerous category of failure:

> The caller stopped observing before the callee's outcome became provable.

A robust system needs more than success/failure.

Sometimes the only accurate answer is:

**unknown — reconcile before continuing.**

That state is not a defect in the model. It is part of the model.

---

[GAR public engineering case study →](https://github.com/Charles-drZ/glassoft-agent-runtime-showcase)  
[Developer profile →](https://github.com/Charles-drZ)
