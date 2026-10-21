
<div align="center">

# ⚖️ Explainable Legal AI for Bangladeshi Traffic Law

**Design and Evaluation of an Explainable Legal AI for Bangladeshi Traffic Law**

Final Year Design Project · Department of CSE · United International University

</div>

---

## Overview

Large Language Models can make legal information easier to reach, but they can also give convincing answers with no reliable evidence behind them. In law, that can mislead people about their rights and duties.

This project builds a **Retrieval-Augmented Generation (RAG)** legal assistant for the **Bangladesh Road Transport Act, 2018**, answering questions in **Bangla** with answers grounded in the statute. It then studies a second question: *when some errors remain, can the interface help users notice them?*

> **Research question:** How do source-traceability and uncertainty-oriented interface designs affect hallucination detection, calibrated reliance, cognitive load, and usability among Bangladeshi users with different levels of legal expertise?

## What we build

1. **Legal corpus:** the Act is cleaned and split into segments that keep section, clause, and page metadata.
2. **Bangla QA dataset:** expert-validated factual, procedural, scenario-based, and edge-case questions linked to statutory provisions.
3. **RAG assistant:** retrieves relevant provisions, then an open-weight LLM (Llama, Qwen, or Gemma) writes a source-grounded answer.
4. **Three web interfaces** on the same backend, so only the presentation changes:

| Treatment | Interface | What the user sees |
|---|---|---|
| **A** | Baseline | A plain chatbot answer |
| **B** | Traceability | Answer plus clickable citations to the exact section, clause, and source text |
| **C** | Explainable | Treatment B plus confidence indicators, uncertainty highlights, and warnings |

## User study

A controlled study with **general users** and **participants with legal knowledge** compares the three interfaces on:

- Hallucination detection and calibrated reliance
- Cognitive workload (NASA-TLX)
- Usability (SUS)

## Planned tech stack

| Area | Tools |
|---|---|
| Backend | Python, PyTorch, Hugging Face Transformers, sentence-transformers (multilingual embeddings) |
| RAG | LangChain or LlamaIndex, FAISS or ChromaDB |
| LLMs | Open-weight models: Llama, Qwen, Gemma |
| API | FastAPI or Flask (REST, JSON, UTF-8) |
| Frontend | HTML5, CSS3, JavaScript (WCAG 2.1 AA) |
| Data and ops | JSON and CSV, Git, Docker |

## Status

Currently at the **FYDP-I** stage: requirements, literature review, and system design are documented. Implementation and the main evaluation come next.

**Roadmap:** requirements and study design → corpus and dataset → RAG backend → interfaces and integration → pilot → main evaluation → analysis and thesis.

<!--
## Team

Supervisor: **Dr. Jannatun Noor Mukta**

| Member | Module |
|---|---|
| Sifatullah | Legal corpus and knowledge base |
| Tasnuba Haque | QA dataset and retrieval pipeline |
| Ibtida Ara | LLM generation and reliability layer |
| Aminul Islam Rifat | Frontend and system integration |
| Ifrat-E-Sarwar Orpa | User study and evaluation |
-->

## Disclaimer

This is an academic research prototype. It is **not legal advice**, and its answers should be checked against the official text of the law.
