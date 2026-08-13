# Changelog

All notable changes to the KnowledgeHub project are documented in this file.

---

# v0.6.5 — Generalized Document Question Answering

Released: August 2026

## Added

- Upload-first PDF ingestion for Google Colab
- Local PDF loading support for Jupyter and VS Code
- Modular `RAGPipeline` class
- Source-page attribution for generated answers
- Streamlit-ready pipeline architecture

## Improved

- Refactored the notebook to remove hidden global dependencies
- Generalized the pipeline to work with arbitrary PDF documents
- Simplified the retrieval and generation workflow into reusable functions
- Bounded conversation memory for efficient multi-turn interactions

## Changed

- Shifted from a research-specific notebook to a reusable document QA pipeline
- Removed evaluation-specific code from the main implementation notebook
- Prepared the backend for future Streamlit integration

---

# v0.6.4 — Engineering Hardening & Context Assembly

Released: August 2026

## Added

- Persistent FAISS index caching
- Model caching for faster notebook execution
- End-to-end latency measurement
- Graceful error handling
- Dependency pinning (`requirements.txt`)
- Author-name diagnostic utilities

## Improved

- Fixed context assembly to include the highest-ranked retrieved evidence
- Expanded query rewriting for gravitational-wave event terminology
- Improved notebook robustness and reproducibility

## Fixed

- Context selection bug affecting retrieved evidence
- Query expansion gaps for real-event retrieval

---

# v0.6.3 — Confidence-Gated Generation

Released: August 2026

## Added

- Retrieval-confidence threshold
- Confidence-gated "Don't Know" mode
- Threshold calibration utility
- Confidence-aware evaluation pipeline

## Improved

- Replaced TinyLlama with Qwen2.5-3B-Instruct
- Adopted chat-template prompting
- Improved instruction following
- Improved decoding strategy for generated responses

## Fixed

- Reduced hallucinations on out-of-document questions
- Fixed prompt decoding behaviour during generation

---

# v0.6.2 — Gold-Set Evaluation Framework

Released: August 2026

## Added

- Gold evaluation dataset
- Retrieval evaluation
- Generation evaluation
- Keyword-based answer checking
- Combined RAG evaluation workflow
- Support for unanswerable-question evaluation

## Improved

- Introduced repeatable benchmarking for retrieval and generation
- Added quantitative evaluation before future model improvements

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