# KnowledgeHub_RAG

> Building a Retrieval-Augmented Generation (RAG) system from scratch — one engineering milestone at a time.

KnowledgeHub_RAG documents the step-by-step development of a Retrieval-Augmented Generation (RAG) system, beginning with a simple PDF question-answering pipeline and progressively evolving into a production-ready knowledge assistant.

Rather than building everything at once, each version introduces a major architectural improvement, allowing the entire engineering journey to be documented, evaluated, and reproduced.

The project now supports **general-purpose document question answering** using hybrid retrieval, conversational memory, confidence-gated generation, and instruction-tuned Large Language Models.

---

# Current Progress

| Version | Status | Major Milestone |
|----------|--------|-----------------|
| v0.1 | ✅ | Basic PDF Question Answering |
| v0.2 | ✅ | Metadata-aware Retrieval |
| v0.3 | ✅ | Hybrid Retrieval (FAISS + BM25) |
| v0.4 | ✅ | Retrieval Optimisation & Score Fusion |
| v0.5 | ✅ | LLM-powered Answer Generation |
| **v0.6** | ✅ | **Conversational RAG, Gold-Set Evaluation, Confidence-Gated Generation, Engineering Optimisation & Generalised PDF Question Answering** |
| v0.7 | 🚧 Next | Streamlit Web Application |
| v0.8 | ⏳ Planned | FastAPI Backend |
| v0.9 | ⏳ Planned | Docker Deployment |
| v1.0 | 🎯 Goal | KnowledgeHub Assistant |

---

# Repository Highlights

The current system includes:

- Upload-first PDF ingestion
- Intelligent document chunking
- Sentence Transformer embeddings
- FAISS semantic retrieval
- BM25 lexical retrieval
- Hybrid retrieval with Reciprocal Rank Fusion (RRF)
- Query expansion
- Context expansion
- Conversation memory
- Confidence-gated retrieval
- Qwen2.5-3B-Instruct answer generation
- Grounded document question answering
- Source page attribution
- Modular RAG pipeline
- Evaluation framework for retrieval and generation
- Persistent vector index caching
- Streamlit-ready architecture

---

# System Architecture

```text
PDF Upload
      │
      ▼
Text Extraction
      │
      ▼
Chunking
      │
      ▼
Embeddings
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
Retrieval Confidence Gate
      │
      ├───────────────┐
      │               │
High Confidence   Low Confidence
      │               │
      ▼               ▼
Qwen2.5            Don't Know
      │
      ▼
Grounded Answer + Source Pages
```

---

# Repository Structure

```text
KnowledgeHub_RAG/

├── notebooks/
│   ├── KnowledgeHub_RAG_v0.1.ipynb
│   ├── KnowledgeHub_RAG_v0.2.ipynb
│   ├── KnowledgeHub_RAG_v0.3.ipynb
│   ├── KnowledgeHub_RAG_v0.4.ipynb
│   ├── KnowledgeHub_RAG_v0.5.ipynb
│   ├── KnowledgeHub_RAG_v0.6.1.ipynb
│   ├── KnowledgeHub_RAG_v0.6.2.ipynb
│   ├── KnowledgeHub_RAG_v0.6.3.ipynb
│   ├── KnowledgeHub_RAG_v0.6.4.ipynb
│   └── KnowledgeHub_RAG_v0.6.5.ipynb
│
├── documents/
├── README.md
├── requirements.txt
└── LICENSE
```

---

# Technologies Used

### Retrieval

- FAISS
- rank-bm25
- Sentence Transformers
- all-MiniLM-L6-v2

### Language Model

- Qwen2.5-3B-Instruct

### Python

- Python
- PyMuPDF
- Transformers
- Torch
- NumPy
- Pandas

---

# Version Evolution

| Version | Major Contribution |
|----------|-------------------|
| **v0.1** | Basic PDF ingestion and semantic retrieval |
| **v0.2** | Metadata-aware retrieval |
| **v0.3** | Hybrid retrieval using FAISS and BM25 |
| **v0.4** | Score fusion and retrieval optimisation |
| **v0.5** | LLM-powered grounded answer generation |
| **v0.6** | Conversational memory, evaluation framework, confidence-gated generation, engineering improvements, and generalised PDF question answering |

---

# Current Status

The project has evolved from a research-specific notebook into a reusable document question-answering pipeline capable of answering questions over arbitrary uploaded PDF documents.

The next stage focuses on transforming the notebook into an interactive application.

---

# Roadmap

- Streamlit web application
- FastAPI backend
- Docker deployment
- Multi-document retrieval
- Cross-document reasoning
- Production-ready KnowledgeHub Assistant (v1.0)

---

# Author

**Surendaranath Kanniyappan**

Building Retrieval-Augmented Generation systems from scratch while documenting every engineering milestone.