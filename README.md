# 🧠 AI/LLM Learning Roadmap
### C++ Backend Developer → AI Application Engineer
> **Duration:** 6–7 Months &nbsp;|&nbsp; **Schedule:** 2–3 hrs/day (~400–450 hrs total) &nbsp;|&nbsp; **Last Updated:** March 2026

---

## 👤 Profile & Context

| Field | Detail |
|---|---|
| Background | C++ backend, 2.5 years — legacy systems, migration, optimization |
| Python Level | Basic (can read it, written small scripts) |
| Goal | LLM application development AND platform/infra understanding |
| Budget | Mostly free; ~$10–20 total on API credits |
| Schedule | 2–3 hours/day, 7 days/week (~15–18 hrs/week) |

### Your C++ Background is an Asset
- Performance intuition maps directly to LLM inference optimization
- Memory and systems reasoning applies to vector stores, batching, serving
- `llama.cpp` and `vLLM` — the dominant inference engines — are C++ codebases
- You will understand production tradeoffs that pure Python developers miss

---

## 🗺️ Roadmap Overview

```
Phase 1 │ Weeks  1– 4 │ Python Solidification + Modern Tooling     │ ~60 hrs
Phase 2 │ Weeks  5– 8 │ AI/ML Conceptual Foundations               │ ~60 hrs
Phase 3 │ Weeks  9–12 │ LLM APIs & Prompt Engineering              │ ~65 hrs
Phase 4 │ Weeks 13–18 │ RAG & LLM Application Frameworks           │ ~90 hrs
Phase 5 │ Weeks 19–23 │ AI Agents & Advanced Patterns              │ ~80 hrs
Phase 6 │ Weeks 24–27 │ Production, LLMOps & Open-Source Models    │ ~70 hrs
Capstone│ Weeks 27–28 │ Flagship Portfolio Project                 │ ~25 hrs
```

---

## Phase 1 — Python Solidification + Modern Tooling
`Weeks 1–4` &nbsp; `~60 hrs`

**Goal:** Close the gap between "can read Python" and "can build real things fluently." Pick up the surrounding modern ecosystem used in every AI project.

### Topics
- Python: OOP, list comprehensions, generators, decorators
- Python: `asyncio` basics, type hints, virtual environments (`venv` / `uv`)
- Tooling: Git branching and PRs (deepen what you know)
- Tooling: Docker fundamentals
- REST APIs: how HTTP actually works, request/response lifecycle
- Framework: **FastAPI** — build a working REST API

### Resources

