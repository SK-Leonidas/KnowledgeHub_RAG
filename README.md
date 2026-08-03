# 📚 KnowledgeHub_RAG

> Building a Retrieval-Augmented Generation (RAG) system from scratch — one version at a time.

KnowledgeHub_RAG is a hands-on project documenting the evolution of a Retrieval-Augmented Generation (RAG) system. Rather than building one large application, this repository demonstrates how a simple document question-answering pipeline gradually evolves into a production-ready knowledge assistant.

Each version introduces **one major capability**, making the repository a learning journey through modern RAG architecture.

---

# 🚀 Current Progress

| Version | Status | Description |
|----------|--------|-------------|
| v0.1 | ✅ Completed | Basic Multi-Document RAG |
| v0.2 | ✅ Completed | FAISS Vector Search |
| v0.3 | ✅ Completed | Metadata-Aware Retrieval |
| v0.4 | ✅ Completed | Hybrid Retrieval (FAISS + BM25) |
| v0.5 | 🚧 Next | Cross-Encoder Re-ranking |
| v0.6 | ⏳ Planned | Conversational Memory |
| v0.7 | ⏳ Planned | Streamlit Interface |
| v0.8 | ⏳ Planned | FastAPI Backend |
| v0.9 | ⏳ Planned | Multi-format Document Support |
| v1.0 | 🎯 Goal | Production-ready Knowledge Assistant |

---

# 📖 Version History

---

## ✅ v0.1 — Basic Multi-Document RAG

### Features

- Load multiple PDF documents
- Extract text using PyPDF
- Paragraph-aware chunking
- SentenceTransformer embeddings
- Cosine similarity retrieval using NumPy
- Basic Question Answering pipeline

### Technologies

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
- Similarity scoring
- Vector index persistence

---

## ✅ v0.3 — Metadata-Aware Retrieval

### Improvements

- Page-aware PDF loading
- Metadata-rich chunks
- Document names
- Page numbers
- Chunk IDs
- Source attribution
- Improved retrieval display

Example output:

```
Document
Page
Chunk ID
Similarity Score
Retrieved Chunk
```

---

## ✅ v0.4 — Hybrid Retrieval

### Improvements

- BM25 keyword retrieval
- FAISS semantic retrieval
- Hybrid score fusion
- Normalized scoring
- Semantic score display
- BM25 score display
- Hybrid score display

Example output:

```
Semantic Score
BM25 Score
Hybrid Score
```

---

# 🏗️ Repository Structure

```
KnowledgeHub_RAG/

├── data/
│
├── docs/
│
├── notebooks/
│   ├── KnowledgeHub_RAG_v0.1.ipynb
│   ├── KnowledgeHub_RAG_v0.2.ipynb
│   ├── KnowledgeHub_RAG_v0.3.ipynb
│   └── KnowledgeHub_RAG_v0.4.ipynb
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

# 🛠️ Technologies Used

- Python
- Google Colab
- PyPDF
- SentenceTransformers
- Hugging Face Transformers
- FAISS
- BM25
- NumPy

---

# 🧠 RAG Evolution

```
PDF Documents
      │
      ▼
Chunking
      │
      ▼
Embeddings
      │
      ▼
FAISS
      │
      ▼
Metadata
      │
      ▼
Hybrid Search
      │
      ▼
Cross Encoder
      │
      ▼
Knowledge Assistant
```

---

# 🎯 Learning Goals

This repository explores the major building blocks of Retrieval-Augmented Generation systems.

- Document ingestion
- Chunking strategies
- Embeddings
- Semantic Search
- FAISS
- Metadata
- Hybrid Search
- Re-ranking
- Retrieval pipelines
- Production deployment

---

# 🚀 Upcoming Version

## v0.5 — Cross-Encoder Re-ranking

Planned improvements:

- Re-rank retrieved chunks using a Cross-Encoder
- Improve answer quality
- Better query-passage relevance
- Production-style retrieval pipeline

---

# 🌟 Future Roadmap

- Conversational Memory
- Streamlit UI
- FastAPI Backend
- Multi-format document support
- Production deployment
- Knowledge Assistant v1.0

---

# 👨‍💻 Author

**Surendaranath Kanniyappan**

Building Retrieval-Augmented Generation systems from scratch while documenting every engineering milestone.
