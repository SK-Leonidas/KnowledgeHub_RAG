# KnowledgeHub RAG v0.6.3 – Confidence-Gated RAG with a Stronger LLM

## Objective

v0.6.3 improves the reliability of the RAG pipeline by addressing two major limitations identified during the v0.6.2 evaluation.

The first improvement replaces TinyLlama with a stronger instruction-tuned language model (**Qwen2.5-3B-Instruct**) to improve grounded answer generation.

The second introduces a **retrieval-confidence gate** that prevents the language model from answering questions when insufficient supporting evidence has been retrieved. Instead of relying solely on prompt instructions to avoid hallucinations, the system now decides whether to answer before the LLM is invoked.

The conversational retrieval pipeline introduced in earlier versions remains unchanged.

---

## What Changed in this Version

### LLM Improvements

- Replaced **TinyLlama-1.1B-Chat** with **Qwen2.5-3B-Instruct**
- Switched from raw prompt completion to **chat-template prompting**
- Improved instruction following and grounded answer generation
- Fixed generation decoding by decoding only newly generated tokens

### Hallucination Reduction

- Added a **retrieval-confidence gate**
- Questions with insufficient retrieval confidence bypass the LLM entirely
- Unsupported questions now return the standard document-not-found response
- Hallucination prevention is no longer dependent on prompt compliance

### Confidence Calibration

- Added confidence-score analysis using the existing gold evaluation dataset
- Visualises confidence distributions for answerable and unanswerable questions
- Enables empirical selection of the confidence threshold instead of manual tuning

### Pipeline Integration

- Interactive QA now uses the confidence-gated pipeline
- `evaluate_rag()` also evaluates the complete confidence-gated workflow
- Gold-set evaluation now measures both retrieval quality and refusal behaviour

### Preserved from v0.6.2

- Gold evaluation framework
- Conversation memory
- Follow-up question handling
- Query expansion
- FAISS semantic retrieval
- BM25 lexical retrieval
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
Context Expansion
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
```

---

## Why this Version Matters

The v0.6.2 evaluation highlighted that prompt engineering alone was insufficient to prevent hallucinations. Even when explicitly instructed not to guess, the language model occasionally generated unsupported information for questions whose answers were absent from the document.

v0.6.3 moves hallucination control outside the language model by introducing retrieval-confidence gating. The decision to answer is now based on retrieval evidence rather than model behaviour, resulting in a more reliable and explainable RAG pipeline.

Replacing TinyLlama with Qwen2.5-3B-Instruct also significantly improves instruction following and answer quality while preserving the existing retrieval architecture.

---

## Current Limitations

- Confidence threshold is a single global value.
- Evaluation remains focused on a single PDF document.
- Retrieval confidence is based on retrieval scores only and does not incorporate generation uncertainty.
- Notebook-based implementation without a user interface.

---

## Next Version (v0.7)

- Streamlit web application
- Upload-your-own PDF interface
- Persistent document indexing
- Improved user experience
- Session-based document management

---

## Version

**KnowledgeHub RAG v0.6.3**

---

## Author

**Surendaranath Kanniyappan**

GitHub: https://github.com/SK-Leonidas

Building Retrieval-Augmented Generation systems from scratch while documenting every engineering milestone.