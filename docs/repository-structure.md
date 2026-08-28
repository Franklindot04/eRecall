# Repository Structure

The repository structure for Stage 1A Repository Foundation is intentionally small. Directories exist only where they clarify future ownership.

## Top-Level Areas

```text
backend/
frontend/
shared/
tests/
infrastructure/
docs/
.github/
```

## Rationale

### `backend/`

Future home for the API and backend services. This area is expected to use Python, FastAPI, and Pydantic when implementation begins.

### `frontend/`

Future home for the client application. This area is expected to use Next.js, TypeScript, and Tailwind CSS when implementation begins.

### `shared/`

Future home for shared contracts, schemas, interface definitions, and documentation that must be understood by more than one runtime.

### `tests/`

Future home for cross-project tests, integration tests, fixtures, and validation assets that do not belong inside a single runtime workspace.

### `infrastructure/`

Future home for deployment, container, observability, and operations assets. Hosting and production infrastructure choices are deferred to a later phase.

### `docs/`

Architecture, development standards, roadmap, and Architecture Decision Records.

### `.github/`

Open-source collaboration templates for issues and pull requests.

## What Is Intentionally Not Present

- No application code.
- No generated scaffold from a frontend or backend framework.
- No container or deployment configuration.
- No dependency manifests.
- No fake credentials or sample secrets.
- No empty directories without documentation.
