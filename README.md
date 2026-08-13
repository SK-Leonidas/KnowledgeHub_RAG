# KnowledgeHub RAG v0.6.4 – Context Assembly Fix & Engineering Hardening

## Objective

v0.6.4 focuses on improving the reliability, efficiency, and maintainability of the RAG system before moving towards a user-facing application.

This release fixes issues discovered during evaluation, improves context construction for answer generation, introduces engineering enhancements such as index persistence and model caching, and prepares the codebase for the upcoming Streamlit application.

The conversational retrieval pipeline, confidence-gated generation, and Qwen2.5 language model introduced in v0.6.3 remain unchanged.

---

## What Changed in this Version

### RAG Pipeline Improvements

- Fixed context assembly so the language model receives context from the top-ranked retrieved documents instead of only neighbouring chunks from the highest-ranked result.
- Improved query expansion by adding aliases and terminology for real gravitational-wave events (e.g. GW170817 and GW190425).
- Added an author-name diagnostic utility to distinguish PDF extraction issues from generation errors.

### Performance Improvements

- Added persistent FAISS index caching to avoid rebuilding embeddings when source documents remain unchanged.
- Added model caching to prevent reloading embedding and language models during notebook reruns.
- Added end-to-end latency measurement for each question.

### Engineering Improvements

- Generated a pinned `requirements.txt` for reproducible environments.
- Added graceful error handling for answer generation and interactive question answering.
- Improved handling of invalid or empty user input.

### Preserved from v0.6.3

- Qwen2.5-3B-Instruct
- Confidence-gated answer generation
- "Don't Know" response mode
- Gold-set evaluation framework
- Conversation memory
- Follow-up question handling
- FAISS semantic retrieval
- BM25 lexical retrieval
- Query expansion
- Weighted score fusion
- Reciprocal Rank Fusion (RRF)
- Context expansion

---

## Updated Workflow

```text
User Question
        │
        ▼
Conversation Memory
        │
        ▼
Query Expansion
        │
        ▼
FAISS Semantic Search
        +
BM25 Retrieval
        │
        ▼
Weighted Score Fusion
        │
        ▼
Reciprocal Rank Fusion (RRF)
        │
        ▼
Context Assembly
        │
        ▼
Retrieval Confidence
        │
        ├───────────────┐
        │               │
Confidence ≥ Threshold  Confidence < Threshold
        │               │
        ▼               ▼
Qwen2.5-3B-Instruct     Return
        │               "I could not find that
        ▼                information in the
Grounded Response        provided document."
        │
        ▼
Latency Measurement
```

---

## Why this Version Matters

Earlier releases primarily focused on retrieval quality and hallucination reduction.

v0.6.4 strengthens the engineering foundation of the project by ensuring the language model receives better-assembled context, reducing unnecessary computation through caching, improving robustness with error handling, and introducing reproducible environments.

These improvements prepare the project for migration from an experimental notebook into an interactive application.

---

## Current Limitations

- Evaluation has been performed on a single PDF document.
- Confidence threshold remains a global value.
- Retrieval quality may still vary depending on document structure.
- Notebook-based implementation.

---

## Next Version (v0.7)

- Streamlit web application
- Upload-your-own PDF interface
- Dynamic document ingestion
- Session-based document management
- Interactive user interface

---

## Version

**KnowledgeHub RAG v0.6.4**

---

## Author

**Surendaranath Kanniyappan**

GitHub: https://github.com/SK-Leonidas

Building Retrieval-Augmented Generation systems from scratch while documenting every engineering milestone.