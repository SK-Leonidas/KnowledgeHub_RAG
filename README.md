#KnowledgeHub RAG v0.6

A Retrieval-Augmented Generation (RAG) system for intelligent question answering over PDF documents using hybrid retrieval and TinyLlama.

---

## Overview

KnowledgeHub is a modular Retrieval-Augmented Generation (RAG) system that allows users to upload research papers or PDF documents and ask natural language questions about their contents.

The system combines semantic retrieval, lexical retrieval, ranking fusion, context expansion, and a lightweight Large Language Model to generate grounded answers directly from the uploaded documents.

Current Version: **v0.6**

---

## Features

- PDF document ingestion
- Intelligent document chunking
- Sentence Transformer embeddings
- FAISS semantic search
- BM25 lexical retrieval
- Hybrid retrieval pipeline
- Weighted score fusion
- Reciprocal Rank Fusion (RRF)
- Query expansion
- Context expansion
- TinyLlama-powered answer generation
- Context-grounded responses
- Interactive command-line QA interface

---

## System Architecture

```
User Question
        │
        ▼
Query Expansion
        │
        ▼
Semantic Search (FAISS)
        +
Lexical Search (BM25)
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
TinyLlama
        │
        ▼
Grounded Answer
```

---

## Project Structure

```
KnowledgeHub/
│
├── KnowledgeHub_v0.6.ipynb
├── README.md
├── CHANGELOG.md
├── requirements.txt
├── documents/
│      ├── sample.pdf
│
└── outputs/
```

---

## Technologies Used

### Retrieval

- FAISS
- rank-bm25
- Sentence Transformers
- all-MiniLM-L6-v2

### Language Model

- TinyLlama-1.1B-Chat

### Python Libraries

- transformers
- torch
- PyMuPDF
- numpy
- pandas

---

## Retrieval Pipeline

The retrieval process consists of several stages:

1. Query Expansion
2. Semantic Search (FAISS)
3. BM25 Retrieval
4. Weighted Score Fusion
5. Reciprocal Rank Fusion (RRF)
6. Context Expansion
7. Top-k Context Selection

The retrieved context is then supplied to TinyLlama for grounded answer generation.

---

## Example

Question

> What algorithm was used for classification?

Answer

> Gradient Boosted Decision Trees (GBDT).

---

## Current Limitations

- Supports PDF documents only
- Uses a lightweight 1.1B parameter language model
- Single-user notebook implementation
- No persistent vector database
- No conversational memory across sessions

---

## Future Work

- Multi-document retrieval
- Cross-document reasoning
- Streaming responses
- Better reranking models
- Metadata-aware retrieval
- Web interface
- Conversation memory
- Larger instruction-tuned language models

---

## Version

Current Release

**KnowledgeHub RAG v0.6**

---

## Author

**Surendaranath Kanniyappan**

GitHub: https://github.com/SK-Leonidas

Building Retrieval-Augmented Generation systems from scratch while documenting every engineering milestone.
