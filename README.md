# Abdulrahman Alsaher

### Applied AI Engineer · AI Product Builder

I design and ship Arabic-first AI products from architecture through deployment and measurement. My work covers retrieval-augmented generation, document processing, embeddings, semantic search, multimodal extraction, structured LLM output, production analytics and web/iOS delivery.

I am completing a **BSc in Computer Science at the University of Manchester** and was selected as a **Qimam Fellow** from more than 18,000 applicants.

[LinkedIn](https://www.linkedin.com/in/abdulrahmansh/) · [AI system case studies](AI_SYSTEMS.md) · [Engineering archive](PROJECTS.md) · [Repository guide](REPOSITORIES.md)

## Shipped AI products

| Product | System I designed and built | Evidence |
| --- | --- | --- |
| **[Shater](https://learnshater.com)** | Arabic-first study platform that converts PDFs into summaries, quizzes, flashcards and source-grounded chat | **4,600+ users** · **50,000+ generated study items** |
| **[Daftar](https://yourdaftar.com)** | Bilingual private knowledge system for saving, enriching, searching and discussing documents, screenshots, links, video and notes | Multimodal ingestion · semantic search · web and iOS clients |
| **Qooti** | Arabic-first nutrition app with AI food-image analysis and barcode scanning | **1,700+ profiles** · **1,000+ confirmed meal logs** |

## Applied AI engineering

- **Retrieval and grounding:** semantic chunking, Cohere and Gemini embeddings, PostgreSQL/pgvector retrieval, reranking, citations and full-document fallback paths.
- **Multimodal ingestion:** PDF extraction, image OCR, screenshot and document enrichment, structured JSON output and background processing.
- **Production controls:** retries, content-hash caching, rate limits, spend tracking, authentication, per-user data isolation and deterministic tests.
- **Product delivery:** TypeScript, Next.js, Supabase, PostgreSQL, Edge Functions, SwiftUI, Vercel, PostHog and RevenueCat.

Read the architecture and implementation notes in **[AI_SYSTEMS.md](AI_SYSTEMS.md)**.

## Selected system snapshots

### Shater — document RAG for Arabic learners

Shater extracts and chunks student documents, generates embeddings, retrieves relevant context from pgvector and sends grounded prompts to Claude. The chat workflow supports citations, images and explicit fallback behavior when retrieval has not finished. I built the product across the web and iOS surfaces and instrumented the user journey from activation to subscription.

### Daftar — multilingual personal knowledge infrastructure

Daftar accepts multiple content types and processes them through enrichment, OCR, embeddings, semantic ranking and auto-filing workflows. The architecture includes background workers, model fallbacks, caching, cost controls and shared web/iOS product behavior.

### Qooti — multimodal consumer AI

Qooti combines food-image analysis and barcode lookup in an Arabic-first nutrition flow. I owned product architecture, UX, testing, analytics and operations from the first build through launch.

## Engineering foundations

My academic work includes processor design in Verilog, systems programming in C/C++, RISC-V assembly, cache simulation, Java/Spring services and browser graphics. The **[engineering archive](PROJECTS.md)** separates individual work, team work and course-provided starter code, and records the verification run for each project.

## Current focus

I am interested in applied AI engineering roles where I can build reliable systems around real user workflows: document intelligence, retrieval, structured extraction, internal tools and agent-assisted operations.

Most product source is private because the applications are active. The linked case studies describe the architecture, my contribution and the evidence that can be shared publicly. I can walk through implementation details and selected code in an interview.
