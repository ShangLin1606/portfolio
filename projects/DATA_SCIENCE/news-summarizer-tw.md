#  news-summarizer-tw — News Classification and Summarization System（新聞分類與摘要系統）
**GitHub Repo:** [🔗 Open Project](https://github.com/ShangLin1606/news-summarizer-tw)

This project provides a **modular NLP pipeline** to clean, convert, summarize, and evaluate Chinese (Traditional) news articles.  
本專案以多階段設計，涵蓋「資料治理 → 簡轉繁 → 文字清理 → 摘要生成 → 指標評估 → 資料集切分 → 訓練」的完整流程，適用於研究與實作落地。

---

## Overview
The pipeline standardizes raw news data, converts Simplified to Traditional Chinese, performs text cleaning, and generates summaries via an LLM/model abstraction.  
結果可透過 **BERTScore/ROUGE** 等指標評估，並輸出可重現的報表與資料集，便於後續模型訓練與比較。

**Dataset**: Kaggle — *Categorised News Dataset from Fudan University*（請依其授權條款使用與引用）

---

## Objectives
- Build a **scalable, stage-based pipeline** for Chinese news summarization.  
- Provide a **unified model interface** to switch between cloud LLMs and local Transformer models.  
- Offer **reproducible metrics and artifacts** (reports, summaries, datasets) for experiments and benchmarking.

---

## Architecture

Raw News → Folder Restructure → S2T Conversion → Text Cleaning → Statistics → Summarization（LLM Wrapper）→ Evaluation（BERTScore/ROUGE）→ Dataset Prep → (Optional) Model Training

---

## Key Features
- **8-Stage Pipeline**: `stage01`–`stage08` 對應清楚；可單獨或串行執行。  
- **繁體中文友善**：Stage 02 內建簡轉繁（S2T），適配臺灣用字。  
- **Model Abstraction**：`models/llm_model.py` 封裝 `summarize()` 介面，輕鬆切換 LLM/本地模型。  
- **Evaluation-Ready**：Stage 06 提供 BERTScore；可延伸 ROUGE、BLEURT 與人評流程。  
- **Reproducible Outputs**：產生統計報表、摘要結果與資料集切分，方便版本化與比較。

---

## Results & Deliverables
- **Artifacts**：
  - 清理後文本與摘要檔（分階段輸出）  
  - 統計報表（長度分佈、詞頻等）與評估結果（BERTScore/ROUGE）  
  - 可直接訓練的資料集（train/valid/test）
- **Qualitative Outcomes**：整體摘要更聚焦、冗詞雜訊下降、長文處理更穩定（可搭配切片/RAG 強化）。

> 註：指標成效會依資料選取、預處理策略與所選模型而異。

---

## My Contributions
- 規劃與實作 **8 階段模組化 Pipeline**，強調可維護性與擴充性。  
- 設計 **LLM/Transformer 統一接口**，支援雲端與本地模型快速切換。  
- 製作 **統計/評估報表輸出** 與資料夾規範，提升重現性與團隊協作效率。

---

## Tech Stack
Python • Transformers • PyTorch • bert-score • OpenCC • Jieba / Tokenization • Pandas / Polars • Matplotlib  
(Optional) Flask / FastAPI for service endpoints; ROUGE / BLEURT for additional metrics


