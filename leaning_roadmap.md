# AI/LLM Learning Roadmap
# C++ Backend Developer → AI Application Engineer
# Duration: 6–7 Months | 2–3 hrs/day (~400–450 hrs total)
# Last Updated: March 2026

================================================================================
PROFILE & CONTEXT
================================================================================

Background : C++ backend, 2.5 years, legacy systems + migration + optimization
Python     : Basic (can read, written small scripts)
Goal       : LLM application development AND platform/infra understanding
Budget     : Mostly free; ~$10–20 total on API credits acceptable
Schedule   : 2–3 hours/day, 7 days/week (~15–18 hrs/week)

Your C++ background is an ASSET:
- Performance intuition maps directly to LLM inference optimization
- Memory and systems reasoning applies to vector stores, batching, serving
- llama.cpp and vLLM (the dominant inference engines) are C++ codebases
- You will understand production tradeoffs that pure Python developers miss

================================================================================
PHASE 1 — PYTHON SOLIDIFICATION + MODERN TOOLING
Weeks 1–4 | ~60 hrs
================================================================================

GOAL
----
Close the gap between "can read Python" and "can build real things fluently."
Pick up the surrounding modern ecosystem used in every AI project.

TOPICS
------
- Python: OOP, list comprehensions, generators, decorators
- Python: asyncio basics, type hints, virtual environments (venv / uv)
- Tooling: Git branching and PRs (deepen what you know)
- Tooling: Docker fundamentals
- REST APIs: how HTTP actually works, request/response lifecycle
- Framework: FastAPI — build a working REST API

RESOURCES
---------
1. Automate the Boring Stuff with Python
   URL  : https://automatetheboringstuff.com/
   Cost : Free
   Scope: Chapters 1–10 only (~6 hrs)
   Note : Covers practical gaps fast, not academic fluff

2. Real Python — targeted articles
   URL  : https://realpython.com/
   Cost : Free tier
   Read : Articles on OOP, asyncio, type hints (search individually)

3. FastAPI Official Tutorial
   URL  : https://fastapi.tiangolo.com/tutorial/
   Cost : Free
   Time : 4–5 hrs to complete fully
   Note : Best-in-class docs, industry-standard framework for AI APIs

4. Docker Getting Started Guide
   URL  : https://docs.docker.com/get-started/
   Cost : Free
   Time : One weekend (~4 hrs)

WEEK-BY-WEEK BREAKDOWN
----------------------
Week 1 : Python OOP, type hints, comprehensions, generators (Automate Ch 1–5)
Week 2 : asyncio, decorators, venv/uv setup (Automate Ch 6–10 + Real Python)
Week 3 : FastAPI tutorial end-to-end
Week 4 : Docker guide + wire FastAPI app into a container

MILESTONE
---------
[ ] A working FastAPI app containerized in Docker, pushed to a public GitHub repo
    The app should: accept text input via POST request, return a JSON response


================================================================================
PHASE 2 — AI/ML CONCEPTUAL FOUNDATIONS
Weeks 5–8 | ~60 hrs
================================================================================

GOAL
----
Understand what LLMs are, why they work, and how to reason about them.
You do NOT need to become an ML researcher. You need enough understanding
to make good architectural decisions and not be misled by hype.

TOPICS
------
- What neural networks are (intuition + light math, no proofs)
- How transformers work: attention mechanism, tokens, embeddings
- Training vs inference — what happens at each stage
- RLHF — what it is and why it matters for LLM behavior
- Fine-tuning vs prompting vs RAG — when to use each
- How to read model cards and interpret benchmarks

RESOURCES
---------
1. 3Blue1Brown — Neural Networks Series (YouTube)
   URL  : https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi
   Cost : Free
   Time : ~4 hrs
   Note : Best visual intuition available anywhere, no prior math needed

2. Andrej Karpathy — Neural Networks: Zero to Hero (YouTube)
   URL  : https://www.youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ
   Cost : Free
   Time : Watch first 4 videos only (~8 hrs)
   Note : Karpathy was on OpenAI founding team. This is the highest-quality
          free ML education that exists. First 4 videos are enough for Phase 2.

3. The Illustrated Transformer (Blog Post)
   URL  : https://jalammar.github.io/illustrated-transformer/
   Cost : Free
   Time : ~1 hr read
   Note : Makes transformer architecture click visually. Read twice.

