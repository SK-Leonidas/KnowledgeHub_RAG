# 📚 KnowledgeHub_RAG

> Building a Retrieval-Augmented Generation (RAG) system from scratch — one version at a time.

KnowledgeHub_RAG is a personal learning and engineering project that documents the evolution of a Retrieval-Augmented Generation (RAG) system. Instead of building one large application all at once, this repository demonstrates how a simple RAG pipeline gradually evolves into a production-ready knowledge assistant.

Every version introduces one major improvement while preserving the previous functionality, making the repository a step-by-step journey into modern RAG systems.

---

# 🚀 Current Progress

| Version | Status | Description |
|---------|--------|-------------|
| v0.1 | ✅ Completed | Basic Multi-Document RAG |
| v0.2 | ✅ Completed | FAISS Vector Search |
| v0.3 | ⏳ Planned | Metadata-aware Retrieval & Better Chunking |
| v0.4 | ⏳ Planned | Hybrid Search (BM25 + Semantic Search) |
| v0.5 | ⏳ Planned | Cross-Encoder Re-ranking |
| v0.6 | ⏳ Planned | Streamlit User Interface |
| v0.7 | ⏳ Planned | FastAPI Backend |
| v0.8 | ⏳ Planned | Multi-format Document Support |
| v0.9 | ⏳ Planned | Web Search Integration |
| v1.0 | 🎯 Goal | Production-ready Knowledge Assistant |

---

# 📌 Version History

## ✅ v0.1 — Basic Multi-Document RAG

### Features

- Load multiple PDF documents
- Extract text using PyPDF
- Paragraph-aware chunking
- SentenceTransformer embeddings
- Cosine similarity retrieval using NumPy
- Basic Question Answering pipeline
- Support multiple uploaded documents

### Tech Used

- Python
- Google Colab
- PyPDF
- SentenceTransformers
- Transformers
- NumPy

---

## ✅ v0.2 — FAISS Vector Search

### Improvements

- Replaced NumPy similarity search with FAISS
- Built a FAISS vector index
- Faster semantic retrieval
- Added similarity scores
- Support for saving/loading vector indexes

### Why FAISS?

Traditional cosine similarity compares a query against every embedding individually.

FAISS builds a vector index, making semantic search scalable for much larger document collections while maintaining similar retrieval quality.

---

# 🏗️ Project Structure

```
KnowledgeHub_RAG/

├── docs/
│
├── notebooks/
│   ├── KnowledgeHub_RAG_v0_1.ipynb
│   └── KnowledgeHub_RAG_v0_2.ipynb
│
├── src/
│
├── tests/
│
├── README.md
├── requirements.txt
└── LICENSE
```

---

# 🛠️ Technologies

- Python
- Google Colab
- PyPDF
- SentenceTransformers
- Hugging Face Transformers
- FAISS
- NumPy

---

# 🎯 Project Roadmap

```
Basic RAG
      │
      ▼
FAISS Vector Search
      │
      ▼
Metadata-aware Retrieval
      │
      ▼
Hybrid Search
      │
      ▼
Cross Encoder Re-ranking
      │
      ▼
Streamlit Interface
      │
      ▼
FastAPI Backend
      │
      ▼
Production-ready Knowledge Assistant
```

---

# 📖 Learning Goals

This repository is built to understand and implement the core concepts behind Retrieval-Augmented Generation systems, including:

- Document ingestion
- Text chunking
- Embedding generation
- Vector databases
- Semantic search
- Hybrid retrieval
- Re-ranking
- RAG pipelines
- Production deployment

---

# 📅 Current Status

**Latest Release:** ✅ v0.2

Currently working on:

> **v0.3 — Metadata-aware Retrieval & Better Chunking**

---

## ⭐ Future Scope

By the end of this project, KnowledgeHub_RAG aims to become a complete document intelligence platform capable of:

- Answering questions across multiple documents
- Supporting different document formats
- Fast semantic retrieval
- Metadata-aware search
- Hybrid retrieval
- Modern web interface
- API deployment
- Real-world scalability

---

## 👨‍💻 Author

**Surendaranath Kanniyappan**

Building in public while learning Retrieval-Augmented Generation systems from the ground up.