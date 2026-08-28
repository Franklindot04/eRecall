# ADR 0001: Record Architecture Decisions

## Status

Accepted

## Context

eRecall is intended to become a production-oriented open-source project with long-lived architectural decisions around memory, persistence, providers, security, evaluation, and deployment.

Without a lightweight decision record, future contributors may have to infer why foundational choices were made.

## Decision

The project will use Architecture Decision Records in `docs/adr/` for decisions that materially affect architecture, boundaries, dependencies, operations, security, or contributor workflows.

Each ADR will record status, context, decision, and consequences.

## Consequences

- Contributors have a durable record of important decisions.
- Future changes can supersede previous decisions without rewriting history.
- The project avoids over-documenting minor implementation details as architecture decisions.
