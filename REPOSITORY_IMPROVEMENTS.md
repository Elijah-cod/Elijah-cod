# Repository Improvement Plan

This plan is based on inspected source code and current repository documentation. Suggested descriptions fit GitHub's repository-card format; topics are intentionally limited to accurate, searchable terms.

## InsightGraph (`hybrid-rag-engine`)

**Suggested name:** `insightgraph-rag` (optional)

**Description:** Hybrid RAG application combining pgvector semantic search, Neo4j graph traversal, Gemini extraction, and an interactive knowledge map.

**Topics:** `rag`, `knowledge-graph`, `vector-search`, `neo4j`, `pgvector`, `nextjs`, `typescript`, `gemini`

README improvements:

- Replace the local absolute migration link with a repository-relative link.
- Add a system architecture diagram and a retrieval sequence diagram.
- Add screenshots of ingestion, chat evidence, source library, and the knowledge map.
- Document supported inputs and the exact behavior of mock mode.
- Add a limitations/evaluation section; there are currently no automated retrieval-quality tests.
- Remove the task-specific security note once credentials have been rotated.

Badges: CI status after adding a workflow for lint, typecheck, and build; license after selecting one. Do not add an unverified coverage badge.

## Anatomy UI (`Anatomy-UI`)

**Suggested name:** keep `Anatomy-UI`

**Description:** Headless, accessible React primitives with keyboard interactions, focus management, Storybook documentation, and automated interaction tests.

**Topics:** `react`, `typescript`, `headless-ui`, `accessibility`, `storybook`, `vitest`, `component-library`, `aria`

README improvements:

- Add a concise status banner stating which primitives are production-ready.
- Resolve the roadmap inconsistency: Modal, Accordion, and Tooltip are listed as both current and future work.
- Add a hosted Storybook link and a small animated interaction example.
- Document the public API, controlled/uncontrolled behavior, browser support, and versioning policy.
- Add package installation instructions only after publishing a package.

Badges: test workflow, Storybook deployment, license, and package version only when those systems are live.

## SaaS Management Tool (`SaaS-Management-Tool`)

**Suggested name:** `project-operations-platform`

**Description:** Full-stack project operations platform with a Next.js client, Express API, PostgreSQL, role-based access control, and tested task workflows.

**Topics:** `nextjs`, `typescript`, `express`, `postgresql`, `prisma`, `redux-toolkit`, `rbac`, `full-stack`

README improvements:

- Replace machine-specific environment-file links with relative paths.
- Add screenshots of the board, task drawer, search, and responsive layout.
- Add an architecture diagram covering auth and client/API boundaries.
- Document roles and permissions in a table.
- Correct the production checklist: request validation and server integration tests are listed as both implemented and still recommended.
- Add CI for client lint/typecheck/build and server typecheck/test/build.
- Avoid publishing long-lived sample passwords outside an explicitly local seed context.

Badges: CI, license, frontend deployment, and API health if a stable backend deployment exists.

## LiftLog (`liftlog`)

**Suggested name:** keep `liftlog`

**Description:** Mobile-first workout logger with resilient autosave, draft recovery, Supabase persistence, row-level security, and mock/live runtime modes.

**Topics:** `nextjs`, `typescript`, `supabase`, `postgresql`, `zustand`, `workout-tracker`, `offline-first`, `vitest`

README improvements:

- Add a short demo GIF of preview → logging → recovery → completion.
- Add a state diagram for the workout lifecycle and autosave states.
- Document the schema and RLS ownership model.
- Expand automated tests around draft recovery, sync failure, and completion guards.
- Add accessibility testing for form controls, timers, and keyboard workflows.

Badges: CI and license after adding a workflow and license; avoid claiming offline support beyond the implemented local draft recovery.

## Anime Tracker (`anime-tracker`)

**Suggested name:** keep `anime-tracker`

**Description:** Full-stack anime tracker using Next.js, FastAPI, PostgreSQL, AniList GraphQL, and Jikan imports with user-scoped libraries.

**Topics:** `fastapi`, `python`, `nextjs`, `postgresql`, `sqlalchemy`, `graphql`, `anilist`, `full-stack`

README improvements:

- Replace absolute local links throughout with repository-relative links.
- Add screenshots for dashboard, library, calendar, and profile.
- Explain the current account/session model precisely; do not imply production authentication if it is local account selection.
- Document API endpoints and error behavior.
- Add backend API tests and frontend interaction tests.
- Add a data-flow diagram for AniList/Jikan → FastAPI → PostgreSQL → Next.js.

Badges: backend tests, frontend build, license, and deployments once both services are stable.

## CrypDash (`Real-Time-Financial-Dashboard`)

**Suggested name:** `crypdash`

**Description:** Cryptocurrency dashboard with CoinGecko market data, Firebase-authenticated watchlists, and a no-configuration local preview mode.

**Topics:** `cryptocurrency`, `market-data`, `javascript`, `coingecko-api`, `firebase`, `firestore`, `data-visualization`, `dashboard`

README improvements:

- Lead with the product and current behavior, not “Cloudflare Pages + Firebase Ready” or “What changed.”
- Add a prominent screenshot and live demo link.
- Clearly label current prices as live and historical chart data as mocked.
- Document API rate-limit and fallback behavior.
- Add tests around market-data normalization, watchlist persistence, and mode selection.
- Add a disclaimer that it is a software demonstration, not investment advice.

Badges: deployment and license. Add CI only after a real test/lint workflow exists.

## Opaque Vault (`Opaque`)

**Suggested name:** `opaque-vault`

**Description:** Encrypted web vault exploring client-side key derivation, OTP authentication, session handoff, and server-side ciphertext storage.

**Topics:** `nextjs`, `typescript`, `cryptography`, `client-side-encryption`, `encrypted-vault`, `web-crypto`, `security`, `turso`

Avoid a `zero-knowledge` topic until the authentication verifier flow and complete threat model have received specialist review. The code supports the narrower, defensible claim that vault item encryption and decryption occur in the browser.

README improvements:

- Move the nested `web/README.md` to a purposeful repository-level README.
- Remove the default Next.js template sections.
- Document the cryptographic construction, algorithms, parameters, key lifecycle, and trust boundaries.
- Add a threat model and an explicit “not security audited” warning.
- Add tests for serialization, key derivation, session expiry, tampering, and auth failure paths.
- Add a sequence diagram for enrollment, unlock, item encryption, and retrieval.

Badges: existing CI workflow and license. Do not use a security/audit badge without an independent audit.

## Reflection Hub (`reflection-hub`)

**Suggested name:** keep `reflection-hub`

**Description:** Personal reflection workspace built with Next.js, Clerk, Prisma, Arcjet, rich-text editing, and chart-based activity views.

**Topics:** `nextjs`, `react`, `prisma`, `clerk`, `journaling`, `rich-text-editor`, `recharts`, `javascript`

README improvements:

- Replace generic template claims with exact implemented features and environment variables.
- Remove speculative text such as “if applicable,” “optional,” and “You may want to.”
- Document Clerk, Prisma, and Arcjet configuration accurately.
- Add tests and CI before presenting this as a leading engineering project.
- Keep it public, but do not pin it ahead of the stronger repositories.

## Python API Exercises

`lateshow-elijah-mathai` and `Superheroes` show Flask/SQLAlchemy fundamentals but still read as coursework. Improve their clone URLs, dependency locking, API examples, validation documentation, tests, and licenses. Keep one as representative Python backend work if needed; archive the other once `anime-tracker` provides stronger Python evidence.
