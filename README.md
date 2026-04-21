# RAG-TotalEnergies-Project
Implementing a Retrieval-Augmented Generation (RAG) System using ChromaDB and Hugging Face LLMs

# Retrieval-Augmented Generation (RAG) System using ChromaDB and Hugging Face LLMs

## Author
Augustin COUVREUR

## Course
Deep Learning – Centrale Lyon  
BSc Data Science for Responsible Business

## Project Objective

The goal of this project is to build a Retrieval-Augmented Generation (RAG) system capable of answering user questions using information extracted from an external document.

The selected dataset is the TotalEnergies Sustainability & Climate Progress Report (2025).

The system combines:

- Sentence embeddings
- ChromaDB vector database
- Hugging Face LLMs
- Prompt engineering
- Retrieval pipeline

---

## Dataset

Document used:

- TotalEnergies Sustainability & Climate Progress Report 2025 (PDF)

This report contains information about:

- Climate targets
- Carbon emissions
- Renewable energy strategy
- Governance commitments
- ESG indicators

---

## Architecture

User Question  
→ Embedding generation  
→ ChromaDB semantic retrieval  
→ Context selection  
→ Prompt construction  
→ LLM answer generation

---

## Technologies Used

- Python
- Google Colab
- ChromaDB
- SentenceTransformers
- Hugging Face Transformers
- LangChain PDF Loader

---

## Iterative Improvements

### V1 – Baseline RAG

- Basic retrieval
- Simple prompt
- FLAN-T5 model

**Issue:** Answers were short and incomplete.

### V2 – Improved Prompting

- Better instructions
- Structured output request

**Issue:** Still weak synthesis.

### V3 – Better Retrieval

- More retrieved chunks
- Filtering relevant chunks

**Issue:** Noise remained.

### V4 – Stronger LLM

- Switched to Qwen model

**Improvement:** Better reasoning and richer answers.

### V5 – Hallucination Reduction

- Lower temperature
- Deterministic generation
- Context-only prompting

**Improvement:** More factual outputs.

---

## Example Question

What are TotalEnergies' main climate goals and targets?

## Example Answer

- Reduce Scope 1 and 2 emissions by 40% by 2030 vs 2015
- Use carbon credits for residual emissions
- Support carbon pricing mechanisms
- Expand renewable energy investments

---

## Evaluation Criteria

The system was evaluated on:

- Relevance of retrieved chunks
- Quality of generated answers
- Hallucination level
- Response clarity
- Runtime performance

---

## Future Improvements

- Add citations with source pages
- Multi-document RAG
- Conversational memory
- Re-ranking retriever
- Gradio web interface
