# Development Workflow

This document records the initial engineering standards for eRecall. Tooling should remain purposeful and should be introduced only when it supports an active workflow.

## Local Development

Stage 1A Repository Foundation has no runnable application. Future setup instructions should be added when the frontend, backend, or supporting services are introduced.

## Formatting and Linting

Formatting and linting tools should be added with the code they validate. Expected future direction:

- TypeScript formatting and linting for the frontend.
- Python formatting, linting, and type checking for the backend.
- Markdown and documentation checks when documentation volume justifies automation.

## Testing

Tests should scale with risk:

- Unit tests for domain logic and provider abstractions.
- Contract tests for shared interfaces.
- Integration tests for persistence, retrieval, and API behavior.
- End-to-end tests for critical user workflows once a client exists.
- Regression tests for memory extraction, retrieval, and maintenance behavior.

## Configuration and Secrets

- Use environment variables for configuration.
- Keep `.env` files local and untracked.
- Provide safe examples only when an implementation needs them.
- Never commit real credentials, tokens, private keys, exported user data, or production configuration.

## Dependencies

Dependencies should be added deliberately:

- Prefer standard library and framework capabilities before adding packages.
- Record architectural implications in ADRs when a dependency constrains design.
- Avoid introducing services or libraries before the stage that needs them.
- Consider security, maintainability, portability, and cost.

## Documentation

Documentation should stay close to decisions and workflows:

- README for project overview.
- `docs/architecture.md` for system shape and boundaries.
- `docs/roadmap.md` for engineering phases.
- ADRs for decisions with long-term consequences.
- Contribution and security files for open-source participation.

## Pull Request Expectations

Pull requests should be small, reviewable, and clear about validation. They should avoid unrelated refactors and should update documentation when behavior, architecture, or contributor workflows change.
