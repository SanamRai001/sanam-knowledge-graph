# Connections

## Git history ↔ Event sourcing ↔ AI memory

**Git history:** preserves a sequence of changes instead of only an unexplained final state.

**Event sourcing:** reconstructs current state from historical events.

**AI memory:** long-running agents need continuity across actions.

**Question:** Could an agent's state be reconstructed from an immutable event stream instead of relying on one mutable memory blob?

**Experiment:** Build a tiny agent whose state is rebuilt entirely from append-only events.

---

## Feedback loops ↔ Observability ↔ Agent self-correction

Biological and control systems regulate behavior through feedback. Production software observes signals and reacts to failures. Agents also need reliable signals for deciding when to retry, re-plan, or ask for help.

**Question:** Can explicit feedback signals make agent self-correction more dependable than vague self-reflection?

---

## Workflow engines ↔ Coding agents

Long AI-assisted coding sessions repeatedly require a human to notice completion, timeouts, failed phases, and when to continue.

Workflow engines already model states, retries, conditions, resumability, and escalation.

**Question:** Could a natural-language orchestration layer supervise coding agents and decide when to continue, retry, stop, or request human input?
