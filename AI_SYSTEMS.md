# Applied AI system case studies

These notes describe systems I designed and implemented. Product repositories remain private because the applications are active. The descriptions focus on architecture, decisions, failure handling and measured outcomes without exposing credentials or user data.

## Shater: document RAG for Arabic learners

**Problem.** Students have large course PDFs and need fast, grounded study help in Arabic and English.

**System.** The ingestion path extracts text from PDFs, divides it into approximately 500-word semantic chunks, generates Cohere `embed-english-v3.0` document embeddings and stores them in Supabase with pgvector. At query time, a query embedding drives a vector-match RPC; retrieved chunks and document metadata are passed to Claude for grounded chat, summaries, quizzes and flashcards.

**Reliability choices.** The application tracks whether indexing is complete, uses the full document as an explicit fallback when retrieval is unavailable, preserves document titles for citation context and supports image input alongside text. API routes validate requests and keep model/provider concerns behind server-side boundaries.

**Delivery.** Next.js, TypeScript, Anthropic Claude, Cohere, Supabase/PostgreSQL, pgvector, PostHog, RevenueCat and iOS delivery.

**Outcome.** More than 4,600 registered users and 50,000 generated study items.

## Daftar: multilingual knowledge ingestion and retrieval

**Problem.** Useful information is scattered across links, PDFs, screenshots, videos and notes. Saving it is easy; finding and using it later is difficult.

**System.** Daftar normalizes multiple input types into a per-user item model. Background jobs run Gemini-based enrichment, multimodal OCR and schema-constrained structured generation. Normalized 1,536-dimensional embeddings support semantic search, while ranking and auto-filing place content into useful spaces. Chat tools retrieve relevant sources and return source-grounded answers across Arabic and English content.

**Reliability choices.** Jobs are idempotent and include retry/fallback paths. Content-hash caches avoid repeated model calls. Rate and spend controls protect production usage. Authentication, row-level security and namespaced storage isolate each user's data. Deterministic tests cover the shared ranking and processing logic.

**Delivery.** Next.js 16, React 19, TypeScript, SwiftUI, Supabase Edge Functions, PostgreSQL/pgvector, Gemini, Vercel and PostHog.

## Qooti: multimodal nutrition capture

**Problem.** Manual nutrition logging creates too much friction for Arabic-speaking users.

**System.** Qooti combines AI-assisted food-image analysis, barcode scanning and a review flow that keeps the user in control of saved nutrition data. The client and backend share production patterns for authentication, queued work, localization, analytics and AI rate controls.

**Delivery.** SwiftUI, Supabase, Edge Functions, Gemini, PostHog and App Store distribution.

**Outcome.** More than 1,700 profiles and 1,000 confirmed meal logs by September 2026.

## How I work

1. Start from a user workflow and define the smallest measurable outcome.
2. Design the data model and AI boundary before choosing prompts or models.
3. Make structured outputs, retries, caching, limits and observability part of the first production design.
4. Test deterministic logic separately from model behavior.
5. Measure activation and repeated use after launch, then simplify the system around what users actually do.

