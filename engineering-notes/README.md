# Engineering notes

Short public notes about engineering decisions behind my projects.

These are intentionally narrower than project case studies. Each note starts from a concrete implementation or qualification problem and extracts the reusable engineering lesson.

## Notes

### [Durable intent is not runtime state](glassport-durable-intent-vs-runtime-state.md)

What a native terminal workspace should persist — and why PTYs, PIDs, SSH authentication state and live processes should be reconstructed rather than serialized.

**Topics:** Swift · AppKit · macOS · PTY · OpenSSH · persistence · state modeling

### [Unknown is a valid engineering state](gar-unknown-outcomes-and-reconciliation.md)

Why local cancellation is not proof of remote termination, why agent runtimes need reconciliation, and why uncertain execution must not trigger blind inference/tool replay.

**Topics:** Go · AI agents · agent runtime · OpenCode · OpenShell · distributed state · recovery

### [A tutor proposal is not mastery](ai-learning-evidence-before-mastery.md)

Why an AI tutor evaluation should remain evidence until a separate product contract authorizes learner-state changes.

**Topics:** AI evaluation · full-stack · PostgreSQL · tutor architecture · learning systems

## Related work

- [GlassBox](https://github.com/Charles-drZ/glassbox-showcase)
- [Glassoft Agent Runtime](https://github.com/Charles-drZ/glassoft-agent-runtime-showcase)
- [GlassPort](https://github.com/Charles-drZ/glassport-showcase)
- [NodeMedic](https://github.com/Charles-drZ/nodemedic-showcase)
- [Developer profile](https://github.com/Charles-drZ)
