---
title: LangChain – Complete Subject Guideline (Obsidian Edition)
alias:
  - LangChain Guide
  - LangChain Mastery Vault
  - LangChain Textbook
type: MOC
subject: LangChain
status: complete
difficulty: Intermediate → Advanced
created: 2025-11-24
updated: 2025-11-24
cssclass: langchain-guide, wide-table, clean-embed
banner: https://raw.githubusercontent.com/langchain-ai/langchain/master/docs/static/img/langchain_banner.png
banner_y: 0.6
tags:
  - langchain
  - llm
  - rag
  - agents
  - lc-el
  - langgraph
  - langserve
  - python
  - ai-engineering
  - second-brain
  - moc
  - evergreen
mastery-goal: Build production-grade RAG + Agent systems autonomously
links:
  - "[[AI Engineering Hub]]"
  - "[[LLM Concepts]]"
  - "[[Prompt Engineering Vault]]"
  - "[[RAG Mastery]]"
  - "[[Python for AI]]"
  - "[[Vector Databases]]"
category: Framework
priority: P0
recommended-plugins:
  - Dataview
  - Tasks
  - Excalidraw
  - Style Settings
  - Advanced Tables
  - Templater
next-steps:
  - Create individual notes for every [[Concept]]
  - Build 30-day LangChain Mastery Plan
  - Link this MOC to your daily notes template
  - Generate printable PDF version
---
> [!quote] Voltaire
> **“Don’t let the perfect be the enemy of the good.”**

## Chapter 1 — Introduction to LangChain
LangChain provides a modular framework for building LLM applications by combining prompts, models, memory, tools, and retrieval into structured, maintainable systems.

| Concept                         | Brief Description (15–25 words)                                                                       |
| ------------------------------- | ----------------------------------------------------------------------------------------------------- |
| [[What is LangChain]]           | A framework that simplifies LLM-based application development using modular, composable components.   |
| [[Why LangChain Exists]]        | Helps manage complexity in prompt usage, state, tools, and retrieval for production-grade AI systems. |
| [[LangChain Ecosystem]]         | Sub-libraries like [[LCEL]], [[LangGraph]], and [[LangServe]] that expand LangChain’s capabilities.   |
| [[When to Use LangChain]]       | Best suited for apps requiring structure, memory, retrieval, or multi-step reasoning.                 |
| [[LangChain Base Architecture]] | The standard flow of data through prompts, models, parsers, chains, and outputs.                      |

## Chapter 2 — Core Concepts & Terminology
This chapter establishes the essential vocabulary required to understand LangChain’s architecture from day one.

| **Concept**                | **Brief Description (15–25 words)**                                                                                                                                        |
| -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **[[PromptTemplates]]**    | A structured template that standardizes how text inputs are framed, ensuring consistent prompts, predictable formatting, and easier dynamic variable injection at runtime. |
| **[[Messages]]**           | Role-based message objects (system, user, assistant) that model conversational state and allow multi-turn dialogue to behave predictably across complex interactions.      |
| **[[LLMs & Chat Models]]** | Unified interfaces that wrap different model providers, enabling generation, reasoning, and dialogue with a consistent API regardless of underlying model architecture.    |
| [[@Output Parsers]]        | Components that transform unstructured model output into structured formats—JSON, lists, objects—ensuring downstream systems receive clean, machine-usable data.           |
| **[[Chains]]**             | Modular execution pipelines that link prompts, models, and processors into a single callable unit, making complex workflows reproducible and maintainable.                 |
| **Tools**                  | External capabilities—APIs, functions, utilities—that a model can call to perform real actions beyond text generation, often used by agentic systems.                      |
| **Memory**                 | Mechanisms that retain conversation or state across interactions, supporting long-context reasoning, personalization, and multi-step task continuity.                      |
| **Vectorstores**           | Databases that store numerical embeddings for semantic search, enabling high-quality retrieval in RAG and knowledge-grounded applications.                                 |
| **Agents**                 | Reasoning systems that autonomously plan actions, select tools, execute steps, and adapt based on intermediate results, making applications more flexible and dynamic.     |
## Chapter 3 — Prompting Foundations
Mastering prompts is central to effective LLM use. Explore structure, composition, and consistency strategies.

