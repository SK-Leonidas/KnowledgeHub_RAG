# Changelog

## v0.5 - LLM Answer Generation

### Added
- TinyLlama integration for natural language answer generation
- Context-aware prompting using retrieved document chunks
- Interactive question-answering interface
- Source attribution alongside generated answers

### Improved
- Retrieval pipeline reused from v0.4
- Reduced hallucinations through context grounding

### Known Limitations
- Small LLM may occasionally produce incomplete or incorrect answers
- Metadata queries (e.g., author, supervisor) may require dedicated handling