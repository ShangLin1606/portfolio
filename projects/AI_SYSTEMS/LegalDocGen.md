# LegalDocGen — AI Legal Document & Evidence Letter Generator
**GitHub Repo:** [🔗 Open Project](https://github.com/ShangLin1606/LegalDocGen)

LegalDocGen is an **AI-driven legal document generation platform** that automates the drafting of lawyer letters, evidence notices, and legal templates using RAG + GraphRAG + TinyLLaMA.  
LegalDocGen 是一個結合法律語料檢索、圖譜推理與生成式 AI 的律師文件自動撰寫系統。

---

## Overview
Designed for law firms and corporate compliance teams, the system allows users to generate context-aware, regulation-compliant drafts in seconds — while ensuring legal validity and citation transparency.

---

## Objectives
- Replace manual legal drafting with **AI-assisted automation**.  
- Incorporate **legal retrieval augmentation (RAG)** for case-based reasoning.  
- Support **graph-based context linking (GraphRAG)** for statute correlation.  
- Provide multilingual generation (Chinese + English).

---

## Architecture

User Input → Retrieval Agent → Graph Reasoning Agent → Drafting Agent → Review Agent → Output (PDF)


- **LangChain** for orchestration  
- **ChromaDB** for embeddings  
- **NetworkX** for legal graph traversal  
- **MLflow** for model management  
- **Streamlit UI** for user-facing preview

---

## Key Features
- **GraphRAG Retrieval:** hybrid vector + graph reasoning for legal context.  
- **Multi-Agent Framework:** separates retrieval, drafting, and review stages.  
- **TinyLLaMA + LoRA Fine-Tuning:** domain adaptation for legal phrasing.  
- **Template Injection:** auto-formatting for lawyer and evidence letters.  
- **Audit Trail:** generates metadata for legal traceability.

---

## Results & Achievements
- Draft generation reduced from 2 minutes → 15 seconds.  
- BLEU score +20% improvement vs GPT-3 baseline.  
- Positive feedback from 5 trial legal professionals.

---

## My Contributions
- Designed the full multi-agent pipeline (Retrieval → Draft → Review).  
- Implemented LoRA fine-tuning and MLflow experiment tracking.  
- Built Streamlit frontend and Dockerized backend deployment.

---

## Tech Stack
LangChain • GraphRAG • TinyLLaMA • MLflow • ChromaDB • Streamlit • Docker • FastAPI • spaCy • BeautifulSoup

---