| Concept                          | Brief Description |
|----------------------------------|-------------------|
| [[PromptTemplate Syntax]]        | Defines placeholders, variables, and formatting patterns within prompts. |
| [[ChatPromptTemplate]]           | Multi-message prompts organizing system, user, and assistant content. |
| [[System Instructions]]          | Foundational messages guiding model behavior and tone throughout interactions. |
| [[Template Composition]]         | Combining multiple smaller prompts into maintainable larger templates. |
| [[Parameter Injection]]          | Dynamically filling prompts with external or runtime data values. |
| [[Modular Prompt Blocks]]        | Designing reusable prompt components for consistent workflows. |

## Chapter 4 — Output Parsers & Structured Formatting
Structured outputs ensure reliability. Enforce formats like JSON or schemas for clean consumption.

| Concept                     | Brief Description |
|-----------------------------|-------------------|
| [[BaseOutputParser]]        | Abstract parser class defining how outputs are transformed into structured formats. |
| [[JSON & Dict Parsers]]     | Convert free-text responses into well-formed dictionaries or JSON objects. |
| [[Pydantic Parsers]]        | Enforce strict schema validation using Python models for predictable outputs. |
| [[Dataclass Parsers]]       | Provide simple, type-safe structured responses through Python dataclasses. |
| [[Parser Error Handling]]   | Detect and manage malformed outputs or parsing failures gracefully. |
| [[Fallback Parsing]]        | Secondary parsing strategies for resilience when primary parsing fails. |

## Chapter 5 — Models & Embeddings
How LangChain communicates with LLMs, generates embeddings, and optimizes usage.

| Concept                    | Brief Description |
|----------------------------|-------------------|
| [[Chat Models]]            | Unified abstraction for GPT, Claude, LLaMA, Groq, and other LLM providers. |
| [[Model I/O]]              | Covers streaming, token calculation, batching, and input/output formatting details. |
| [[Embedding Models]]       | Transform text into numerical vectors for semantic retrieval. |
| [[Text Splitters]]         | Break large documents into smaller chunks optimized for embedding. |
| [[Tokenization]]           | Understand token limits, segmentation, and truncation behaviors. |
| [[Cost Optimization]]     | How to choose efficient models and reduce unnecessary API calls. |

## Chapter 6 — Chains & LCEL (LangChain Expression Language)
Chains connect steps. [[LCEL]] makes them elegant, composable, and production-ready.

| Concept                 | Brief Description                                                           |
| ----------------------- | --------------------------------------------------------------------------- |
| [[RunnableSequence]]    | Executes processing steps in a strictly ordered sequence.                   |
| [[RunnableMap]]         | Runs parallel branches of processing for speed or separation of concerns.   |
| [[RunnableBranch]]      | Conditional routing that selects execution paths dynamically.               |
| [[pipe (``) Syntax]]    | Clean operator for connecting runnables (also written as `>` in some docs). |
| [[Streaming Chains]]    | Enable real-time output token streaming from LLMs.                          |
| [[Retries & Fallbacks]] | Build resilience by automatically retrying or re-routing failures.          |

## Chapter 7 — Memory Systems
LLMs lack persistent memory. Explore state management for coherent conversations.

| Concept                   | Brief Description |
|---------------------------|-------------------|
| [[Buffer Memory]]         | Stores entire conversation history for full context retention. |
| [[Window Memory]]         | Limits memory to recent messages to reduce token usage. |
| [[Token Memory]]          | Ensures context stays within a certain token boundary. |
| [[Summary Memory]]        | Automatically summarizes interactions to condense memory. |
| [[Entity Memory]]         | Tracks people, places, or objects across conversations. |
| [[Hybrid Memory Models]]  | Combining multiple memory types for robust performance. |

