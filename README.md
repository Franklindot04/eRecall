# eRecall

eRecall (Enhanced Recall) is a memory-first AI assistant project focused on persistent, user-controlled conversational memory.

The goal is to build a serious open-source system where conversations can benefit from remembered context across sessions without giving up clear user control, privacy-conscious storage, and maintainable engineering boundaries.

## Problem

Most chat assistants are optimized around the current prompt and short-term context. Useful personal context, preferences, corrections, and long-running goals are often lost, repeated, or hidden inside provider-specific behavior.

eRecall explores an explicit memory architecture where stored information is modeled, retrieved, maintained, reviewed, and deleted through project-owned interfaces.

## Status

Stage 1A — Repository Foundation establishes the repository foundation and engineering baseline. The project is not yet an implemented chatbot, memory engine, backend API, frontend application, or deployed service.

This stage establishes documentation, contribution practices, architecture direction, and decision records for future work.

## Intended Architecture

At a high level, eRecall is expected to evolve around these layers:

```text
Client / Frontend
        |
API / Application Layer
        |
Core Services
        |
Memory System
        |
Persistence / Retrieval Infrastructure
        |
External Providers
```

Major planned areas include:

- Client experience for conversation, memory review, and user controls.
- API and application layer for request handling, validation, authentication boundaries, and orchestration.
- Core services for conversation workflows, memory extraction, retrieval, maintenance, and evaluation.
- Memory system for structured memory records, lifecycle state, provenance, deletion, and semantic retrieval.
- Persistence and retrieval infrastructure for structured storage, vector search, caching, and background work when justified.
- Provider abstractions for chat models, embeddings, and other external services.

See [Architecture](docs/architecture.md) for the intended boundaries and responsibilities.

## Memory Concepts

eRecall treats memory as an explicit product and architecture concern. Future implementation should distinguish between:

- Conversation history: raw or summarized interaction records.
- Extracted memories: structured facts, preferences, events, or user-provided context derived from conversations.
- Retrieved context: relevant memories selected for a specific interaction.
- Maintained memories: records merged, updated, expired, archived, or deleted over time.
- User-controlled memory: inspectable and removable information that remains under user control.

The project should avoid hidden or provider-locked memory behavior where practical.

## Technology Direction

The current intended direction is:

- Frontend: Next.js, TypeScript, Tailwind CSS.
- Backend: Python, FastAPI, Pydantic.
- Structured storage: PostgreSQL.
- Vector storage: Qdrant.
- Caching and asynchronous infrastructure: Redis and background processing when the architecture justifies them.
- Delivery: Docker and GitHub Actions.
- Observability: OpenTelemetry, Prometheus, and Grafana.
- AI providers: provider abstractions for chat, embeddings, extraction, and evaluation workflows.

These are directional choices for future stages. Stage 1A — Repository Foundation does not install, configure, or integrate them.

## Repository Layout

```text
.
|-- backend/                 Future API and backend service workspace
|-- frontend/                Future client application workspace
|-- shared/                  Future shared contracts and interface definitions
|-- tests/                   Future cross-project and integration test workspace
|-- infrastructure/          Future deployment and operations assets
|-- docs/                    Architecture, development, roadmap, and ADRs
|-- .github/                 Issue and pull request templates
|-- CONTRIBUTING.md          Contribution workflow
|-- SECURITY.md              Security reporting and baseline expectations
|-- CODE_OF_CONDUCT.md       Community standards
|-- LICENSE                  Project license
```

See [Repository Structure](docs/repository-structure.md) for rationale.

## Development

The project is intentionally light on tooling until implementation begins. Future tooling should be added when it supports a real workflow: formatting, linting, tests, type checking, documentation validation, or release automation.

For current contribution expectations, see [Development Workflow](docs/development.md) and [Contributing](CONTRIBUTING.md).

## Roadmap

The roadmap is organized by engineering phases rather than artificial deadlines:

1. Stage 1A — Repository Foundation.
2. Stage 1B — Core Application Foundation.
3. Conversation persistence.
4. Memory extraction.
5. Memory storage.
6. Memory retrieval.
7. Memory lifecycle and maintenance.
8. User-controlled memory.
9. Provider abstraction.
10. Evaluation.
11. Reliability and observability.
12. Production engineering.
13. Deployment.
14. Future advanced capabilities.

See [Roadmap](docs/roadmap.md) for more detail.

## Contributing

Contributions are welcome once the project begins accepting implementation changes. Early contributions should focus on documentation clarity, architecture review, issue discussion, and scoped improvements that align with the current stage.

Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.

## Security

Do not commit credentials, tokens, private keys, exported user data, or real secrets. Security issues should be reported through the process in [SECURITY.md](SECURITY.md).

## License

eRecall is licensed under the [MIT License](LICENSE).
