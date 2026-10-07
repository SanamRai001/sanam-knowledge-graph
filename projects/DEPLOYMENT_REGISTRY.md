# GitHub Deployment Registry

_Last audited: 2026-10-07_

This file is the durable deployment map for repositories owned by `SanamRai001`.

The goal is **not** to deploy every repository. Deploy only projects that gain portfolio, research, product, or demo value from having a live URL. Coursework, forks, archives, concept-only repositories, empty repositories, and private/client work should stay on GitHub unless there is a specific reason to host them.

## Hosting rules

- Prefer **Cloudflare Pages** for static React/Vite/HTML projects. Static asset requests are free and unlimited; Pages Functions consume Workers quota.
- **Vercel Hobby** is useful for personal/non-commercial demos and Next.js, but its Hobby terms are personal/non-commercial and usage limits can block deployments.
- Use **Render Free Web Service** for Node/Express demo APIs when cold starts are acceptable. Free services sleep after 15 minutes, have an ephemeral filesystem, and must not store durable SQLite/uploads locally.
- Use **MongoDB Atlas M0** for small MongoDB demos. The M0 tier is free and does not expire, within its limits.
- Use **Supabase Free** for small PostgreSQL-backed demos when appropriate. The account currently gets two free projects; free-plan limits and pausing behavior must be considered.
- Use **Firestore free quota** only for projects already designed around Firebase/Firestore.
- Do not force a project onto a free platform if doing so changes its architecture or makes its reliability claims dishonest.

Official references checked on 2026-10-07:
- Render free: https://render.com/docs/free
- Render web services: https://render.com/docs/web-services
- Cloudflare Pages pricing: https://developers.cloudflare.com/pages/functions/pricing/
- Vercel pricing: https://vercel.com/pricing
- Vercel Hobby terms: https://vercel.com/legal/terms
- Supabase billing/free plan: https://supabase.com/docs/guides/platform/billing-on-supabase
- MongoDB Atlas free cluster: https://www.mongodb.com/docs/atlas/tutorial/deploy-free-tier-cluster/
- Firestore pricing/free quota: https://firebase.google.com/docs/firestore/pricing

## Priority deployment queue

| Priority | Project | Current readiness | Recommended free/demo topology | Suggested domain | Decision |
|---|---|---|---|---|---|
| P0 | Eonborne | Strong static/browser build with CI and deterministic tests; active development continues | Cloudflare Pages | `eonborne.run.place` | **Deploy now** as an evolving playable research demo |
| P0 | RepoScout | Main has production-oriented search/contribution UX and green CI; docs explicitly say deployment is next | Web: Cloudflare Pages or Vercel; API: Render Free; DB: Supabase Free PostgreSQL | `reposcout.run.place` | **Deploy next**, then smoke-test live catalog/ingestion |
| P0 | Business Doorway | Phases 1–9 implemented including auth, public pages, templates, analytics, monetization boundary and hardening | Vercel Hobby for personal demo + Supabase Free PostgreSQL; move off Hobby before commercial use | `businessdoorway.run.place` | **Near deployable**; verify env, migrations, auth/cookies and production seed |
| P0 | Playza | Strong controlled-beta baseline; realtime Socket.IO + local SQLite durability | **Oracle Always Free VM** when account/payment verification is available | `playza.run.place` | **Oracle exception — wait**. Render Free would lose SQLite on restart/spindown |
| P1 | SS Furniture | Full MERN site/admin, static fallback, session auth, optional Cloudinary | Single Render Free Node service serving built frontend + MongoDB Atlas M0 + Cloudinary | `ssfurniture.run.place` | **Near deployable**, provided this is meant to be public and not client-confidential |
| P1 | Usora | Full-stack private couple app with tests/security and Firestore | Frontend/API on Render Free or split frontend on Cloudflare Pages + API on Render; Firestore free quota | `usora.run.place` | **Near deployable**, but privacy review is mandatory before real personal data |
| P1 | Knowledge AI | Technically mature, but relies on PostgreSQL, durable object storage, worker jobs, integrations and LLM provider | Partial demo could use Render + Supabase + R2, but full worker/watch behavior is not a clean zero-cost fit | `knowledgeai.run.place` | **Hold for proper deployment topology** rather than weaken the architecture |
| P1 | Dear Future | Code is heavily verified, but PROJECT_STATE explicitly says no public release yet; real email/staging/restore checks remain | Eventually static/web + persistent PostgreSQL + email provider + reliable worker | `dearfuture.run.place` | **Do not deploy publicly yet**; finish M1C-D2 operational verification first |
| P2 | StateScout | Active research implementation, Phase 10; tool/research artifact rather than consumer web product | GitHub Releases/npm later; optionally Cloudflare Pages for docs/benchmark visualizer | `statescout.run.place` | **Do not force an app deployment**; publish the tool when experiment gates mature |
| P2 | Reality Archive | Reconstruction platform still gated on real capture + real COLMAP/GPU proof | Static docs/viewer can be Pages; reconstruction workers need GPU compute later | `realityarchive.run.place` | **Hold platform deployment**; MaybeBoudha already proves the browser-viewer direction |
| P2 | ScanSketch | Research project; default-branch README still says no reconstruction engine | Static research page later | `scansketch.run.place` | **Not deployment-ready** on current default branch |
| P2 | Sajilo Business | UX prototype with mock data; backend intentionally deferred | Cloudflare Pages only if a UX prototype demo is useful | `sajilo.run.place` | **Optional prototype deploy**, not a product launch |
| P2 | Mascot Login | React Native/Expo prototype; real 3D path requires native dev build | Expo/EAS or downloadable dev build, not ordinary web hosting | no web domain needed yet | **Not a web-deployment target** |

