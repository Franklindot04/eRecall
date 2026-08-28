# ADR 0004: Document Technology Direction Without Stage 0 Integration

## Status

Accepted

## Context

The project has an intended technology direction: Next.js, TypeScript, Tailwind CSS, Python, FastAPI, Pydantic, PostgreSQL, Qdrant, Redis, Docker, GitHub Actions, OpenTelemetry, Prometheus, and Grafana.

Stage 0 is not the correct phase to install frameworks, configure infrastructure, or introduce dependencies that do not yet validate working code.

## Decision

Stage 0 will document the technology direction but will not install, configure, or integrate those technologies.

Tooling and dependencies will be introduced in later phases when they support concrete implementation, validation, or operations needs.

## Consequences

- The repository communicates direction without pretending implementation exists.
- Future stages can revisit choices with better requirements.
- The initial repository remains lightweight and easier to review.
