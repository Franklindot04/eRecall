# Roadmap

This roadmap is organized by engineering phase. It intentionally avoids artificial dates because requirements will become clearer as each phase is completed.

## Phase 0: Repository and Architecture Foundation

Establish repository structure, governance files, high-level architecture, development standards, security expectations, roadmap, and ADR practices.

## Phase 1: Core Application Foundation

Introduce the minimal frontend and backend application foundations, local development workflow, baseline tests, formatting, linting, and service boundaries.

## Phase 2: Conversation Persistence

Persist conversations, messages, sessions, and related metadata with clear ownership and retention expectations.

## Phase 3: Memory Extraction

Define memory schemas and extraction workflows that can convert conversations into reviewable structured memory records.

## Phase 4: Memory Storage

Store memory records in structured persistence with lifecycle metadata, provenance, and deletion support.

## Phase 5: Memory Retrieval

Introduce semantic retrieval and relevance ranking through provider-independent embedding and vector search interfaces.

## Phase 6: Memory Lifecycle and Maintenance

Support deduplication, merging, conflict handling, expiration, archiving, summarization, and maintenance workflows.

## Phase 7: User-Controlled Memory

Build user-facing controls for memory inspection, correction, deletion, consent, and export where appropriate.

## Phase 8: Provider Abstraction

Harden provider boundaries for chat models, embeddings, extraction, evaluation, and future model integrations.

## Phase 9: Evaluation

Create repeatable evaluation practices for memory extraction quality, retrieval relevance, privacy behavior, and provider changes.

## Phase 10: Reliability and Observability

Add tracing, metrics, logs, operational dashboards, health checks, and failure-mode analysis for critical workflows.

## Phase 11: Production Engineering

Strengthen security, data retention, migrations, background processing, performance, dependency management, and operational runbooks.

## Phase 12: Deployment

Evaluate hosting and deployment options based on portability, cost, security, reliability, and self-hosting feasibility.

## Phase 13: Future Advanced Capabilities

Explore advanced memory models, richer personalization, graph relationships, collaborative memory, and additional provider integrations when core behavior is reliable.
