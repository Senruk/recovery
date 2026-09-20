---
name: "AI Engineering Roadmap"
description: "Notes from the mentor deck on going from vibe coding to real AI systems"
type: reference
---

# AI Engineering Roadmap

**Source:** Mentor session with dad's friend (Lead Tech, ~£70k)
**Date:** 2026-07-18

---

## The Core Message

> "The model is powerful, but the product value comes from the system around it: data, retrieval, tools, workflow, security, evaluation, and monitoring."

Calling an LLM API is easy. Building a reliable AI application that solves a business problem is the real skill.

---

## The 5-Stage Path

1. **Programming** — Python/TS, functions, classes, async, error handling, clean code
2. **Software Engineering** — Git, APIs, databases, testing, system design, security
3. **Cloud & DevOps** — Docker, CI/CD, logging, monitoring, deployment
4. **AI Engineering** — LLMs, RAG, agents, data pipelines, evaluation, guardrails
5. **Enterprise AI** — Production systems with security, compliance, scale

---

## The 4 Architecture Patterns

| Pattern | What | When |
|---------|------|------|
| Simple LLM call | Input → LLM → Output | Summarisation, rewriting, extraction |
| RAG | Question → Retrieve → LLM | Company knowledge Q&A |
| Agent/Tool use | Goal → Tools → Result | Multi-step tasks needing API calls |
| Workflow pipeline | Data → Steps → Review | Deterministic processes with AI steps |

---

## AI Application Layers

| Layer | Components |
|-------|------------|
| User | Web, Mobile, WhatsApp, Voice, Auth, Permissions |
| Application | Backend API, Business logic, Conversation state, Workflow engine |
| AI | Prompt builder, Model router, Tool calling, Guardrails, Memory |
| Knowledge | Vector DB, SQL, Search, Documents, APIs, Business rules |
| Quality | Evaluation, Logging, Tracing, Human review, Analytics |

---

## Tech Stack Reference

| Category | Tools |
|----------|-------|
| Models | OpenAI, Claude, Gemini, Llama, Mistral, Qwen |
| Embeddings | OpenAI, Cohere, Voyage, BGE, Nomic |
| Vector DBs | Qdrant, Pinecone, Weaviate, Chroma, FAISS, Milvus |
| Search | Elasticsearch, OpenSearch, Azure AI Search |
| Frameworks | OpenAI Agents SDK, LangGraph, LlamaIndex, Haystack, Vercel AI SDK |
| Evaluation | Ragas, DeepEval, promptfoo, OpenAI Evals |
| Observability | Langfuse, LangSmith, Helicone, Phoenix, OpenTelemetry |
| Guardrails | Presidio, NeMo Guardrails, Guardrails AI, Pydantic validation |

---

## Portfolio Projects (From Deck)

1. **Company policy assistant** — Upload docs, retrieve relevant sections, answer with citations, collect feedback
2. **Customer support agent** — RAG + escalation + tone controls + human handoff + conversation summary
3. **Invoice/document processor** — Extract structured data, validate fields, flag missing info, route for human review
4. **SQL analytics assistant** — Natural language → safe SQL → explain results → prevent dangerous queries

---

## Strong vs Weak AI Use

| Weak | Strong |
|------|--------|
| Paste vague prompt | Plan first |
| Accept code without understanding | Ask for options and trade-offs |
| No tests | Review generated code |
| No architecture | Add tests |
| No debugging skill | Refactor deliberately |
| No documentation | Document decisions |

---

## 6-Month Learning Path

- **Month 1:** LLM APIs, prompting, structured output, basic app
- **Month 2:** Embeddings, vector databases, chunking, simple RAG
- **Month 3:** Tool calling, agents, workflow design, API integration
- **Month 4:** Data ingestion pipeline, cleaning, metadata, evaluation dataset
- **Month 5:** Deployment, Docker, cloud basics, observability, security
- **Month 6:** Polished portfolio project with README, demo, architecture diagram

---

## My Action Plan

### Week 1: Testing
Add tests to AI receptionist backend

### Week 2: Docker
Containerise the AI receptionist

### Week 3: RAG Knowledge Layer
Add document retrieval to the receptionist

### Week 4: Monitoring
Add Langfuse tracing

### Week 5: CI/CD
GitHub Actions auto-deploy

### Week 6: Polish
README, architecture diagram, demo video
