# Getting Started

This guide shows the recommended way to turn the framework into your own living knowledge graph.

## 1. Fork the repository

Fork the project into your own GitHub account.

You can also use it as inspiration and copy the structure elsewhere under the MIT License.

## 2. Keep main generic

Keeping `main` close to the reusable framework makes future framework updates easier to understand and merge.

Create a personal branch:

```bash
git checkout -b personal
```

You can name it `personal`, your name, or anything meaningful to you.

## 3. Start with the knowledge map

Open:

`knowledge/KNOWLEDGE_MAP.md`

Do not try to catalog your entire life in one sitting.

Start with a few areas you already work in.

For each area, record:

- your current level
- what you can actually do
- evidence
- what you still do not understand

## 4. Choose a small current focus

Use:

`learning/CURRENT_FOCUS.md`

A useful default is:

- one primary learning area
- one secondary area
- one exploration area

Everything else belongs in the backlog.

## 5. Capture curiosity without losing focus

When a question appears, put it in:

`curiosity/QUESTIONS.md`

When two ideas seem related, put the connection in:

`curiosity/CONNECTIONS.md`

You do not have to research everything immediately.

## 6. Use projects as evidence

Use:

`projects/PROJECTS.md`

A project is useful evidence when it shows that you have applied a concept, made decisions, handled failures, or learned from trade-offs.

Do not treat every repository you have touched as proof of mastery.

## 7. Run experiments

When you think you understand a difficult concept, use:

`templates/EXPERIMENT.md`

Keep experiments small enough that they test one idea.

## 8. Review your understanding

At the end of a month, copy:

`templates/REVIEW.md`

into:

`reviews/monthly/YYYY-MM.md`

The goal is not productivity scoring. The goal is to notice how your understanding changed.

## 9. Commit meaningful changes

Useful commit examples:

```text
knowledge: deepen understanding of database isolation
learning: move transformers into current focus
curiosity: add questions about distributed consensus
projects: record lessons from production deployment
review: add 2026-09 monthly reflection
```

Git history becomes part of the value: years later, you can see how your thinking evolved.

## 10. Update levels carefully

Do not raise a level because you watched a course.

Raise it when the evidence changes.

For example:

- you can explain it
- you implemented it
- you debugged it
- you compared alternatives
- you understand its failure modes
- you can teach or review it

## Optional: private knowledge

If your graph contains sensitive reflections or private life information, use a private repository or keep that material outside the public graph.

Read [Privacy and Safety](PRIVACY_AND_SAFETY.md) before publishing personal content.
