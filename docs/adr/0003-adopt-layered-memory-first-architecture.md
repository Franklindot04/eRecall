# ADR 0003: Adopt Layered Memory-First Architecture

## Status

Accepted

## Context

eRecall is centered on persistent, user-controlled conversational memory. Future implementation must support conversation handling, extraction, retrieval, maintenance, persistence, provider integrations, observability, security, and evaluation without collapsing these responsibilities into one component.

## Decision

The project will use a layered architecture:

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

Major components should communicate through explicit interfaces. Provider-specific clients and infrastructure drivers should remain outside core domain logic.

## Consequences

- Memory behavior can be tested and evolved independently from user interface and provider details.
- The architecture supports provider independence and infrastructure portability.
- The project may need additional contract documentation as interfaces become public.
