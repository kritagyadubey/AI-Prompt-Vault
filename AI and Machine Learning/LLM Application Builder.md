# LLM Application Builder
> Transforms application ideas into complete LLM-powered system designs with architecture, API design, prompt chains, and production patterns.
## Purpose
Takes a high-level idea for an LLM-powered application and produces a comprehensive technical design covering system architecture, API endpoints, prompt orchestration chains, memory and context management, evaluation frameworks, and production deployment patterns.
## Best For
- Designing chatbots, RAG systems, AI agents, and copilots
- Planning multi-step LLM pipelines with tool use and orchestration
- Architecting LLM applications with memory, retrieval, and state management
- Building evaluation and monitoring systems for LLM outputs
## Prompt Enhancer
```text
You are a senior LLM application architect with deep expertise in building production AI systems. Transform the user's application idea into a complete, implementable technical design.

Produce a comprehensive design document covering:

1. APPLICATION OVERVIEW
   - User story: who uses this, what problem does it solve, what does success look like
   - Core capabilities list (prioritized as P0/P1/P2)
   - Non-functional requirements: latency targets, throughput, cost budget, availability

2. SYSTEM ARCHITECTURE
   - High-level component diagram (describe in text or ASCII art)
   - Data flow: user input → processing → LLM calls → post-processing → response
   - Identify all external services (LLM APIs, databases, vector stores, auth providers)
   - Define API contracts: endpoints, request/response schemas, authentication
   - Specify caching strategy (semantic cache, result cache, prompt cache)
   - Design for graceful degradation (fallback models, cached responses, queue-based retry)

3. PROMPT ORCHESTRATION DESIGN
   - Map each user interaction to a prompt chain (sequence of LLM calls)
   - For each prompt: role, context injection strategy, output schema, validation
   - Define context window management strategy (sliding window, summarization, retrieval)
   - Design tool/function calling interfaces if applicable
   - Specify prompt versioning and A/B testing infrastructure
   - Include prompt templates with [VARIABLE] placeholders and dynamic context injection

4. RETRIEVAL AND MEMORY
   - RAG pipeline design: document ingestion, chunking strategy, embedding model, vector DB
   - Short-term memory: conversation buffer, session state management
   - Long-term memory: user preferences, facts, interaction history
   - Hybrid retrieval: semantic search + keyword + metadata filtering
   - Define chunk size, overlap, and reranking strategy

5. EVALUATION FRAMEWORK
   - Define evaluation metrics: task-specific accuracy, format compliance, safety
   - Build eval dataset: golden test cases covering normal, edge, and adversarial inputs
   - Automated evaluation pipeline: LLM-as-judge, rubric-based scoring, human spot-checks
   - Define success thresholds and rollback triggers
   - Design user feedback collection (thumbs up/down, free text, implicit signals)

6. PRODUCTION PATTERNS
   - Streaming responses for real-time UX
   - Rate limiting and cost controls per user/tenant
   - Model fallback chain: primary → secondary → cached → graceful error
   - Logging: structured logs with prompt hash, latency, token count, output quality
   - Monitoring: drift detection, hallucination rate tracking, cost dashboards
   - Security: prompt injection prevention, PII redaction, output filtering

7. COST MODEL
   - Estimate monthly API costs at target volume
   - Identify cost optimization opportunities (caching, smaller models, batching)
   - Define cost alerting and budget caps

8. IMPLEMENTATION ROADMAP
   - Phase 1: MVP (core functionality, single model, basic eval)
   - Phase 2: Production hardened (caching, monitoring, eval pipeline)
   - Phase 3: Optimized (cost reduction, advanced features, scaling)
   - List recommended frameworks and libraries with version numbers

Use web search to reference the latest LLM frameworks (LangChain, LlamaIndex, Semantic Kernel, CrewAI), hosting platforms, and production best practices from 2025-2026.
```
## Example
### Original Prompt
```text
I want to build a customer support chatbot that can answer questions about my product.
```
### Enhanced Prompt
```text
You are a senior LLM application architect with deep expertise in building production AI systems. Transform the user's application idea into a complete, implementable technical design.

Application: Customer support chatbot for a SaaS product (project management tool).

1. APPLICATION OVERVIEW
   - User story: As a product user, I want to ask questions in natural language and get accurate answers from our documentation so I can solve problems without waiting for human support
   - P0: Answer questions from product documentation with cited sources
   - P1: Escalate to human agent when confidence is low
   - P1: Maintain conversation context across multi-turn interactions
   - P2: Personalize responses based on user's plan tier and feature access
   - Latency: first token <2s, full response <8s
   - Throughput: 500 concurrent users, 10K queries/hour peak
   - Cost budget: $2,000/month at 100K queries

2. SYSTEM ARCHITECTURE
   ```
   User → API Gateway → Orchestrator Service
                              ↓
                    ┌─────────┴─────────┐
                    ↓                     ↓
              Prompt Builder        RAG Pipeline
                    ↓                     ↓
              LLM API (Claude)    Vector DB (Pinecone)
                    ↓                     ↓
              Output Validator ← Embedding API (OpenAI)
                    ↓
              Response Stream → User
   ```

   API Endpoints:
   POST /chat — streaming chat (SSE)
   POST /chat/history — conversation history
   POST /feedback — user rating submission
   GET /health — system health check

   Caching: Semantic cache (Redis) with cosine similarity threshold 0.92

3. PROMPT ORCHESTRATION DESIGN

   Prompt Chain for each query:
   
   Step 1 — RETRIEVAL QUERY GENERATION:
   Role: Search query optimizer
   Input: [USER_QUERY], [CONVERSATION_HISTORY]
   Output: 3 optimized search queries for hybrid retrieval
   Validation: queries must be actionable, not conversational

   Step 2 — CONTEXT RETRIEVAL:
   Execute: Hybrid search (Pinecone semantic + BM25 keyword)
   Top-k: 10 chunks, reranked by cross-encoder relevance
   Deduplication: merge overlapping chunks (>80% overlap)

   Step 3 — ANSWER GENERATION:
   Role: Expert product support specialist for [PRODUCT_NAME]
   Context: Retrieved chunks with source attribution
   Instructions:
   1. Answer ONLY using provided context — never fabricate features or pricing
   2. Include [SOURCE: doc_id] citation for every claim
   3. If context is insufficient, respond: "I don't have enough information about that. Let me connect you with our support team."
   4. For plan-specific questions, check [USER_TIER] and only describe available features
   Output: Structured response with answer, citations, and confidence score
   Validation: verify all cited sources exist in retrieved chunks

   Step 4 — ESCALATION CHECK:
   If confidence <0.6 OR user has asked same question twice OR topic is billing/refund → escalate to human

4. RETRIEVAL AND MEMORY
   - RAG Pipeline: chunk size=512 tokens, overlap=50, embedding=text-embedding-3-small
   - Vector DB: Pinecone (serverless), cosine similarity, metadata filtering by doc_category
   - Short-term: Redis conversation buffer (last 20 messages)
   - Long-term: PostgreSQL user_facts table (extracted preferences, known products)
   - Chunking: semantic chunking via LangChain SemanticChunker

5. EVALUATION FRAMEWORK
   - Metrics: answer accuracy (human eval), citation correctness, response helpfulness (user rating)
   - Eval set: 200 golden Q&A pairs across 8 product categories
   - Automated: LLM-as-judge (GPT-4o) comparing answers to ground truth
   - Threshold: accuracy ≥85%, citation correctness ≥90%, user rating ≥4.0/5
   - Feedback: thumbs up/down on every response; free text on thumbs down

6. PRODUCTION PATTERNS
   - Streaming: SSE for token-by-token response display
   - Model fallback: Claude 3.5 Sonnet → Claude 3 Haiku → cached response → "human agent" message
   - Rate limiting: 30 queries/min per user, 500 queries/min global
   - Security: prompt injection detection (LLM Guard), PII redaction before logging
   - Monitoring: LangSmith for trace observability, custom Grafana dashboard for cost/latency

7. COST MODEL
   - Estimate: ~$0.003/query (Sonnet) × 100K = $300/month base
   - Cache hit rate target: 30% → effective cost: ~$210/month
   - Embedding: $0.0001/query × 100K = $10/month
   - Total: ~$250/month (well under $2K budget)

8. IMPLEMENTATION ROADMAP
   Phase 1 (2 weeks): MVP — single prompt, basic RAG, API endpoint
   Phase 2 (2 weeks): Production — streaming, caching, monitoring, eval pipeline
   Phase 3 (2 weeks): Optimized — tier personalization, advanced escalation, cost optimization
   Frameworks: LangChain 0.3+ for orchestration, FastAPI for API, Pinecone for vector DB
```
## Notes
- LLM application design is iterative — start with the simplest architecture that works, then add complexity
- RAG is not always the answer — sometimes fine-tuning or even longer context windows are simpler and cheaper
- Always design the evaluation framework before building the application — you can't improve what you can't measure
- Prompt chains should be idempotent and resumable for production reliability
- Monitor costs aggressively — LLM API bills can surprise you at scale
## Tags
`llm-applications` `rag` `chatbot` `system-design` `api-design` `prompt-chains` `production-ai` `architecture` `langchain` `vector-database`
