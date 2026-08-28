# ADR 0005: Require Provider Abstractions for Model and Embedding Services

## Status

Accepted

## Context

eRecall will likely depend on external model and embedding providers. Coupling core memory behavior directly to one provider would make evaluation, cost control, portability, and future provider changes harder.

## Decision

Future model, embedding, extraction, and evaluation integrations must sit behind explicit provider abstractions. Core services should depend on project-owned interfaces rather than vendor SDKs directly.

## Consequences

- Provider changes can be evaluated and implemented with less domain churn.
- Tests can use local or fake provider implementations.
- Initial interfaces must be designed carefully enough to avoid hiding important provider behavior.