## Chapter 8 — Tools & Agent Tool-Calling
Let agents call real tools safely and effectively.

| Concept                  | Brief Description |
|--------------------------|-------------------|
| [[Tool Schema]]          | Defines how tools accept inputs and return results for model use. |
| [[Tool Execution]]       | Handles execution and validation of tool outputs. |
| [[ReAct Agents]]         | Reasoning pattern mixing thoughts, actions, and observations. |
| [[OpenAI Tool Calling]]  | Modern JSON-based structured tool execution interface. |
| [[Tool Routing]]         | Logic for selecting the correct tool at the right time. |
| [[Tool Safety Checks]]   | Prevent invalid or unsafe tool calls through validations. |

## Chapter 9 — Retrieval-Augmented Generation (RAG)
Combine retrieval + generation for accurate, grounded answers.

| Concept                     | Brief Description |
|-----------------------------|-------------------|
| [[Document Loaders]]        | Extract structured content from PDFs, HTML, markdown, and more. |
| [[Chunking Methods]]        | Split documents for efficient embedding and retrieval. |
| [[Vectorstores]]            | Store and retrieve embeddings using FAISS, Chroma, Pinecone, etc. |
| [[Similarity Search]]       | Find relevant contexts using nearest-neighbor retrieval. |
| [[Compression Retrievers]]  | Reduce irrelevant content before model input. |
| [[Self-Query Retriever]]    | LLM-driven queries automatically select relevant data. |
| [[RAG Pipelines]]           | Complete end-to-end retrieval and generation workflows. |

## Chapter 10 — Agents & LangGraph
Graph-based control flow for reliable multi-step and multi-agent systems.

| Concept                  | Brief Description |
|--------------------------|-------------------|
| [[Agent Planning]]       | Breaking down tasks into actionable reasoning steps. |
| [[Multi-step Reasoning]] | Iterative loops enabling deeper problem solving. |
| [[LangGraph Nodes]]      | Isolated logic blocks representing steps in a workflow. |
| [[LangGraph Edges & Conditions]] | Control flow transitions based on logic or model output. |
| [[Checkpointing]]        | Captures intermediate progress for recovery or iteration. |
| [[Multi-agent Systems]]  | Enables specialized agents to collaborate on tasks. |

## Chapter 11 — Evaluation, Testing & Debugging
Make your systems reliable and observable.

| Concept                  | Brief Description |
|--------------------------|-------------------|
| [[Prompt Evaluation]]    | Score and analyze prompt quality and stability. |
| [[RAG Evaluation]]       | Validate context accuracy and grounding against sources. |
| [[Chain Unit Tests]]     | Ensure reproducible behavior of each pipeline component. |
| [[Observability]]        | Logs, metrics, and traces for understanding runtime behavior. |
| [[Error Patterns]]       | Catalog of common issues and strategies for resolution. |

## Chapter 12 — Deployment & Production Systems
From prototype to scalable API.

| Concept                  | Brief Description |
|--------------------------|-------------------|
| [[LangServe]]            | Framework for deploying LangChain chains as scalable APIs. |
| [[FastAPI + LangChain]]  | Build custom endpoints integrating chains and tools. |
| [[Scaling]]              | Manage concurrency, worker pools, and throughput. |
| [[Vectorstore Syncing]]  | Update embeddings and documents in production. |
| [[Security]]             | Protect API keys and enforce access controls. |
| [[CI/CD]]                | Automate deployment pipelines and rolling updates. |

---

Move step by step, not all at once. Start with one small, high-impact note—your “gold standard”—and let everything else follow that pattern. Keep drafts messy, refine later, and stay focused on *usefulness over perfection*. Break work into atomic notes so progress feels constant. You’re not fighting a war—you’re assembling a toolkit that will make future work effortless. Build smart, stay consistent, and let momentum carry you forward.

---
