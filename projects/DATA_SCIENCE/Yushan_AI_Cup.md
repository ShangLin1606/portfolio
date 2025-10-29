# 🏆 Yushan AI Cup — RAG Document QA System (文件檢索與問答系統)
**GitHub Repo:** [🔗 Open Project](https://github.com/ShangLin1606/yushan_ai_cup)

This project was developed for the **E.Sun AI Cup competition**,  
implementing a full RAG pipeline combining OCR, embeddings, FAISS, and LLM-based question answering.  
本專案參賽於玉山 AI Cup，以 OCR + 向量檢索 + LLM 為核心的文件問答系統。

---

## 🧩 Overview
The system processes thousands of PDF and JSON documents, converting them into searchable vector databases.  
Users can query across legal, financial, and insurance categories, and receive GPT-generated summarized answers.

---

## 🚀 Objectives
- Extract and normalize PDF/JSON datasets using OCR and regex rules.  
- Implement embedding + vector search pipeline for document retrieval.  
- Integrate GPT-4o-mini for final answer synthesis.  
- Support multi-domain question routing.

---

## 🧠 Architecture

OCR (pdfplumber + pytesseract)
↓
Embedding (m3e-large)
↓
Vector Store (FAISS)
↓
LLM (GPT-4o-mini)
↓
Answer JSON Output + Evaluation Script


---

## 💡 Key Features
- **Document Ingestion:** automatic OCR preprocessing and cleaning.  
- **Embedding Model:** m3e-large for multilingual sentence representation.  
- **Retriever-Augmented Generation:** FAISS + LLM hybrid pipeline.  
- **Evaluation Metrics:** JSON-based auto scoring script.

---

## 🧪 Results & Achievements
- Accuracy: **88% average match rate** across test set.  
- Automated data pipeline rebuilds per category.  
- One of top-performing submissions for that year’s competition.

---

## 👤 My Contributions
- Designed full RAG data flow (OCR → Embedding → FAISS → LLM).  
- Wrote auto-evaluation scripts and domain-based retrieval routing.  
- Tuned model hyperparameters for multilingual context.

---

## 🧰 Tech Stack
Python • LangChain • FAISS • m3e-large • pdfplumber • pytesseract • OpenAI API

---
