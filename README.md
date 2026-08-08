# KnowledgeHub RAG v0.6.1

A Retrieval-Augmented Generation (RAG) system for intelligent question answering over PDF documents using hybrid retrieval, conversational memory, and TinyLlama.

---

## Overview

KnowledgeHub is a modular Retrieval-Augmented Generation (RAG) system that allows users to upload research papers or PDF documents and ask natural language questions about their contents.

The system combines semantic retrieval, lexical retrieval, ranking fusion, context expansion, conversational memory, and a lightweight Large Language Model to generate grounded answers directly from uploaded documents.

Current Version: **v0.6.1**

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
- Conversational memory
- Multi-turn question answering
- Interactive command-line QA interface

---

## System Architecture

```
User Question
        │
        ▼
Conversation Memory
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
Grounded Conversational Answer
```

---

## Project Structure

```
KnowledgeHub/
│
├── KnowledgeHub_v0.6.1.ipynb
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

The conversational retrieval pipeline consists of the following stages:

1. Conversation Memory
2. Query Expansion
3. Semantic Search (FAISS)
4. BM25 Retrieval
5. Weighted Score Fusion
6. Reciprocal Rank Fusion (RRF)
7. Context Expansion
8. Top-k Context Selection

The retrieved context is then supplied to TinyLlama for grounded conversational answer generation.

---

## Example

**Question**

> What algorithm was used for classification?

**Answer**

> Gradient Boosted Decision Trees (GBDT).

**Follow-up Question**

> What algorithm did he use?

**Answer**

> Gradient Boosted Decision Trees (GBDT).

---

## Current Limitations

- Supports PDF documents only
- Uses a lightweight 1.1B parameter language model
- Single-user notebook implementation
- No persistent vector database
- Conversation memory is available only during the current chat session
- TinyLlama (1.1B) may occasionally generate unsupported details when summarising long contexts
- Out-of-document questions may be answered using the model's pretrained knowledge

---

## Future Work

- Multi-document retrieval
- Cross-document reasoning
- Streaming responses
- Better reranking models
- Metadata-aware retrieval
- Web interface (Streamlit)
- Retrieval confidence threshold
- "Don't Know" response mode
- Automated evaluation framework
- Larger instruction-tuned language models

---

## Version

Current Release

**KnowledgeHub RAG v0.6.1**

---

## Author

**Surendaranath Kanniyappan**

GitHub: https://github.com/SK-Leonidas

Building Retrieval-Augmented Generation systems from scratch while documenting every engineering milestone.**Surendaranath Kanniyappan**
