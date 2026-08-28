# ADR 0002: Establish Repository Structure

## Status

Accepted

## Context

eRecall is expected to include a frontend, backend, shared contracts, documentation, tests, and future infrastructure. Stage 1A Repository Foundation should establish ownership boundaries without generating application scaffolding or empty directories for appearance.

## Decision

The repository will use top-level areas for `frontend/`, `backend/`, `shared/`, `tests/`, `infrastructure/`, `docs/`, and `.github/`.

Each future runtime area currently contains documentation only. Application code, dependency manifests, Docker assets, and service configuration are deferred until their implementation stage.

## Consequences

- Contributors can understand where future work belongs.
- The project avoids premature framework scaffolding.
- Future stages can add tooling inside the appropriate ownership boundary.