4. fast.ai — Practical Deep Learning for Coders
   URL  : https://course.fast.ai/
   Cost : Free
   Scope: Lessons 1–3 only (~6 hrs)
   Note : Top-down practical approach. Matches your experience profile better
          than bottom-up academic courses.

C++ BRIDGE (Do this in Week 5)
------------------------------
Read the llama.cpp GitHub README and skim the Issues tab.
URL: https://github.com/ggerganov/llama.cpp
This is the most widely-used open-source LLM inference engine and it is C++.
You will understand most of the performance decisions being made immediately.
This is also a future open-source contribution path for you.

WEEK-BY-WEEK BREAKDOWN
----------------------
Week 5 : 3Blue1Brown playlist + llama.cpp README
Week 6 : Karpathy first 2 videos + Illustrated Transformer article
Week 7 : Karpathy videos 3–4
Week 8 : fast.ai Lessons 1–3

MILESTONE
---------
[ ] Can explain in plain English:
    - How a transformer processes text (tokens, attention, embeddings)
    - The difference between training and inference
    - What fine-tuning means vs prompting vs RAG
    - Why context window size matters


================================================================================
PHASE 3 — LLM APIs & PROMPT ENGINEERING
Weeks 9–12 | ~65 hrs
================================================================================

GOAL
----
Go hands-on with real LLMs via API. Prompt engineering is a real, learnable
skill and a large percentage of AI application quality comes from it.

TOPICS
------
- OpenAI API fundamentals (industry standard, most widely used)
- Anthropic Claude API fundamentals (second most important)
- System prompts, user prompts, conversation history
- Few-shot prompting, chain-of-thought prompting
- Structured outputs: JSON mode, function calling / tool use
- Tokens, context windows, and cost reasoning
- Embeddings: what they are, how to generate and use them
- Rate limits, retries, error handling

SETUP (Do this at start of Week 9)
-----------------------------------
- Create OpenAI account  : https://platform.openai.com/
- Create Anthropic account: https://console.anthropic.com/
- Load $5–10 onto each account
- These credits will cover ALL experiments in Phase 3 and Phase 4

RESOURCES
---------
1. DeepLearning.AI — ChatGPT Prompt Engineering for Developers
   URL  : https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/
   Cost : Free
   Time : ~1.5 hrs
   Note : Co-created with OpenAI. Start here.

2. Anthropic Prompt Engineering Guide (Official Docs)
   URL  : https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview
   Cost : Free
   Note : Extremely well-written. Read fully, not just skim.

3. OpenAI Cookbook (GitHub)
   URL  : https://github.com/openai/openai-cookbook
   Cost : Free
   Note : Practical recipes you can run immediately. Bookmark and use throughout.

4. DeepLearning.AI — Building Systems with the ChatGPT API
   URL  : https://www.deeplearning.ai/short-courses/building-systems-with-chatgpt/
   Cost : Free
   Time : ~1.5 hrs

WEEK-BY-WEEK BREAKDOWN
----------------------
Week 9  : Account setup + DeepLearning.AI prompt engineering course + basics
Week 10 : Anthropic guide fully + structured outputs / function calling
Week 11 : Embeddings deep dive + OpenAI Cookbook experiments
Week 12 : Building Systems course + project build

MILESTONE
---------
[ ] A CLI tool (pushed to GitHub) that:
    - Accepts a user question and a block of text as input
    - Calls the OpenAI or Anthropic API
    - Returns a structured JSON answer with citations from the text
    - Handles errors and rate limits gracefully


================================================================================
PHASE 4 — RAG & LLM APPLICATION FRAMEWORKS
Weeks 13–18 | ~90 hrs
================================================================================

GOAL
----
Master RAG (Retrieval-Augmented Generation).
This is the single most in-demand LLM skill in the industry today.
Nearly every enterprise AI application is a RAG system of some kind.
This phase is the core of your market value.

WHAT IS RAG
-----------
RAG = Retrieval-Augmented Generation
Instead of asking the LLM to "know" your data, you:
  1. Chunk your documents into smaller pieces
  2. Convert chunks to vector embeddings and store in a vector database
  3. At query time, find the most relevant chunks via similarity search
  4. Inject those chunks into the LLM prompt as context
  5. LLM answers using your retrieved data + its general knowledge
Result: LLM answers questions about YOUR documents accurately and with sources.

