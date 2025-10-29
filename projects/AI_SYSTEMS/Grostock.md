# 📊 Grostock — AI Investment Advisor Platform (AI 投顧平台)
**GitHub Repo:** [🔗 Open Project](https://github.com/ShangLin1606/Grostock)

Grostock is an enterprise-grade **AI-powered investment advisor** that integrates RAG, GraphRAG, Dagster, and multi-agent orchestration for fully automated quantitative research and trading decision-making.  
Grostock 是一個結合 **RAG、GraphRAG、Dagster、自動化排程與多代理 LLM 系統** 的量化投資分析平台。

---

## 🧩 Overview
This system automates the entire data-to-decision pipeline for quantitative investment:  
from daily market data ingestion, ML model training, and portfolio analysis,  
to AI-driven strategy recommendation and PDF report generation.  

---

## 🚀 Objectives
- Create a unified AI platform for **quant strategy research and reporting**.  
- Use **multi-agent AI decision routing** to handle RAG and financial logic dynamically.  
- Enable **retrain-on-performance-drop** automation for daily models.  
- Integrate data orchestration via **Dagster** with financial database layers (PostgreSQL, Milvus, MongoDB).

---

## 🧠 Architecture

Frontend (React + Vite)
↓
FastAPI (LLM Router + Multi-Agent Decision Layer)
↓
Dagster (ETL + Scheduling + Model Jobs)
↓
PostgreSQL / Milvus / Neo4j
↓
Grafana / Prometheus / ELK (Monitoring)

---

## 💡 Key Features
- **Multi-Agent Decision Flow:** auto-selects FinanceAgent / SentimentAgent / RAG / GraphRAG.  
- **RAG Pipeline:** combines textual insights with database-driven metrics.  
- **Stacking Model:** LGBM + XGB + MLP + SVC → Logistic Regression meta-layer.  
- **Retraining Trigger:** automatic retrain when IC/F1 < threshold.  
- **Visualization:** real-time NAV, Sharpe, MDD dashboards.

---

## 🧪 Results & Achievements
- Reduced manual report generation time by 90%.  
- Model ensemble accuracy +8% after Bayesian tuning.  
- Integrated 20+ strategy portfolios in production.

---

## 👤 My Contributions
- Architected multi-agent logic & Dagster pipelines.  
- Implemented database schema for strategies, AUM, and audit logs.  
- Designed monitoring dashboards and CI/CD pipelines.

---

## 🧰 Tech Stack
FastAPI • Dagster • PostgreSQL • Milvus • LangChain • GraphRAG • PyTorch • Optuna • React • Grafana • Docker

---
