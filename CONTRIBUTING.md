# Contributing to eRecall

Thank you for taking an interest in eRecall. This project is early, so the best contributions are focused, well-scoped, and aligned with the current engineering phase.

## Current Stage

The project is in Stage 1A — Repository Foundation. Implementation work for the chatbot, backend, frontend, authentication, memory engine, storage integrations, deployment, and production infrastructure is intentionally deferred.

## Contribution Workflow

1. Open or find an issue that describes the change.
2. Discuss the approach for larger or architectural changes before implementation.
3. Create a branch with a clear engineering name.
4. Keep pull requests small enough to review.
5. Include documentation and tests when the change affects behavior, interfaces, or contributor workflows.
6. Ensure no secrets, credentials, private data, or generated build output are committed.

## Pull Requests

Pull requests should include:

- A short description of the change.
- The reason the change is needed.
- Validation performed.
- Any known limitations or follow-up work.

Do not include unrelated refactors, formatting churn, or speculative implementation.

## Commit Style

Use clear conventional commits where practical, such as:

- `docs: clarify architecture boundaries`
- `chore: add repository baseline`
- `test: add memory retrieval contract coverage`

## Development Standards

See [docs/development.md](docs/development.md) for formatting, testing, configuration, documentation, and dependency expectations.

## Architecture Decisions

Meaningful architecture choices should be recorded as Architecture Decision Records under [docs/adr](docs/adr). Use the existing ADR format and keep each record focused on one decision.
