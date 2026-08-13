# KnowledgeHub RAG v0.6.2 – Gold Set Evaluation

## Objective

v0.6.2 adds a structured evaluation layer to the conversational RAG system introduced in v0.6.1.

The goal of this release is to evaluate whether the system retrieves the correct document evidence and generates grounded answers for both answerable and unanswerable questions. This establishes a repeatable baseline for identifying retrieval failures, hallucinations, and weaknesses in the generation model before introducing further improvements.

---

## What Changed in this Version

### Added

- Gold evaluation dataset (`gold_eval.json`)
- Answerable document questions
- Unanswerable and out-of-document questions
- Expected answers and keyword-based evaluation
- Expected source pages and chunks
- Retrieval evaluation
- Generation evaluation
- End-to-end `evaluate_rag()` benchmarking pipeline

### Evaluation Metrics

- Retrieval Accuracy
- Generation Accuracy

### Preserved from v0.6.1

- Conversation memory
- Follow-up question handling
- FAISS semantic retrieval
- BM25 lexical retrieval
- Hybrid retrieval
- Query expansion
- Weighted score fusion
- Reciprocal Rank Fusion (RRF)
- Context expansion
- TinyLlama answer generation

---

## Evaluation Workflow

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
TinyLlama Response
        │
        ▼
Gold Set Evaluation
        │
        ▼
Retrieval Accuracy + Generation Accuracy
```

---

## Example Evaluation

```text
Question:
What algorithm was used for classification?

Retrieval : PASS

Generated Answer:
Gradient Boosted Decision Trees (GBDT).

Generation : PASS
```

---

## Why this Version Matters

v0.6.2 transforms KnowledgeHub from a system that can be demonstrated manually into one that can be evaluated systematically.

The automated evaluation framework provides quantitative measurements of retrieval and generation performance, making future improvements measurable instead of subjective.

This release establishes the first evaluation baseline against which future retrieval strategies, language models, confidence thresholds, and hallucination mitigation techniques can be compared.

---

## Current Limitations

- Keyword-based evaluation is heuristic rather than semantic.
- TinyLlama may hallucinate on unsupported or out-of-document questions.
- Gold evaluation set is manually curated.
- Supports evaluation on one document at a time.

---

## Next Version (v0.6.3)

- Retrieval confidence scoring
- Confidence thresholding
- "Don't Know" response mode
- Hallucination reduction for unsupported questions

---

## Version

**KnowledgeHub RAG v0.6.2**

---

## Author

**Surendaranath Kanniyappan**

GitHub: https://github.com/SK-Leonidas

Building Retrieval-Augmented Generation systems from scratch while documenting every engineering milestone.