TOPICS
------
- Document loading and chunking strategies
- Embedding models: OpenAI text-embedding-3-small, open-source alternatives
- Vector databases: Chroma (local, free), Pinecone (free tier cloud)
- Similarity search: cosine similarity, ANN algorithms
- LangChain: chains, prompts, retrievers, memory, document loaders
- LlamaIndex: alternative framework, different philosophy
- Advanced RAG: hybrid search, reranking, query transformation, HyDE
- RAG evaluation: RAGAS framework — measuring if your RAG actually works
- Caching strategies and cost reduction patterns

RESOURCES
---------
1. DeepLearning.AI — LangChain for LLM Application Development
   URL  : https://www.deeplearning.ai/short-courses/langchain-for-llm-application-development/
   Cost : Free
   Time : ~3 hrs
   Note : Start here for LangChain foundations

2. DeepLearning.AI — Building and Evaluating Advanced RAG
   URL  : https://www.deeplearning.ai/short-courses/building-evaluating-advanced-rag/
   Cost : Free
   Time : ~2.5 hrs
   Note : CRITICAL. Do not skip this. Evaluation is what separates toy RAG
          from production RAG.

3. LangChain Official Docs — RAG Tutorial
   URL  : https://python.langchain.com/docs/introduction/
   Cost : Free
   Note : Follow the RAG tutorial end-to-end on the official site

4. LlamaIndex — Starter Tutorial
   URL  : https://docs.llamaindex.ai/en/stable/getting_started/starter_example/
   Cost : Free
   Time : ~2 hrs
   Note : LlamaIndex excels at document ingestion; LangChain excels at chains/agents
          Learn both — you will encounter both in the industry

5. RAGAS Evaluation Framework
   URL  : https://docs.ragas.io/
   Cost : Free
   Note : Standard RAG evaluation. Measures faithfulness, answer relevancy,
          context precision. Use on your project.

WEEK-BY-WEEK BREAKDOWN
----------------------
Week 13 : LangChain DeepLearning.AI course + LangChain docs basics
Week 14 : Vector databases — Chroma setup, indexing, retrieval experiments
Week 15 : Advanced RAG course (DeepLearning.AI) + reranking + retrieval patterns
Week 16 : LlamaIndex starter tutorial + compare to LangChain approach
Week 17 : RAGAS evaluation setup + measure your own RAG outputs
Week 18 : Project build and polish (see milestone below)

MILESTONE — PORTFOLIO PROJECT
------------------------------
[ ] A RAG application pushed to GitHub with a detailed README that includes:
    - FastAPI endpoint accepting a question
    - Ingests a folder of PDF/text files
    - Stores embeddings in ChromaDB
    - Retrieves relevant chunks and generates an answer with sources
    - RAGAS evaluation report showing performance metrics
    - Architecture diagram or diagram description in README
    This directly replicates a real enterprise production pattern.


================================================================================
PHASE 5 — AI AGENTS & ADVANCED PATTERNS
Weeks 19–23 | ~80 hrs
================================================================================

GOAL
----
Understand and build AI agents — LLMs that plan, use tools, and take
multi-step actions to complete goals. This is the frontier of what is
being built in products today.

WHAT IS AN AGENT
----------------
An agent is an LLM in a loop:
  1. Given a goal, the LLM decides what action to take
  2. It calls a tool (web search, code execution, database query, API call)
  3. It observes the result
  4. It decides the next action
  5. Repeat until goal is achieved
ReAct (Reason + Act) is the core pattern. LangGraph is the standard framework.

TOPICS
------
- ReAct pattern: how agents reason and act in a loop
- Tool use: defining tools, parsing LLM tool calls, executing, returning results
- LangGraph: stateful graph-based agent orchestration (current industry standard)
- Multi-agent systems: multiple specialized agents collaborating
- Agent memory: short-term (conversation), long-term (vector store), episodic
- Guardrails: validating and constraining LLM outputs
- Structured output: Pydantic models + Instructor library
- Observability: tracing every LLM call with LangSmith (free tier)

RESOURCES
---------
1. DeepLearning.AI — AI Agents in LangGraph
   URL  : https://www.deeplearning.ai/short-courses/ai-agents-in-langgraph/
   Cost : Free
   Time : ~4 hrs
   Note : START HERE. Best introduction to LangGraph and agent patterns.

2. DeepLearning.AI — Multi AI Agent Systems with crewAI
   URL  : https://www.deeplearning.ai/short-courses/multi-ai-agent-systems-with-crewai/
   Cost : Free
   Time : ~3 hrs

3. LangGraph Official Docs
   URL  : https://langchain-ai.github.io/langgraph/
   Cost : Free
   Note : Work through the tutorials section completely