## Already live / keep live

| Project | Current live state from repository | Action |
|---|---|---|
| Portofolio | Live at `https://sanam-rai.com.np` | Keep as the primary portfolio. Finish current G4D/share-preview work; do not create a second domain |
| MaybeBoudha | Live at `https://maybeboudha.run.place/` on GitHub Pages | Keep live; it is already a strong public digital-heritage prototype |
| KrishiBazar | Frontend on Vercel and backend on Render according to README | Keep live if endpoints still healthy; custom domain is optional rather than necessary |
| YakTalk-chatapp | Full-stack Render deployment documented in README | Keep as a legacy live demo if still functioning |
| PaSec | README points to `pasec.ssuroj.com.np` | Treat as already hosted / collaborator project; no new deployment needed |

## Repository-by-repository inventory

Legend:
- **LIVE** — already has a documented live deployment.
- **NOW** — worthwhile and sufficiently close to deploy.
- **NEAR** — small deployment-readiness work remains.
- **HOLD** — active/valuable project, but deployment would be premature or misleading.
- **ARCHIVE** — learning/history; do not spend hosting effort.
- **FORK** — upstream/fork/reference repository, not a separate product deployment.
- **EMPTY** — no meaningful deployable application in the current repository.

| Repository | Classification | Deployment note |
|---|---|---|
| `16_legs` | ARCHIVE | Legacy web-project archive; preserve as development history |
| `A-site` | EMPTY | Empty repository |
| `activepieces` | FORK | Upstream automation platform fork; self-host only when actively developing the fork |
| `agentbridge` | HOLD | README explicitly says PARKED / VALIDATION STAGE — DO NOT BUILD YET |
| `AlbionOnline_api` | ARCHIVE | Small API learning experiment |
| `API_crud` | ARCHIVE | Basic Express/MySQL CRUD learning project |
| `blackbird` | PRIVATE/CLIENT | Public-facing Black Bird site code, but treat as client/work deployment, not personal portfolio hosting |
| `BlackbirdMain` | EMPTY/PRIVATE | Empty repo |
| `BloodCare` | ARCHIVE | Large earlier full-stack project; README says modernization required before production |
| `business-doorway` | NEAR | High-value product candidate; Vercel + PostgreSQL demo topology |
| `cantorDust` | ARCHIVE | Consulting/company website archive |
| `Clone` | ARCHIVE | Early HTML/CSS recreation exercises |
| `constillation` | ARCHIVE | Private visual experiment |
| `course` | FORK | Hugging Face course repository; do not deploy as personal project |
| `Daily-Dose-of-Motivation` | ARCHIVE | Full-stack learning archive |
| `Dear-future` | HOLD | Operational staging verification is still required before public release |
| `Eonborne` | NOW | Excellent static web demo candidate for Cloudflare Pages |
| `FinanceCantorDust` | ARCHIVE | Accounting-dashboard learning/archive project; production correctness review would be required |
| `FullStackOpen_Sanam` | ARCHIVE | Coursework |
| `github-badge-test` | ARCHIVE | Badge experiment only |
| `HER` | PRIVATE DEMO | Static portrait viewer is technically deployable to Vercel, but contains personal photographs; do not publish broadly without explicit consent |
| `Kept` | HOLD | Product-definition / MVP development; not yet implementation-ready enough for public hosting |
| `knowledge-ai` | HOLD | Mature architecture, but full zero-cost topology is not reliable because of worker/storage/LLM requirements |
| `KrishiBazar` | LIVE | Already Vercel + Render + MongoDB Atlas |
| `mascot_login` | HOLD | Native React Native/Filament prototype; use Expo/EAS rather than web deployment |
| `MaybeBoudha` | LIVE | Already GitHub Pages + custom domain |
| `My-notebook` | EMPTY | Empty repository |
| `OurWorld` | HOLD | AI Studio experiment; deploy only if it becomes a distinct product |
| `page-agent` | FORK | Alibaba Page Agent fork/reference; not a personal app deployment |
| `pasec` | LIVE/COLLAB | Existing website listed in README |
| `passive-emergency-inference` | HOLD | Concept/research proposal only |
| `PhoneBook-Application-` | ARCHIVE | Python CLI learning project; no hosting needed |
| `playza` | NEAR / ORACLE | Controlled-beta web game; Oracle VM is the correct current target because SQLite + realtime state need durable disk/process |
| `pocket-tts` | FORK/RESEARCH | Upstream Pocket TTS fork with local research work; package/research artifact rather than ordinary website |
| `Portofolio` | LIVE | Primary portfolio at sanam-rai.com.np |
| `rag-from-scratch` | ARCHIVE/LEARNING | Local RAG learning lab; no need to host |
| `RAG-system` | EMPTY | Empty repository |
| `Reality-Archive` | HOLD | Real reconstruction proof gate still open |
| `reposcout` | NOW | Strong public product/demo deployment candidate |
| `sajilo-business` | HOLD/PROTOTYPE | Mock-data UX prototype; optional static demo only |
| `Sample-Portofolio` | ARCHIVE | Superseded by current Portfolio |
| `sanam-knowledge-graph` | DOCS | Git repository is the product; GitHub is the correct host |
| `SanamRai001` | DOCS | GitHub profile README repository |
| `ScanSketch` | HOLD | Research foundation on default branch; not yet deployable product |
| `Skribble` | ARCHIVE/UNFINISHED | Realtime learning foundation; unfinished |
| `SS-furniture` | NEAR | Technically close to deployment; confirm ownership/public intent first |
| `StarySpace` | ARCHIVE | Single-file visual experiment |
| `StateScout` | HOLD/RESEARCH | Active research/tool project; publication should be package/release/docs oriented |
| `Task-Manager` | ARCHIVE | Basic Express/MySQL CRUD learning project |
| `Usora` | NEAR | Technically deployable private app; strong privacy/data-handling gate |
| `YakTalk-chatapp` | LIVE | Existing Render deployment |

