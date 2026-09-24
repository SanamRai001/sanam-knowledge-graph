# Project State

## Objective
Maintain a reusable public knowledge-graph framework on `main` and Sanam's evolving personal knowledge graph on `sanam`.

## Branch model
- `main` — generic reusable skeleton and shared framework only.
- `sanam` — personal knowledge, learning map, ideas, questions, projects, principles, and reflections.

## Completed phase
Open-source foundation complete.

### Main now includes
- reusable Markdown knowledge-graph skeleton
- polished public README
- MIT License
- contribution guide
- code of conduct
- getting-started guide
- privacy and safety guidance
- pull request template
- framework issue templates
- repository .gitignore

### Sanam branch
- contains all finalized framework files from `main`
- preserves Sanam-specific knowledge content separately
- is now the working branch for ongoing personal knowledge updates

## Verification
- `main/knowledge/KNOWLEDGE_MAP.md` remains generic.
- `sanam/knowledge/KNOWLEDGE_MAP.md` contains the personal knowledge map.
- MIT License exists on `main` and was synced into `sanam`.
- PR #1 completed the open-source foundation on `main`.
- PR #2 synced that foundation into `sanam` without replacing personal content.

## Decisions
- Never add Sanam-specific knowledge to `main`.
- Personal knowledge updates target `sanam`.
- Shared framework improvements should be developed separately and merged into `main`, then synced into `sanam`.
- Use evidence-based knowledge levels rather than binary "know / don't know".
- Plain Markdown + Git must remain a first-class way to use the project.
- Keep personal branch content non-sensitive because the repository is public.

## Risks
- This repository and the `sanam` branch are public.
- Never add secrets, credentials, confidential client/employer information, or sensitive personal data.
- The temporary setup branch `chore/open-source-foundation` is now merged and can be deleted later with explicit approval.

## Next phase
Begin ongoing personal knowledge capture on `sanam`: expand, correct, and deepen the knowledge map based on actual evidence and new learning.