4. Instructor Library (Structured LLM Outputs)
   URL  : https://python.useinstructor.com/
   Cost : Free
   Note : Uses Pydantic to enforce structured outputs from any LLM.
          Very commonly used in production. Learn this.

5. LangSmith Observability Platform
   URL  : https://www.langsmith.com/
   Cost : Free tier (generous limits)
   Note : Set up LangSmith NOW and trace every LLM call you make from
          this point forward. Debugging agents without tracing is impossible.

WEEK-BY-WEEK BREAKDOWN
----------------------
Week 19 : AI Agents in LangGraph course + LangSmith setup
Week 20 : LangGraph docs tutorials + build first simple agent with 2 tools
Week 21 : Multi-agent systems course + CrewAI experiments
Week 22 : Instructor library + structured output patterns + guardrails
Week 23 : Project build (see milestone below)

MILESTONE — PORTFOLIO PROJECT
------------------------------
[ ] A research agent pushed to GitHub that:
    - Accepts a research topic as input
    - Uses web search as a tool (Tavily API has free tier)
    - Summarizes multiple sources
    - Produces a structured report (Pydantic model)
    - Is fully traced in LangSmith (include screenshot in README)
    - Handles failures gracefully (tool errors, LLM refusals)


================================================================================
PHASE 6 — PRODUCTION, LLMOPS & OPEN-SOURCE MODELS
Weeks 24–27 | ~70 hrs
================================================================================

GOAL
----
Understand how AI applications run in production. This is where your
C++ and systems background becomes a genuine differentiator.
Most application developers skip this layer. You should own it.

TOPICS
------
- Running LLMs locally with Ollama — free, no API costs
- vLLM — production-grade inference server (heavily C++ under the hood)
- LLM cost optimization: prompt caching, batching, model routing
- Model routing: small model first, escalate to large model only when needed
- LLMOps: monitoring, logging, cost dashboards, drift detection
- System design for AI: RAG vs fine-tuning vs agents — decision framework
- Latency vs cost vs quality — the core production tradeoff triangle
- Cloud AI services overview: AWS Bedrock, GCP Vertex AI, Azure OpenAI

RESOURCES
---------
1. Ollama
   URL  : https://ollama.com/
   Cost : Free
   Time : 15-minute setup
   Note : Pull and run Llama, Mistral, Qwen models locally on your machine.
          No API costs. Swap Ollama for OpenAI in your existing projects.

2. vLLM Documentation
   URL  : https://docs.vllm.ai/
   Cost : Free
   Note : Read the architecture docs and understand the design.
          Run it locally. This is used at production scale in industry.