## Recommended deployment order

1. **Eonborne** — easiest high-value win. Static deployment, no database, no backend operational burden.
2. **RepoScout** — strongest serious full-stack public product candidate. Deploy web/API/DB separately and smoke-test live ingestion/catalog behavior.
3. **Business Doorway** — deploy as a personal demo after env/migration/auth checks. Keep Vercel Hobby's non-commercial restriction in mind.
4. **SS Furniture** — only after confirming this is yours to publish. Use MongoDB Atlas for durable data; never rely on Render's local filesystem for uploads.
5. **Usora** — deploy only with demo/synthetic relationship data first. Treat private user data as sensitive.
6. **Playza** — deploy when Oracle VM access is available. Do not move the current SQLite architecture to ephemeral free hosting merely to get a URL.
7. **Dear Future** — deploy only after real staging email, webhook, backup/restore, worker and operational verification.
8. **Knowledge AI** — design a deliberately limited public demo or obtain a proper always-on topology; do not claim Watch/worker reliability on a sleeping free service.

## Domain plan

Use simple project-native names. Availability is not asserted here; these are preferred targets if your free-domain source can provide them.

- `eonborne.run.place`
- `reposcout.run.place`
- `businessdoorway.run.place`
- `playza.run.place`
- `ssfurniture.run.place`
- `usora.run.place`
- reserve `dearfuture.run.place`
- reserve `knowledgeai.run.place`
- reserve `statescout.run.place`
- reserve `realityarchive.run.place`
- reserve `scansketch.run.place`

Existing domains should stay unchanged:
- `sanam-rai.com.np`
- `maybeboudha.run.place`

If a new free root domain is inconvenient, use subdomains under an owned domain instead, e.g. `reposcout.sanam-rai.com.np`. One stable domain is better than repeatedly moving projects between free-domain providers.

## Deployment acceptance checklist

Before marking any project LIVE:

- default branch is the intended release source;
- README and PROJECT_STATE agree with reality;
- build/typecheck/tests relevant to that project pass;
- production secrets are not committed;
- environment variables are documented;
- health/readiness routes exist for dynamic services;
- database migrations are reproducible;
- CORS/cookie/session settings match the real domain topology;
- SPA rewrites/deep links are tested;
- uploaded files are stored outside ephemeral local disk;
- demo data contains no real private/client information;
- custom domain HTTPS works;
- one desktop and one mobile smoke test passes;
- the live URL is added back to the repository README and this registry.

## Next maintenance rule

Update this file whenever:
- a project becomes live;
- a deployment topology changes;
- a project crosses from HOLD → NEAR → NOW;
- a free provider changes a material limitation;
- a new serious repository is created.

Do **not** update it for every tiny branch or experiment. The registry should remain a decision document, not a commit diary.
