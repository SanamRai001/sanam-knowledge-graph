# Idea Inbox

Ideas stay cheap until evidence says they deserve serious investment.

## Natural-language coding workflow orchestrator

**Observation:** Long AI coding sessions require repeated manual supervision: continue prompts, timeout checks, phase tracking, and recovery.

**Idea:** A supervisor that understands a project plan and watches agent execution, deciding whether to continue, retry, stop, or escalate.

**Smallest experiment:** Model one coding session as a state machine and simulate completion, timeout, and failure events.

**Status:** explore

---

## Personal knowledge graph

**Observation:** Normal note systems collect information but do not clearly represent what a person understands, their evidence, gaps, questions, or changing beliefs.

**Idea:** A Git-based knowledge graph where understanding, curiosity, projects, evidence, and reflection evolve together.

**Smallest experiment:** This repository.

**Status:** active

---

## Event-sourced agent memory

**Observation:** Mutable agent memory can become noisy and difficult to audit.

**Idea:** Represent agent experience as immutable events and derive working state from them.

**Smallest experiment:** Toy event log plus deterministic state reconstruction.

**Status:** curiosity