| # | Resource | Cost | Time | Notes |
|---|---|---|---|---|
| 1 | [Automate the Boring Stuff with Python](https://automatetheboringstuff.com/) | Free | ~6 hrs | Chapters 1–10 only. Covers practical gaps fast. |
| 2 | [Real Python — targeted articles](https://realpython.com/) | Free tier | Varies | Read articles on OOP, asyncio, type hints individually |
| 3 | [FastAPI Official Tutorial](https://fastapi.tiangolo.com/tutorial/) | Free | 4–5 hrs | Best-in-class docs. Industry standard for AI APIs. |
| 4 | [Docker Getting Started Guide](https://docs.docker.com/get-started/) | Free | ~4 hrs | Complete in one weekend |

### Week-by-Week
| Week | Focus |
|---|---|
| 1 | Python OOP, type hints, comprehensions, generators (Automate Ch 1–5) |
| 2 | asyncio, decorators, venv/uv setup (Automate Ch 6–10 + Real Python) |
| 3 | FastAPI tutorial end-to-end |
| 4 | Docker guide + containerize the FastAPI app |

### ✅ Milestone
- [ ] A working FastAPI app containerized in Docker, pushed to a **public GitHub repo**
  - Accepts text input via `POST` request
  - Returns a structured JSON response

---

## Phase 2 — AI/ML Conceptual Foundations
`Weeks 5–8` &nbsp; `~60 hrs`

**Goal:** Understand what LLMs are, why they work, and how to reason about them. You do **not** need to become an ML researcher — you need enough depth to make good architectural decisions.

### Topics
- What neural networks are (intuition + light math, no proofs)
- How transformers work: attention mechanism, tokens, embeddings
- Training vs inference — what happens at each stage
- RLHF — what it is and why it matters for LLM behavior
- Fine-tuning vs prompting vs RAG — when to use each
- How to read model cards and interpret benchmarks

### Resources

| # | Resource | Cost | Time | Notes |
|---|---|---|---|---|
| 1 | [3Blue1Brown — Neural Networks Series](https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi) | Free | ~4 hrs | Best visual intuition available. No prior math needed. |
| 2 | [Andrej Karpathy — Neural Networks: Zero to Hero](https://www.youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ) | Free | ~8 hrs | **Watch first 4 videos only.** Karpathy was OpenAI founding team. Highest-quality free ML content that exists. |
| 3 | [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) | Free | ~1 hr | Makes transformer architecture click visually. **Read twice.** |
| 4 | [fast.ai — Practical Deep Learning for Coders](https://course.fast.ai/) | Free | ~6 hrs | Lessons 1–3 only. Top-down practical approach. |

### 🔗 C++ Bridge — Do This in Week 5
> Read the [`llama.cpp` GitHub README](https://github.com/ggerganov/llama.cpp) and skim the Issues tab.
> This is the most widely-used open-source LLM inference engine — written in C++.
> You will understand most of the performance decisions immediately. This is also a future **open-source contribution path** for you.

### Week-by-Week
| Week | Focus |
|---|---|
| 5 | 3Blue1Brown playlist + llama.cpp README |
| 6 | Karpathy videos 1–2 + Illustrated Transformer article |
| 7 | Karpathy videos 3–4 |
| 8 | fast.ai Lessons 1–3 |

### ✅ Milestone
Can explain in plain English:
- [ ] How a transformer processes text (tokens, attention, embeddings)
- [ ] The difference between training and inference
- [ ] What fine-tuning means vs prompting vs RAG
- [ ] Why context window size matters

---

## Phase 3 — LLM APIs & Prompt Engineering
`Weeks 9–12` &nbsp; `~65 hrs`

**Goal:** Go hands-on with real LLMs via API. Prompt engineering is a real, learnable skill — a large percentage of AI application quality comes from it.

### Topics
- OpenAI API fundamentals (industry standard, most widely used)
- Anthropic Claude API fundamentals (second most important)
- System prompts, user prompts, conversation history
- Few-shot prompting, chain-of-thought prompting
- Structured outputs: JSON mode, function calling / tool use
- Tokens, context windows, and cost reasoning
- Embeddings: what they are, how to generate and use them
- Rate limits, retries, error handling

### ⚙️ Setup — Do This at the Start of Week 9
- Create [OpenAI account](https://platform.openai.com/) — load **$5–10** in credits
- Create [Anthropic account](https://console.anthropic.com/) — load **$5–10** in credits
- These credits will cover **all** experiments in Phase 3 and Phase 4

> 💡 **Cost tip:** Use `gpt-4o-mini` and `claude-haiku` for all experiments. Use `gpt-4o` / `claude-sonnet` only when output quality actually matters.

### Resources

| # | Resource | Cost | Time | Notes |
|---|---|---|---|---|
| 1 | [DeepLearning.AI — Prompt Engineering for Developers](https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/) | Free | ~1.5 hrs | Co-created with OpenAI. Start here. |
| 2 | [Anthropic Prompt Engineering Guide](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview) | Free | ~2 hrs | Extremely well-written. Read fully, not just skim. |
| 3 | [OpenAI Cookbook (GitHub)](https://github.com/openai/openai-cookbook) | Free | Ongoing | Practical recipes you can run immediately. Bookmark. |
| 4 | [DeepLearning.AI — Building Systems with ChatGPT API](https://www.deeplearning.ai/short-courses/building-systems-with-chatgpt/) | Free | ~1.5 hrs | |

### Week-by-Week
| Week | Focus |
|---|---|
| 9 | Account setup + prompt engineering course + API basics |
| 10 | Anthropic guide fully + structured outputs / function calling |
| 11 | Embeddings deep dive + OpenAI Cookbook experiments |
| 12 | Building Systems course + project build |

### ✅ Milestone
- [ ] A CLI tool pushed to GitHub that:
  - Accepts a user question and a block of text as input
  - Calls the OpenAI or Anthropic API
  - Returns a structured JSON answer with citations from the text
  - Handles errors and rate limits gracefully

---

## Phase 4 — RAG & LLM Application Frameworks
`Weeks 13–18` &nbsp; `~90 hrs`

**Goal:** Master RAG. This is the **single most in-demand LLM skill in the industry today.** Nearly every enterprise AI application is a RAG system of some kind. This phase is the core of your market value.

<details>
<summary><strong>What is RAG? (click to expand)</strong></summary>

**RAG = Retrieval-Augmented Generation**

Instead of asking the LLM to "know" your data, you:
1. Chunk your documents into smaller pieces
2. Convert chunks to vector embeddings and store in a vector database
3. At query time, find the most relevant chunks via similarity search
4. Inject those chunks into the LLM prompt as context
5. LLM answers using your retrieved data + its general knowledge

**Result:** LLM answers questions about YOUR documents accurately and with sources.

</details>

### Topics
- Document loading and chunking strategies
- Embedding models: `text-embedding-3-small`, open-source alternatives
- Vector databases: **Chroma** (local, free), **Pinecone** (free tier cloud)
- Similarity search: cosine similarity, ANN algorithms
- **LangChain**: chains, prompts, retrievers, memory, document loaders
- **LlamaIndex**: alternative framework, different philosophy
- Advanced RAG: hybrid search, reranking, query transformation, HyDE
- RAG evaluation: **RAGAS** framework — measuring if your RAG actually works
- Caching strategies and cost reduction patterns

### Resources

| # | Resource | Cost | Time | Notes |
|---|---|---|---|---|
| 1 | [DeepLearning.AI — LangChain for LLM Application Development](https://www.deeplearning.ai/short-courses/langchain-for-llm-application-development/) | Free | ~3 hrs | Start here for LangChain foundations |
| 2 | [DeepLearning.AI — Building and Evaluating Advanced RAG](https://www.deeplearning.ai/short-courses/building-evaluating-advanced-rag/) | Free | ~2.5 hrs | ⚠️ **CRITICAL — do not skip.** Evaluation separates toy RAG from production RAG. |
| 3 | [LangChain Official Docs — RAG Tutorial](https://python.langchain.com/docs/introduction/) | Free | ~3 hrs | Follow the RAG tutorial end-to-end |
| 4 | [LlamaIndex Starter Tutorial](https://docs.llamaindex.ai/en/stable/getting_started/starter_example/) | Free | ~2 hrs | LlamaIndex excels at document ingestion; learn both frameworks |
| 5 | [RAGAS Evaluation Framework](https://docs.ragas.io/) | Free | ~2 hrs | Measures faithfulness, answer relevancy, context precision |

### Week-by-Week
| Week | Focus |
|---|---|
| 13 | LangChain DeepLearning.AI course + LangChain docs basics |
| 14 | Vector databases — Chroma setup, indexing, retrieval experiments |
| 15 | Advanced RAG course + reranking + retrieval patterns |
| 16 | LlamaIndex tutorial + compare to LangChain approach |
| 17 | RAGAS evaluation setup + measure your own RAG outputs |
| 18 | Project build and polish |

### ✅ Milestone — Portfolio Project
- [ ] A RAG application on GitHub with a detailed README:
  - FastAPI endpoint accepting a natural language question
  - Ingests a folder of PDF/text files
  - Stores embeddings in ChromaDB
  - Retrieves relevant chunks and generates an answer with source citations
  - RAGAS evaluation report showing performance metrics
  - Architecture diagram in the README

> This directly replicates a real enterprise production pattern.

---

## Phase 5 — AI Agents & Advanced Patterns
`Weeks 19–23` &nbsp; `~80 hrs`

**Goal:** Understand and build AI agents — LLMs that plan, use tools, and take multi-step actions. This is the frontier of what is being built in products today.

<details>
<summary><strong>What is an Agent? (click to expand)</strong></summary>

An agent is an LLM in a loop:
1. Given a goal, the LLM decides what action to take
2. It calls a **tool** (web search, code execution, database query, API call)
3. It observes the result
4. It decides the next action
5. Repeat until the goal is achieved

**ReAct** (Reason + Act) is the core pattern. **LangGraph** is the current industry-standard framework.

</details>

### Topics
- ReAct pattern: how agents reason and act in a loop
- Tool use: defining tools, parsing LLM tool calls, executing, returning results
- **LangGraph**: stateful graph-based agent orchestration
- Multi-agent systems: multiple specialized agents collaborating
- Agent memory: short-term (conversation), long-term (vector store), episodic
- Guardrails: validating and constraining LLM outputs
- Structured output: Pydantic models + **Instructor** library
- Observability: tracing every LLM call with **LangSmith**

### Resources

| # | Resource | Cost | Time | Notes |
|---|---|---|---|---|
| 1 | [DeepLearning.AI — AI Agents in LangGraph](https://www.deeplearning.ai/short-courses/ai-agents-in-langgraph/) | Free | ~4 hrs | **Start here.** Best introduction to LangGraph and agent patterns. |
| 2 | [DeepLearning.AI — Multi AI Agent Systems with crewAI](https://www.deeplearning.ai/short-courses/multi-ai-agent-systems-with-crewai/) | Free | ~3 hrs | |
| 3 | [LangGraph Official Docs](https://langchain-ai.github.io/langgraph/) | Free | ~4 hrs | Work through the tutorials section completely |
| 4 | [Instructor Library](https://python.useinstructor.com/) | Free | ~2 hrs | Pydantic-enforced structured outputs. Very commonly used in production. |
| 5 | [LangSmith](https://www.langsmith.com/) | Free tier | 30 min setup | Set up NOW. Trace every LLM call from this point forward. Debugging agents without tracing is impossible. |

### Week-by-Week
| Week | Focus |
|---|---|
| 19 | AI Agents in LangGraph course + LangSmith setup |
| 20 | LangGraph docs tutorials + build first simple agent with 2 tools |
| 21 | Multi-agent systems course + CrewAI experiments |
| 22 | Instructor library + structured output patterns + guardrails |
| 23 | Research agent project build |

### ✅ Milestone — Portfolio Project
- [ ] A research agent on GitHub that:
  - Accepts a research topic as input
  - Uses web search as a tool ([Tavily API](https://tavily.com/) — free tier)
  - Summarizes multiple sources
  - Produces a structured report (Pydantic model)
  - Is fully traced in LangSmith (include screenshot in README)
  - Handles failures gracefully (tool errors, LLM refusals)

---

## Phase 6 — Production, LLMOps & Open-Source Models
`Weeks 24–27` &nbsp; `~70 hrs`

**Goal:** Understand how AI applications run in production. This is where your C++ and systems background becomes a **genuine differentiator.** Most application developers skip this layer entirely — you should own it.

### Topics
- Running LLMs locally with **Ollama** — free, no API costs
- **vLLM** — production-grade inference server (heavily C++ under the hood)
- LLM cost optimization: prompt caching, batching, model routing
- Model routing: small model first, escalate to large model only when needed
- LLMOps: monitoring, logging, cost dashboards, drift detection
- System design for AI: RAG vs fine-tuning vs agents — decision framework
- Latency vs cost vs quality — the core production tradeoff triangle
- Cloud AI services overview: AWS Bedrock, GCP Vertex AI, Azure OpenAI

### Resources

| # | Resource | Cost | Time | Notes |
|---|---|---|---|---|
| 1 | [Ollama](https://ollama.com/) | Free | 15 min setup | Run Llama, Mistral, Qwen locally. No API costs. Swap into existing projects. |
| 2 | [vLLM Docs](https://docs.vllm.ai/) | Free | ~4 hrs | Read architecture docs. Production-scale inference. C++ inside. |
| 3 | **LLM Engineer's Handbook** — Iusztin & Labonne (2024) — [Amazon](https://www.amazon.com/LLM-Engineers-Handbook-engineering-production/dp/1836200072) | ~$40 | Book | THE most complete production-focused LLM book. Check O'Reilly/Safari first — your employer may provide free access. **Worth the spend.** |
| 4 | [DeepLearning.AI — LLMOps](https://www.deeplearning.ai/short-courses/llmops/) | Free | ~1.5 hrs | |
| 5 | [Chip Huyen — LLM Engineering Articles](https://huyenchip.com/2023/04/11/llm-engineering.html) | Free | ~2 hrs | Excellent systems-thinking approach. Trust her analysis. |

### 🔗 C++ Leverage Opportunities
> Browse open issues on these repos. **You will understand them.** A merged PR here is an exceptional portfolio item.
> - [`llama.cpp` issues](https://github.com/ggerganov/llama.cpp/issues)
> - [`vLLM` issues](https://github.com/vllm-project/vllm/issues)

### Week-by-Week
| Week | Focus |
|---|---|
| 24 | Ollama setup + run models locally + swap into existing projects |
| 25 | vLLM docs + architecture deep dive + run production inference locally |
| 26 | LLMOps course + cost optimization patterns + monitoring setup |
| 27 | System design study (LLM Engineer's Handbook + Chip Huyen) + capstone start |

---

## 🏆 Capstone Project
`Weeks 27–28`

Choose **one** and build it to portfolio quality. Polish the README, add architecture diagrams, document design decisions, and be ready to talk through it in interviews.

<details>
<summary><strong>Option A — Code Review Assistant</strong> ⭐ Recommended for your profile</summary>

| Field | Detail |
|---|---|
| **What** | A RAG + agent system that ingests your codebase and style guide, then reviews code changes and suggests improvements |
| **Stack** | LangGraph agent + ChromaDB + FastAPI + LangSmith tracing |
| **Why** | Directly relevant to your C++ work. Concrete business value. You can demo it on your own actual code. |

</details>

<details>
<summary><strong>Option B — Local AI Developer Assistant</strong></summary>

| Field | Detail |
|---|---|
| **What** | A fully local (zero API cost) AI assistant using Ollama + RAG over technical documentation |
| **Stack** | Ollama + LlamaIndex + FastAPI + Chroma (all local, no external APIs) |
| **Why** | Demonstrates privacy-aware architecture and infra depth. Shows you can deploy AI without depending on cloud APIs. |

</details>

<details>
<summary><strong>Option C — Enterprise Document Q&A Platform</strong></summary>

| Field | Detail |
|---|---|
| **What** | A multi-tenant RAG app with user auth, per-user document collections, usage tracking, and a simple frontend |
| **Stack** | LangChain RAG + FastAPI + ChromaDB + LangSmith + basic HTML frontend |
| **Why** | Demonstrates production patterns: auth, multi-tenancy, observability. Most directly mirrors what enterprise clients buy. |

</details>

---

## 📋 Portfolio Checklist

### GitHub Repos (public)
- [ ] **Phase 1** — FastAPI app containerized in Docker
- [ ] **Phase 3** — Structured output CLI tool (LLM API + JSON responses)
- [ ] **Phase 4** — RAG application with RAGAS evaluation report
- [ ] **Phase 5** — Multi-step research agent with LangSmith traces
- [ ] **Capstone** — One polished, well-documented flagship project

### Skills You Can Demonstrate
- [ ] Explain transformer architecture and attention mechanism clearly
- [ ] Build a RAG pipeline from scratch without tutorials
- [ ] Design and build a multi-step LLM agent
- [ ] Evaluate whether an LLM application is actually working (RAGAS)
- [ ] Run LLMs locally via Ollama and articulate the tradeoffs vs API
- [ ] Articulate latency / cost / quality tradeoffs in production AI systems
- [ ] Read `vLLM` and `llama.cpp` code and understand the design decisions

### Interview Questions You Will Be Able To Answer
- [ ] *"Walk me through how RAG works"*
- [ ] *"When would you fine-tune vs use RAG vs prompting?"*
- [ ] *"How do you evaluate an LLM application?"*
- [ ] *"How would you reduce costs in production?"*
- [ ] *"What is an agent and when does the pattern make sense?"*
- [ ] *"How would you handle hallucinations in a production system?"*

---

## 📚 Full Resource Master List

### Free Courses (DeepLearning.AI)
| Course | Link |
|---|---|
| ChatGPT Prompt Engineering for Developers | [link](https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/) |
| Building Systems with the ChatGPT API | [link](https://www.deeplearning.ai/short-courses/building-systems-with-chatgpt/) |
| LangChain for LLM Application Development | [link](https://www.deeplearning.ai/short-courses/langchain-for-llm-application-development/) |
| Building and Evaluating Advanced RAG | [link](https://www.deeplearning.ai/short-courses/building-evaluating-advanced-rag/) |
| AI Agents in LangGraph | [link](https://www.deeplearning.ai/short-courses/ai-agents-in-langgraph/) |
| Multi AI Agent Systems with crewAI | [link](https://www.deeplearning.ai/short-courses/multi-ai-agent-systems-with-crewai/) |
| LLMOps | [link](https://www.deeplearning.ai/short-courses/llmops/) |

### Free Video Content
| Resource | Link |
|---|---|
| 3Blue1Brown — Neural Networks | [YouTube](https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi) |
| Andrej Karpathy — Neural Networks: Zero to Hero | [YouTube](https://www.youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ) |

### Free Written Resources
| Resource | Link |
|---|---|
| Automate the Boring Stuff with Python | [automatetheboringstuff.com](https://automatetheboringstuff.com/) |
| Real Python | [realpython.com](https://realpython.com/) |
| FastAPI Official Tutorial | [fastapi.tiangolo.com](https://fastapi.tiangolo.com/tutorial/) |
| Docker Getting Started | [docs.docker.com](https://docs.docker.com/get-started/) |
| The Illustrated Transformer | [jalammar.github.io](https://jalammar.github.io/illustrated-transformer/) |
| fast.ai Practical Deep Learning | [course.fast.ai](https://course.fast.ai/) |
| Anthropic Prompt Engineering Guide | [docs.anthropic.com](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview) |
| OpenAI Cookbook | [github.com/openai](https://github.com/openai/openai-cookbook) |
| LangChain Docs | [python.langchain.com](https://python.langchain.com/docs/introduction/) |
| LlamaIndex Starter Tutorial | [docs.llamaindex.ai](https://docs.llamaindex.ai/en/stable/getting_started/starter_example/) |
| RAGAS Docs | [docs.ragas.io](https://docs.ragas.io/) |
| LangGraph Docs | [langchain-ai.github.io](https://langchain-ai.github.io/langgraph/) |
| Instructor Library | [python.useinstructor.com](https://python.useinstructor.com/) |
| Ollama | [ollama.com](https://ollama.com/) |
| vLLM Docs | [docs.vllm.ai](https://docs.vllm.ai/) |
| Chip Huyen — LLM Engineering | [huyenchip.com](https://huyenchip.com/2023/04/11/llm-engineering.html) |
| llama.cpp GitHub | [github.com](https://github.com/ggerganov/llama.cpp) |

### Tools & Platforms
| Tool | Purpose | Cost | Link |
|---|---|---|---|
| LangSmith | Observability & tracing | Free tier | [langsmith.com](https://www.langsmith.com/) |
| Tavily Search API | Agent web search tool | Free tier | [tavily.com](https://tavily.com/) |
| Chroma | Local vector database | Free | [trychroma.com](https://www.trychroma.com/) |
| Pinecone | Cloud vector database | Free tier | [pinecone.io](https://www.pinecone.io/) |
| OpenAI API | LLM API | Pay-per-use | [platform.openai.com](https://platform.openai.com/) |
| Anthropic API | LLM API | Pay-per-use | [console.anthropic.com](https://console.anthropic.com/) |

### Paid Resource (Optional but Recommended)
| Resource | Cost | Link |
|---|---|---|
| LLM Engineer's Handbook — Iusztin & Labonne (2024) | ~$40 (check O'Reilly first) | [Amazon](https://www.amazon.com/LLM-Engineers-Handbook-engineering-production/dp/1836200072) |

---

## 💰 Estimated Spend Summary

| Item | Cost |
|---|---|
| OpenAI API credits | $5–10 |
| Anthropic API credits | $5–10 |
| LLM Engineer's Handbook (optional) | $0–40 |
| **Total** | **$10–60** |

> Everything else on this roadmap is completely free.

---

## 📅 Weekly Progress Tracker

| Week | Focus | Phase | Done |
|---|---|---|---|
| 1 | Python fundamentals — OOP, types, comprehensions | 1 | - [ ] |
| 2 | Python async, decorators, environment tooling | 1 | - [ ] |
| 3 | FastAPI tutorial end-to-end | 1 | - [ ] |
| 4 | Docker + containerize FastAPI app — **MILESTONE 1** | 1 | - [ ] |
| 5 | 3Blue1Brown neural networks + llama.cpp exploration | 2 | - [ ] |
| 6 | Karpathy videos 1–2 + Illustrated Transformer | 2 | - [ ] |
| 7 | Karpathy videos 3–4 | 2 | - [ ] |
| 8 | fast.ai Lessons 1–3 — **MILESTONE 2** | 2 | - [ ] |
| 9 | API account setup + prompt engineering course | 3 | - [ ] |
| 10 | Anthropic guide + structured outputs + function calling | 3 | - [ ] |
| 11 | Embeddings + OpenAI Cookbook experiments | 3 | - [ ] |
| 12 | Building Systems course + CLI project — **MILESTONE 3** | 3 | - [ ] |
| 13 | LangChain fundamentals | 4 | - [ ] |
| 14 | Vector databases + ChromaDB setup + retrieval | 4 | - [ ] |
| 15 | Advanced RAG course + reranking patterns | 4 | - [ ] |
| 16 | LlamaIndex tutorial | 4 | - [ ] |
| 17 | RAGAS evaluation setup + measure outputs | 4 | - [ ] |
| 18 | RAG project build and polish — **MILESTONE 4** | 4 | - [ ] |
| 19 | Agents in LangGraph course + LangSmith setup | 5 | - [ ] |
| 20 | LangGraph tutorials + first working agent | 5 | - [ ] |
| 21 | Multi-agent systems course + CrewAI | 5 | - [ ] |
| 22 | Instructor library + structured output + guardrails | 5 | - [ ] |
| 23 | Research agent project — **MILESTONE 5** | 5 | - [ ] |
| 24 | Ollama setup + run local models | 6 | - [ ] |
| 25 | vLLM architecture + local production inference | 6 | - [ ] |
| 26 | LLMOps course + cost/monitoring patterns | 6 | - [ ] |
| 27 | System design study + capstone start | 6 | - [ ] |
| 28 | Capstone project finish and polish — **MILESTONE 6 ✅** | Capstone | - [ ] |

---

## 📝 Notes

- **If a week slips, do not skip content.** Slow down, finish it, then continue.
- **API costs:** Use `gpt-4o-mini` and `claude-haiku` for all experiments. Use larger models only when quality actually matters.
- **Local models via Ollama** can replace API calls in Phases 4–6 to cut costs to zero.
- **Do not optimize or refactor early projects.** Build forward. Polish only the capstone.
- **Every project** should be on GitHub from day one, updated as you go.
- **Post about what you're building on LinkedIn.** Visibility compounds over months.
