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

---

## Embedded AI product copilot with Page Agent + voice

**Observation:** Many SaaS products still force users to learn navigation, forms, and multi-step workflows even when the product already exposes everything through its UI. Alibaba's Page Agent is an MIT-licensed, JavaScript in-page GUI agent that can control web interfaces through natural language and can use a configurable LLM. This makes it interesting as an embedded product capability rather than only as external browser automation.

**Idea:** Explore Page Agent as a reusable AI interaction layer for products such as MIH DineOS / RMS and future SaaS applications. A user could describe what they want in natural language and the copilot could navigate or operate permitted parts of the existing UI. Add voice as another input/output layer so the same agent can potentially support hands-free workflows.

Possible examples:
- In MIH DineOS: "Open table T-04", "show unpaid bills", "go to today's sales report", or guide a waiter toward the correct workflow.
- In an admin SaaS: fill repetitive forms, navigate settings, find records, and execute allowed multi-step UI tasks.
- Accessibility / hands-free mode: speech-to-text -> agent instruction -> UI action -> optional text-to-speech confirmation.

**Architecture direction:** Treat Page Agent as the UI-control layer, not as the authority layer. Existing backend authentication, tenant isolation, RBAC, validation, and business rules must remain authoritative. Do not give the browser unrestricted credentials or expose private LLM keys. Route model access safely, restrict the agent to explicit capabilities/actions, require confirmation for destructive or financial operations, and audit consequential actions.

**Why this is interesting:** It could turn an existing SaaS UI into a natural-language/voice-operated product without rebuilding every workflow as a separate chatbot tool. Because the project is MIT licensed, it can be studied, adapted, and incorporated into commercial experiments while preserving required license/copyright notices.

**Main risks / questions:**
- How reliable is DOM-driven control as the application's UI evolves?
- Can permissions be constrained strongly enough for multi-tenant production use?
- Which actions should be read-only, immediately executable, or confirmation-gated?
- What information is sent to the configured LLM provider?
- How should voice behave in noisy restaurant environments?
- Would Page Agent remain an embedded dependency, be wrapped behind our own abstraction, or eventually be forked/customized?

**Smallest experiment:** Add Page Agent only to a disposable/local MIH DineOS sandbox and allow a tightly scoped read/navigation task such as "open Bills & Payments" or "show the Sales Report". No order mutation, payment, cancellation, user-management, or production data in the first experiment. If the UI agent is reliable, add browser speech-to-text as a second experiment rather than coupling voice into the first prototype.

**Source:** https://github.com/alibaba/page-agent

**License:** MIT

**Status:** explore
