# 📚 KnowledgeHub RAG

> A Retrieval-Augmented Generation (RAG) system that enables intelligent question answering over PDF documents using Hybrid Search and Large Language Models.

![Python](https://img.shields.io/badge/Python-3.11-blue)
![FAISS](https://img.shields.io/badge/FAISS-Vector_Search-green)
![SentenceTransformers](https://img.shields.io/badge/SentenceTransformers-Embeddings-orange)
![TinyLlama](https://img.shields.io/badge/TinyLlama-LLM-purple)
![License](https://img.shields.io/badge/License-MIT-red)

---

## 🚀 Overview

KnowledgeHub RAG is an end-to-end Retrieval-Augmented Generation (RAG) project that retrieves relevant information from PDF documents and generates natural language answers using an instruction-tuned Large Language Model.

The project demonstrates the complete RAG workflow:

```
PDF Documents
      │
      ▼
Document Chunking
      │
      ▼
Sentence Embeddings
      │
      ▼
FAISS Vector Search
      │
      ▼
BM25 Keyword Search
      │
      ▼
Hybrid Retrieval
      │
      ▼
TinyLlama LLM
      │
      ▼
Natural Language Answer
      │
      ▼
Source Attribution
```

---

# ✨ Features

- 📄 Multi-document PDF ingestion
- ✂️ Intelligent text chunking
- 🔍 Semantic search using FAISS
- 🔎 Keyword retrieval using BM25
- ⚖️ Hybrid retrieval scoring
- 🤖 LLM-powered answer generation (TinyLlama)
- 📚 Source attribution with document and page references
- 💬 Interactive question-answering interface

---

# 🛠️ Tech Stack

- Python
- Google Colab
- FAISS
- Sentence Transformers
- rank-bm25
- Hugging Face Transformers
- TinyLlama
- PyTorch

---

# 📂 Project Structure

```
KnowledgeHub_RAG/

│── notebooks/
│     ├── KnowledgeHub_RAG_v0_1.ipynb
│     ├── KnowledgeHub_RAG_v0_2.ipynb
│     ├── KnowledgeHub_RAG_v0_3.ipynb
│     ├── KnowledgeHub_RAG_v0_4.ipynb
│     └── KnowledgeHub_RAG_v0_5.ipynb
│
│── docs/
│
│── src/
│
│── tests/
│
│── requirements.txt
│── README.md
│── LICENSE
│── CHANGELOG.md
```

---

# 📈 Development Roadmap

| Version | Status | Features |
|----------|--------|----------|
| ✅ v0.1 | Completed | Multi-document Semantic Search |
| ✅ v0.2 | Completed | Metadata-aware Retrieval |
| ✅ v0.3 | Completed | Hybrid Search (FAISS + BM25) |
| ✅ v0.4 | Completed | Score Normalisation & Improved Retrieval |
| ✅ v0.5 | Completed | LLM-powered Answer Generation (TinyLlama) |
| 🔜 v0.6 | Planned | Conversation Memory |
| 🔜 v0.7 | Planned | Streamlit Web Application |
| 🔜 v0.8 | Planned | FastAPI Backend |
| 🔜 v0.9 | Planned | Docker Deployment |
| 🎯 v1.0 | Planned | KnowledgeHub Assistant |

---

# 💡 Example

### Question

> What algorithm was used for classification?

### Answer

```
The classification system uses Gradient Boosted Decision Trees (GBDT).

Three classifiers were developed for binary, three-class and four-class
classification of binary neutron star merger remnants.

The models use inspiral parameters such as total mass,
mass ratio, tidal deformability and effective spin.
```

### Sources

- FinalProjectReport.pdf (Page 6)
- FinalProjectReport.pdf (Page 8)
- FinalProjectReport.pdf (Page 9)

---

# 🎯 Current Capabilities

- Multi-document retrieval
- Hybrid semantic and keyword search
- Context-aware answer generation
- Grounded responses
- Source attribution

---

# 🔮 Upcoming Features

- Multi-turn conversation memory
- Streamlit web application
- REST API with FastAPI
- Docker deployment
- Multi-user KnowledgeHub Assistant

---

# 📜 License

Released under the MIT License.

---

# 👨‍💻 Author

**Surendaranath Kanniyappan**
GitHub: https://github.com/SK-Leonidas

Building Retrieval-Augmented Generation systems from scratch while documenting every engineering milestone.
