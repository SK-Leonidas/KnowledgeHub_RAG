# Changelog

All notable changes to the KnowledgeHub project are documented in this file.

---

# v0.6.1 — Conversational Retrieval-Augmented Generation

Released: August 2026

## Added

- Conversational memory for multi-turn question answering
- Conversation history integration into prompt construction
- Support for follow-up questions without repeating previous context
- Improved documentation describing current system limitations

## Improved

- Refined TinyLlama prompt for cleaner and more grounded responses
- Improved generation stability through updated model configuration
- Reduced prompt leakage during answer generation
- Improved conversational experience during interactive chat sessions

## Fixed

- Removed unnecessary generation configuration warnings
- Improved answer formatting
- Better handling of conversational follow-up questions

## Known Limitations

- TinyLlama (1.1B) may occasionally generate unsupported details when summarising long contexts
- Out-of-document questions may still be answered using the model's pretrained knowledge
- No retrieval confidence threshold or "Don't Know" response mechanism yet

---

# v0.6 — Enhanced Retrieval-Augmented Generation

Released: August 2026

## Added

- TinyLlama instruction-tuned language model
- End-to-end Retrieval-Augmented Generation (RAG)
- Query expansion for technical and abbreviated queries
- Weighted score fusion before ranking
- Reciprocal Rank Fusion (RRF)
- Context expansion using neighbouring chunks
- Interactive command-line question answering
- Grounded prompt template for answer generation

## Improved

- Retrieval accuracy for technical questions
- Ranking consistency using hybrid retrieval
- Reduced hallucinations through stricter prompt engineering
- Better support for abbreviation-based queries (e.g. GBDT)
- Cleaner modular notebook structure

## Changed

- Retrieval pipeline upgraded from hybrid search to full RAG pipeline
- Prompt instructions rewritten to enforce context-grounded responses
- Retrieval ranking enhanced with weighted fusion before RRF

---

# v0.5 — LLM-Based Answer Generation

## Added

- TinyLlama integration
- Prompt template
- Natural language answer generation
- Interactive QA loop

---

# v0.4 — Hybrid Retrieval

## Added

- FAISS semantic retrieval
- BM25 lexical retrieval
- Hybrid retrieval
- Context expansion

---

# v0.3 — Semantic Search

## Added

- SentenceTransformer embeddings
- FAISS vector index
- Top-k semantic retrieval

---

# v0.2 — Document Processing

## Added

- PDF loading
- Text cleaning
- Intelligent chunking

---

# v0.1 — Initial Prototype

## Added

- Project structure
- Basic PDF parsing
- Initial retrieval experiments