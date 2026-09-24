# Sanam Knowledge Graph

A reusable, Git-based framework for mapping **what you know, what you're learning, what you're curious about, and what you want to build**.

> **Learn → Understand → Connect → Build → Reflect → Evolve**

## What this is

Most note systems are good at storing information. This project is designed to track **understanding**.

It gives you a simple, version-controlled place to record:

- what you already know
- how deeply you understand it
- evidence from projects and experiments
- what you are learning now
- what you want to learn later
- unanswered questions
- connections between ideas
- projects that prove applied knowledge
- principles you have developed
- how your thinking changes over time

The goal is not to create a perfect résumé. The goal is to build an **honest, evolving map of your mind**.

## Who this is for

This repository may be useful if you:

- learn across many technical or creative subjects
- want to distinguish exposure from real understanding
- want evidence behind skill claims
- have too many things you want to learn
- want to preserve questions instead of losing them
- want to connect ideas across different fields
- want to look back years later and see how your thinking evolved

## Quick start

1. **Fork this repository.**
2. Keep `main` as the reusable framework.
3. Create a personal branch such as `your-name`, `personal`, or `knowledge`.
4. Fill that branch with your real knowledge, questions, projects, and reflections.
5. Update it as your understanding changes.

See [Getting Started](docs/GETTING_STARTED.md) for the recommended workflow.

## Branch model

This repository intentionally separates the framework from personal knowledge.

```text
main
└── reusable skeleton only

your-personal-branch
└── your actual knowledge graph
```

This makes it easier to pull future framework improvements without mixing them with your personal content.

## Knowledge levels

Use levels as a rough self-assessment, backed by evidence whenever possible.

| Level | Meaning |
|---|---|
| 0 | Heard of it |
| 1 | Can explain the basic idea |
| 2 | Can use it with guidance |
| 3 | Can use/build with it independently |
| 4 | Understand trade-offs, limitations, and failure modes |
| 5 | Can design, teach, or review systems using it |

Levels are **not trophies**. They are snapshots that should change when the evidence changes.

## Repository structure

```text
.
├── knowledge/
│   └── KNOWLEDGE_MAP.md
├── learning/
│   ├── CURRENT_FOCUS.md
│   ├── LEARNING_BACKLOG.md
│   └── LEARNING_LOG.md
├── curiosity/
│   ├── QUESTIONS.md
│   └── CONNECTIONS.md
├── ideas/
│   └── IDEA_INBOX.md
├── projects/
│   └── PROJECTS.md
├── principles/
│   └── PRINCIPLES.md
├── reviews/
│   └── monthly/
├── templates/
│   ├── KNOWLEDGE_ENTRY.md
│   ├── EXPERIMENT.md
│   └── REVIEW.md
└── docs/
    └── GETTING_STARTED.md
```

## Core philosophy

- Be honest about what you know.
- Prefer evidence over confidence.
- Track gaps instead of hiding them.
- Exposure is not mastery.
- Build small experiments to test understanding.
- Record connections between different fields.
- Let your knowledge map change when you change your mind.
- Do not turn every interesting idea into a full project.
- Keep current focus small enough to make real progress.
- Treat curiosity as material for creation, not just consumption.

## A simple learning loop

```text
Discover
   ↓
Understand
   ↓
Connect
   ↓
Experiment
   ↓
Build
   ↓
Reflect
   ↓
Update the graph
```

## Privacy

A public knowledge graph should never contain:

- passwords, API keys, tokens, or secrets
- confidential employer/client information
- private conversations
- personal identification documents
- sensitive health, financial, or account information

If a note is too private for the public internet, keep it out of a public branch or use a private fork/repository.

Read [Privacy and Safety](docs/PRIVACY_AND_SAFETY.md) before adding personal content.

## Contributing

Improvements to the reusable framework are welcome.

Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.

Personal knowledge should normally stay in your own fork or personal branch rather than being contributed back to `main`.

## Project status

The initial Markdown framework is intentionally simple. Future improvements may include optional validation, statistics, visualization, and tooling, while keeping plain Markdown and Git useful on their own.

## License

This project is licensed under the [MIT License](LICENSE).

You are free to use, copy, modify, fork, and adapt the framework for your own knowledge graph.
