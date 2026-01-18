# rag-knowledge-graph-qa
Academic RAG pipeline with knowledge graph integration for document-based question answering

## Project Overview
This project is an academic implementation of a Retrieval-Augmented Generation (RAG) system designed to answer user queries from unstructured documents. The system combines semantic retrieval using vector embeddings with a knowledge graph layer to improve contextual understanding and answer relevance.

The project was developed as part of a postgraduate semester curriculum focused on Deep Learning and Generative AI.

---

## Problem Statement
Traditional keyword-based search systems struggle to provide accurate answers from large unstructured documents. This project aims to:
- Retrieve the most relevant document segments for a given query
- Enhance retrieval using semantic similarity and entity relationships
- Generate coherent, context-aware answers using a Large Language Model (LLM)

---

## System Architecture (Conceptual)
The system follows a modular pipeline:

1. Document ingestion and preprocessing  
2. Text chunking for manageable context windows  
3. Embedding generation for semantic representation  
4. Vector-based retrieval using similarity search  
5. Knowledge graph-based contextual enrichment  
6. LLM-based answer generation  

---

## End-to-End Pipeline

### 1. Document Ingestion
Input documents (PDFs/text files) are loaded and converted into plain text for further processing.

### 2. Text Chunking
Documents are split into smaller chunks to ensure effective embedding generation and retrieval within LLM context limits.

### 3. Embedding Generation
Each text chunk is converted into a dense vector representation using transformer-based embedding models via LangChain.

### 4. Semantic Retrieval
Vector similarity search is performed using FAISS to retrieve the most relevant chunks for a given query.

### 5. Knowledge Graph Integration
Entities and relationships extracted from the documents are structured into a basic knowledge graph. This graph is used to:
- Maintain relationships between key concepts
- Improve contextual grounding during retrieval

### 6. Answer Generation
Retrieved context is passed to an LLM through a LangChain-powered RAG pipeline to generate final answers.

---

## Role of the Knowledge Graph
The knowledge graph acts as a contextual layer that:
- Preserves entity relationships across documents
- Reduces ambiguity in retrieved content
- Improves answer consistency for related queries

---

## Technologies Used
- Python  
- LangChain  
- FAISS  
- Hugging Face Transformers  
- Ollama (local LLM inference)  
- Jupyter Notebook  

---

## Results and Evaluation
The system was evaluated qualitatively based on:
- Retrieval relevance
- Semantic coherence of generated answers
- Response latency during inference

---

## Limitations
- Knowledge graph construction is basic and rule-driven
- Evaluation metrics are mostly qualitative
- Limited dataset size due to academic constraints

---

## Future Improvements
- Automated knowledge graph extraction using NLP pipelines
- Integration with scalable vector databases
- Deployment as a REST API using FastAPI
- Quantitative evaluation using benchmark datasets

---

## Notes
Generated artifacts such as embeddings and FAISS indexes are excluded from this repository as they are reproducible outputs and environment-dependent.