3. LLM Engineer's Handbook (Book)
   Author: Paul Iusztin & Maxime Labonne (2024)
   URL   : https://www.amazon.com/LLM-Engineers-Handbook-engineering-production/dp/1836200072
   Cost  : ~$40 (check O'Reilly — your employer may provide free access)
   Note  : THE most complete production-focused LLM book available.
           Covers data, training, RAG, serving, MLOps end-to-end.
           This is worth the spend. Check Safari/O'Reilly first.

4. DeepLearning.AI — LLMOps
   URL  : https://www.deeplearning.ai/short-courses/llmops/
   Cost : Free
   Time : ~1.5 hrs

5. Chip Huyen — LLM Engineering Articles
   URL  : https://huyenchip.com/2023/04/11/llm-engineering.html
   Cost : Free
   Note : Excellent systems-thinking approach to LLM architecture decisions.
          Chip wrote the ML Systems Design book. Trust her analysis.

C++ LEVERAGE OPPORTUNITIES
--------------------------
- llama.cpp GitHub issues  : https://github.com/ggerganov/llama.cpp/issues
- vLLM GitHub issues       : https://github.com/vllm-project/vllm/issues
Browse open issues. You will understand them. This is a real contribution path.
A merged PR to llama.cpp or vLLM is an exceptional portfolio item.

WEEK-BY-WEEK BREAKDOWN
----------------------
Week 24 : Ollama setup + run models locally + swap into your existing projects
Week 25 : vLLM docs + architecture deep dive + run production inference locally
Week 26 : LLMOps course + cost optimization patterns + monitoring setup
Week 27 : System design study (LLM Engineer's Handbook + Chip Huyen articles)
          + Capstone project start (see below)


================================================================================
CAPSTONE PROJECT
Weeks 27–28
================================================================================

Choose ONE and build it to portfolio quality. Polish the README, add architecture
diagrams, document design decisions, and be ready to talk through it in interviews.

OPTION A — Code Review Assistant (Recommended for your profile)
---------------------------------------------------------------
What  : A RAG + agent system that ingests your codebase and style guide,
        then reviews code changes and suggests improvements
Stack : LangGraph agent + ChromaDB + FastAPI + LangSmith tracing
Why   : Directly relevant to your C++ work. Concrete business value.
        You can demo it on your own actual code.

OPTION B — Local AI Developer Assistant
----------------------------------------
What  : A fully local (zero API cost) AI assistant using Ollama + RAG
        over technical documentation you choose (e.g., Linux kernel docs,
        company internal docs, CMake docs, etc.)
Stack : Ollama + LlamaIndex + FastAPI + Chroma (all local)
Why   : Demonstrates privacy-aware architecture and infra depth.
        Shows you can deploy AI without depending on external APIs.

OPTION C — Enterprise Document Q&A Platform
--------------------------------------------
What  : A multi-tenant RAG app with user auth, per-user document collections,
        usage tracking, and a simple frontend
Stack : LangChain RAG + FastAPI + ChromaDB + LangSmith + basic HTML frontend
Why   : Demonstrates production patterns: auth, multi-tenancy, observability.
        Most directly mirrors what enterprise clients actually want to buy.


================================================================================
PORTFOLIO CHECKLIST
================================================================================

By end of 6 months, you should have all of the following:

GITHUB REPOS (public)
[ ] Phase 1 : FastAPI app containerized in Docker
[ ] Phase 3 : Structured output CLI tool (LLM API + JSON responses)
[ ] Phase 4 : RAG application with RAGAS evaluation report
[ ] Phase 5 : Multi-step research agent with LangSmith traces
[ ] Capstone : One polished, well-documented flagship project

SKILLS YOU CAN DEMONSTRATE
[ ] Can explain transformer architecture and attention mechanism clearly
[ ] Can build a RAG pipeline from scratch without tutorials
[ ] Can design and build a multi-step LLM agent
[ ] Can evaluate whether an LLM application is working correctly (RAGAS)
[ ] Can run LLMs locally via Ollama and explain the tradeoffs vs API
[ ] Can articulate latency / cost / quality tradeoffs in production AI systems
[ ] Can read vLLM and llama.cpp code and understand the design decisions

INTERVIEW TOPICS YOU WILL BE ABLE TO SPEAK TO
[ ] "Walk me through how RAG works"
[ ] "When would you fine-tune vs use RAG vs prompting?"
[ ] "How do you evaluate an LLM application?"
[ ] "How would you reduce costs in production?"
[ ] "What is an agent and when does the pattern make sense?"
[ ] "How would you handle hallucinations in a production system?"


================================================================================
FULL RESOURCE MASTER LIST
================================================================================

FREE COURSES (DeepLearning.AI — all free)
-----------------------------------------
- ChatGPT Prompt Engineering for Developers
  https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/
- Building Systems with the ChatGPT API
  https://www.deeplearning.ai/short-courses/building-systems-with-chatgpt/
- LangChain for LLM Application Development
  https://www.deeplearning.ai/short-courses/langchain-for-llm-application-development/
- Building and Evaluating Advanced RAG
  https://www.deeplearning.ai/short-courses/building-evaluating-advanced-rag/
- AI Agents in LangGraph
  https://www.deeplearning.ai/short-courses/ai-agents-in-langgraph/
- Multi AI Agent Systems with crewAI
  https://www.deeplearning.ai/short-courses/multi-ai-agent-systems-with-crewai/
- LLMOps
  https://www.deeplearning.ai/short-courses/llmops/

FREE VIDEO CONTENT
------------------
- 3Blue1Brown Neural Networks playlist
  https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi
- Andrej Karpathy — Neural Networks: Zero to Hero
  https://www.youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ

FREE WRITTEN RESOURCES
-----------------------
- Automate the Boring Stuff with Python : https://automatetheboringstuff.com/
- Real Python                           : https://realpython.com/
- FastAPI Tutorial                      : https://fastapi.tiangolo.com/tutorial/
- Docker Getting Started                : https://docs.docker.com/get-started/
- The Illustrated Transformer           : https://jalammar.github.io/illustrated-transformer/
- fast.ai Practical Deep Learning       : https://course.fast.ai/
- Anthropic Prompt Engineering Guide    : https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview
- OpenAI Cookbook                       : https://github.com/openai/openai-cookbook
- LangChain Docs                        : https://python.langchain.com/docs/introduction/
- LlamaIndex Starter Tutorial           : https://docs.llamaindex.ai/en/stable/getting_started/starter_example/
- RAGAS Docs                            : https://docs.ragas.io/
- LangGraph Docs                        : https://langchain-ai.github.io/langgraph/
- Instructor Library                    : https://python.useinstructor.com/
- Ollama                                : https://ollama.com/
- vLLM Docs                             : https://docs.vllm.ai/
- Chip Huyen LLM Engineering            : https://huyenchip.com/2023/04/11/llm-engineering.html
- llama.cpp GitHub                      : https://github.com/ggerganov/llama.cpp

TOOLS & PLATFORMS (all free tier unless noted)
----------------------------------------------
- LangSmith (observability)  : https://www.langsmith.com/
- Tavily Search API (agents) : https://tavily.com/
- Chroma (vector DB, local)  : https://www.trychroma.com/
- Pinecone (vector DB, cloud): https://www.pinecone.io/
- OpenAI API                 : https://platform.openai.com/
- Anthropic API              : https://console.anthropic.com/

PAID RESOURCE (optional but recommended)
-----------------------------------------
- LLM Engineer's Handbook (Iusztin & Labonne, 2024)
  https://www.amazon.com/LLM-Engineers-Handbook-engineering-production/dp/1836200072
  ~$40 or free via O'Reilly/Safari (check employer subscription)


================================================================================
ESTIMATED SPEND SUMMARY
================================================================================

OpenAI API credits  : $5–10    (covers all Phase 3, 4, 5 experiments)
Anthropic API credits: $5–10   (covers Phase 3 experiments)
LLM Engineer's Handbook: $0–40 (optional; check O'Reilly access first)
-------------------------------------------------------------------
TOTAL               : $10–60   (book optional; APIs are the minimum)

Everything else on this roadmap is completely free.


================================================================================
WEEKLY PROGRESS TRACKER
================================================================================

Use this to track completion. Check off each week as you finish it.

[ ] Week 1  — Python fundamentals (OOP, types, comprehensions)
[ ] Week 2  — Python async, decorators, environment tooling
[ ] Week 3  — FastAPI tutorial end-to-end
[ ] Week 4  — Docker + containerize FastAPI app | MILESTONE 1
[ ] Week 5  — 3Blue1Brown neural networks + llama.cpp exploration
[ ] Week 6  — Karpathy videos 1-2 + Illustrated Transformer
[ ] Week 7  — Karpathy videos 3-4
[ ] Week 8  — fast.ai Lessons 1–3 | MILESTONE 2
[ ] Week 9  — API account setup + prompt engineering course
[ ] Week 10 — Anthropic guide + structured outputs + function calling
[ ] Week 11 — Embeddings + OpenAI Cookbook experiments
[ ] Week 12 — Building Systems course + CLI project | MILESTONE 3
[ ] Week 13 — LangChain fundamentals
[ ] Week 14 — Vector databases + ChromaDB setup + retrieval
[ ] Week 15 — Advanced RAG course + reranking patterns
[ ] Week 16 — LlamaIndex tutorial
[ ] Week 17 — RAGAS evaluation setup + measure outputs
[ ] Week 18 — RAG project build and polish | MILESTONE 4
[ ] Week 19 — Agents in LangGraph course + LangSmith setup
[ ] Week 20 — LangGraph tutorials + first working agent
[ ] Week 21 — Multi-agent systems course + CrewAI
[ ] Week 22 — Instructor library + structured output + guardrails
[ ] Week 23 — Research agent project | MILESTONE 5
[ ] Week 24 — Ollama setup + run local models
[ ] Week 25 — vLLM architecture + local production inference
[ ] Week 26 — LLMOps course + cost/monitoring patterns
[ ] Week 27 — System design study + capstone start
[ ] Week 28 — Capstone project finish and polish | MILESTONE 6 (COMPLETE)


================================================================================
NOTES
================================================================================

- If a week slips, do not skip content. Slow down, finish it, then continue.
- API costs: use GPT-4o-mini and Claude Haiku for experiments (cheapest models).
  Use GPT-4o or Claude Sonnet only when quality actually matters.
- Local models via Ollama can replace API calls in Phases 4–6 to cut costs.
- Do not optimize or refactor early projects. Build forward. Polish only capstone.
- Every project should be on GitHub from day one, updated as you go.
- Post about what you're building on LinkedIn. This builds visibility in parallel.