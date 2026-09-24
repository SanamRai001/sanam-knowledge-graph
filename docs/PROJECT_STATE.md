# Project State

## Objective
Maintain a reusable public knowledge-graph framework on `main` and Sanam's evolving personal knowledge graph on `sanam`.

## Branch model
- `main` — generic reusable skeleton and shared framework only.
- `sanam` — personal knowledge, learning map, ideas, questions, projects, principles, and reflections.

## Completed foundation
Open-source foundation complete.

## Active personal phase

### Month 1 learning cycle
**Start:** 2026-09-25  
**End:** 2026-10-24

The first learning cycle is intentionally minimal.

Required outcomes:

1. PostgreSQL foundations + transactions/isolation.
2. Web request lifecycle: DNS → TCP → TLS → HTTP → application → PostgreSQL.
3. Transformers and embeddings at a high-level mental-model level.

PostgreSQL was added on 2026-09-24 by folding it into the existing database outcome rather than adding a fourth topic.

Required outputs:

- one tiny experiment;
- one monthly review on 2026-10-24.

Detailed plan:

`learning/monthly/2026-09-25_to_2026-10-24.md`

## Knowledge correction — 2026-09-24

The knowledge map previously grouped PostgreSQL with databases Sanam could already use independently.

Sanam clarified that PostgreSQL has appeared in projects but is not yet independently understood.

The knowledge map now records PostgreSQL separately at Level 0–1 until hands-on evidence justifies raising it.

## Learning decision
Curiosity must not continually expand the active roadmap.

When a side topic appears:

- capture it in the learning backlog or curiosity questions;
- do not change the active month;
- only investigate it immediately if it blocks understanding of the current topic.

## Date convention
New learning entries should use exact ISO dates:

`YYYY-MM-DD`

Planned dates may be written in roadmap files, but completed learning should only be logged after it actually happens.

## Verification
- `main/knowledge/KNOWLEDGE_MAP.md` remains generic.
- `sanam/knowledge/KNOWLEDGE_MAP.md` contains the personal knowledge map.
- `learning/CURRENT_FOCUS.md` contains only Month 1 essentials.
- PostgreSQL is now part of the Month 1 database outcome.
- PostgreSQL is no longer overstated as an independently known skill.
- The wider learning backlog remains deferred.
- `learning/LEARNING_LOG.md` uses dated, evidence-based entries.

## Decisions
- Never add Sanam-specific knowledge to `main`.
- Personal knowledge updates target `sanam`.
- Shared framework improvements should be merged into `main`, then synced into `sanam`.
- Use evidence-based knowledge levels rather than binary "know / don't know".
- Plain Markdown + Git remains a first-class way to use the project.
- Keep personal branch content non-sensitive because the repository is public.

## Risks
- This repository and the `sanam` branch are public.
- Never add secrets, credentials, confidential client/employer information, or sensitive personal data.
- The temporary setup branch `chore/open-source-foundation` is merged and can be deleted later with explicit approval.

## Next phase
Start the Month 1 PostgreSQL foundation on 2026-09-25 and add dated learning evidence as it actually happens.
