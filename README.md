# eRecall — Enhanced Recall AI Chatbot

A memory‑first AI assistant designed to learn, adapt, and remember user interactions over time.
Built with a modern architecture combining LLMs, vector databases, memory extraction, and semantic retrieval.

# Status

🚧 Active Development Phase  
eRecall is currently under construction. Core components are being implemented, refined, and tested.  
Expect rapid iteration, new features, and architectural improvements.

# Overview

eRecall (short for Enhanced Recall) is an AI chatbot engineered to maintain long‑term memory across sessions.

Unlike traditional chatbots that forget everything after each message, eRecall builds a persistent memory profile using:

- Memory extraction
- Vector embeddings
- Semantic search
- Episodic + structured memory
- Maintenance agents

This enables eRecall to deliver context‑aware, personalized, and adaptive conversations.

# Key Features

- Long‑Term Memory  
  Stores user preferences, facts, events, and summaries.

- Memory Extraction Engine  
  Converts raw messages into structured “atomic memories.”

- Vector-Based Semantic Retrieval  
  Uses embeddings and similarity search to recall relevant information.

- Memory Maintenance Agent  
  Updates, merges, summarizes, and cleans memory over time.

- User Profiles  
  Persistent identity and multi-user support.

- Modular Architecture  
  Easy to extend, replace components, or integrate new models.

# High-Level Architecture

1. Frontend (Next.js)
   - Chat UI
   - Streaming responses
   - Authentication
   - Session management

2. Backend API (FastAPI / Node.js)
   - /chat — main chat endpoint
   - /extract_memory — memory extraction
   - /retrieve_memory — semantic search
   - /maintain_memory — memory cleanup and updates
   - /profile — user identity and metadata

3. Memory Layer
   - Episodic Memory — events, interactions
   - Semantic Memory — facts, preferences
   - Summary Memory — compressed long-term context
   - Vector Embeddings — for similarity search
   - Graph Relationships (future)

4. LLM Layer
   - Chat model
   - Extractor model
   - Summarizer model
   - Maintenance agent model

5. Database Layer
   - Qdrant — vector DB
   - PostgreSQL — structured memory and profiles
   - Redis — caching recent messages

# Tech Stack

Frontend:
- Next.js
- TailwindCSS
- SWR
- WebSockets

Backend:
- FastAPI / Node.js
- Pydantic
- Celery / BullMQ

Memory & Storage:
- Qdrant
- PostgreSQL
- Redis

AI & Embeddings:
- OpenAI / Anthropic / Groq
- SentenceTransformers
- LangChain (optional)

DevOps:
- Docker
- GitHub Actions
- Railway / Fly.io / Azure

# Project Roadmap

## Phase 1 — Foundations (Week 1)
- Repo structure
- Basic backend
- Basic frontend chat UI
- Streaming chat endpoint

## Phase 2 — Memory Extraction (Week 2)
- Memory schema
- Extraction prompts
- Embedding pipeline
- Qdrant integration

## Phase 3 — Memory Retrieval (Week 3)
- Semantic search
- Relevance scoring
- Memory injection into prompts

## Phase 4 — Memory Maintenance (Week 4)
- Maintenance agent
- Contradiction detection
- Summary generation
- Memory cleanup

## Phase 5 — User Profiles (Week 5)
- Authentication
- User identity
- Profile-linked memory

## Phase 6 — Advanced Memory (Week 6)
- Graph memory
- Importance scoring
- Time decay

## Phase 7 — Production (Week 7)
- Docker deployment
- CI/CD
- Monitoring
- Documentation

Note: Roadmap is flexible and will evolve as the project grows.

# Contributing

Contributions are welcome!

Since eRecall is in active development, you can help by:

- Reporting issues
- Suggesting features
- Improving documentation
- Contributing to memory extraction, retrieval, or UI components

Please open a pull request or start a discussion.

# License

This project will use the MIT License (recommended for open-source adoption).  
You may update this section once the license file is added.

# Development Status

eRecall is currently in early development.  
Many components are experimental, incomplete, or subject to change.  
Expect frequent updates, refactoring, and architectural improvements.

# Branding

eRecall = Enhanced Recall  
A modern AI assistant that remembers you.

# Contact

If you have suggestions or want to collaborate, feel free to open an issue or discussion in the repo.
