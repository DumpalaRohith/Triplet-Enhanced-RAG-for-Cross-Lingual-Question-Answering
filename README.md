# Triplet-Enhanced Cross-Lingual RAG System

A Retrieval-Augmented Generation (RAG) based cross-lingual question answering system that combines structured triplet extraction with retrieval and reranking techniques to improve multilingual answer generation.

This project enhances traditional RAG pipelines by converting retrieved passages into structured knowledge triplets before answer generation, reducing retrieval noise and improving answer relevance across multiple languages.

# Features

- Cross-lingual Question Answering using the XOR-TyDi QA dataset
- BM25-based document retrieval from English Wikipedia passages
- CrossEncoder reranking for semantic relevance filtering
- REBEL-based triplet extraction for structured knowledge representation
- Query-aware triplet ranking using semantic similarity and answer-type matching
- Lightweight and efficient pipeline without dependency on large multilingual models
- Supports Telugu, Bengali, Arabic, and Korean datasets

# Pipeline Overview

1. Query Translation  
   Non-English queries are translated into English for downstream processing.

2. Document Retrieval  
   BM25 retrieves candidate Wikipedia passages relevant to the translated query.

3. Neural Reranking  
   CrossEncoder reranking selects the most semantically relevant passages.

4. Triplet Extraction  
   REBEL extracts structured subject–relation–object triplets from retrieved passages.

5. Triplet Ranking  
   Triplets are ranked using semantic similarity and answer-type-aware scoring.

6. Answer Generation  
   A lightweight LLM generates concise answers using ranked triplets and supporting evidence.

# Results

The proposed Triplet-Enhanced RAG pipeline achieved strong performance on the XOR-TyDi QA benchmark:

| Language | F1 Score |
|---|---|
| Telugu | 47.72% |
| Bengali | 31.37% |
| Arabic | 43.33% |
| Korean | 26.14% |

The system outperformed existing cross-lingual QA baselines while maintaining computational efficiency.

# Technologies Used

- Python
- RAG
- BM25 Retrieval
- CrossEncoder Reranking
- REBEL
- Sentence Transformers
- Qwen2.5
- spaCy
- Hugging Face Transformers
- PyTorch

# Applications

- Multilingual Question Answering
- AI Assistants
- Information Retrieval Systems
- Cross-Lingual Search
- Knowledge-Augmented NLP Systems
