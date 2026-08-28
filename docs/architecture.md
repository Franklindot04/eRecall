# Architecture

This document describes the intended eRecall architecture at a high level. It defines responsibilities and boundaries for future implementation; it does not imply that the components exist yet.

## System Shape

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

## Layer Responsibilities

### Client / Frontend

The frontend will provide the user-facing experience for conversations, account flows, memory review, consent, correction, deletion, and project settings. It should not own memory extraction or retrieval logic.

Current technology direction: Next.js, TypeScript, and Tailwind CSS.

### API / Application Layer

The API layer will expose stable service boundaries for clients and integrations. It should handle request validation, authentication boundaries, authorization checks, session context, response shaping, and orchestration into core services.

Current technology direction: Python, FastAPI, and Pydantic.

### Core Services

Core services will coordinate domain workflows without depending directly on vendor-specific model clients or storage drivers. Expected service areas include:

- Conversation handling.
- Memory extraction.
- Memory retrieval.
- Memory maintenance.
- User memory controls.
- Evaluation workflows.
- Observability instrumentation.

### Memory System

The memory system will model persistent information explicitly. It should account for:

- Structured memories with type, source, confidence, timestamps, lifecycle state, and provenance.
- Conversation-derived memories that can be inspected and corrected.
- Semantic retrieval using embedding abstractions.
- Maintenance operations such as merging, expiration, deduplication, archiving, and deletion.
- User-controlled visibility, correction, export, and removal.

Memory should remain understandable as domain data rather than being hidden entirely inside prompts or provider-specific features.

### Persistence / Retrieval Infrastructure

Storage and retrieval infrastructure should support structured persistence, semantic/vector retrieval, caching, and asynchronous work only where justified.

Current technology direction:

- PostgreSQL for structured data.
- Qdrant for vector search.
- Redis for caching or queue-adjacent responsibilities when needed.

Infrastructure choices should remain portable and cost-conscious.

### External Providers

External providers may include chat models, embedding models, evaluators, telemetry backends, and deployment platforms. The core application should depend on explicit interfaces rather than direct provider coupling.

Provider abstractions should make it possible to replace chat, embedding, extraction, and evaluation implementations without rewriting domain logic.

## Cross-Cutting Concerns

### Security and Privacy

Security and privacy must be designed into the architecture from the beginning. Persistent memory should be treated as sensitive data, with explicit user control, clear authorization boundaries, least-privilege credentials, careful logging, and deletion semantics.

### Observability

Future services should emit useful traces, metrics, and structured logs around request flow, provider calls, memory extraction, retrieval quality, latency, errors, and maintenance jobs. The intended direction is OpenTelemetry with Prometheus and Grafana where appropriate.

### Evaluation

Memory behavior should be evaluated deliberately. Future evaluation should cover extraction quality, retrieval relevance, stale memory handling, privacy expectations, and regression behavior across provider changes.

### Deployment

Deployment design is intentionally deferred. Future deployment should favor portable, reproducible, and cost-conscious options before selecting managed services or hosting providers.

## Architectural Principles

- Keep major layers modular and independently understandable.
- Separate client experience, API orchestration, domain services, storage, and provider integrations.
- Design APIs and contracts before relying on implementation details.
- Configure services through environment variables and documented defaults.
- Keep provider-specific logic behind explicit interfaces.
- Prefer testable domain logic over framework-coupled code.
- Add observability at important boundaries and workflows.
- Apply security by design and least privilege.
- Preserve backward compatibility where practical once public interfaces exist.
- Make persistent memory inspectable, correctable, and deletable by users.
- Handle stored information with privacy-conscious defaults.
- Keep local development reproducible.
- Prefer infrastructure portability and realistic operating costs.
- Avoid abstractions until they clarify ownership or reduce real duplication.
