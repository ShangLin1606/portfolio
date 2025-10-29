# 📰 news-summarizer-tw — Traditional Chinese News Summarization Pipeline（繁中新聞摘要全流程）
**GitHub Repo:** [🔗 Open Project](https://github.com/ShangLin1606/news-summarizer-tw)

This project provides a **modular NLP pipeline** to clean, convert, summarize, and evaluate Chinese (Traditional) news articles.  
本專案以多階段設計，涵蓋「資料治理 → 簡轉繁 → 文字清理 → 摘要生成 → 指標評估 → 資料集切分 → 訓練」的完整流程，適用於研究與實作落地。

---

## 🧩 Overview
The pipeline standardizes raw news data, converts Simplified to Traditional Chinese, performs text cleaning, and generates summaries via an LLM/model abstraction.  
結果可透過 **BERTScore/ROUGE** 等指標評估，並輸出可重現的報表與資料集，便於後續模型訓練與比較。

**Dataset**: Kaggle — *Categorised News Dataset from Fudan University*（請依其授權條款使用與引用）

---

## 🚀 Objectives
- Build a **scalable, stage-based pipeline** for Chinese news summarization.  
- Provide a **unified model interface** to switch between cloud LLMs and local Transformer models.  
- Offer **reproducible metrics and artifacts** (reports, summaries, datasets) for experiments and benchmarking.

---

## 🧠 Architecture

Raw News → Folder Restructure → S2T Conversion → Text Cleaning → Statistics → Summarization（LLM Wrapper）→ Evaluation（BERTScore/ROUGE）→ Dataset Prep → (Optional) Model Training

---

## 💡 Key Features
- **8-Stage Pipeline**: `stage01`–`stage08` 對應清楚；可單獨或串行執行。  
- **繁體中文友善**：Stage 02 內建簡轉繁（S2T），適配臺灣用字。  
- **Model Abstraction**：`models/llm_model.py` 封裝 `summarize()` 介面，輕鬆切換 LLM/本地模型。  
- **Evaluation-Ready**：Stage 06 提供 BERTScore；可延伸 ROUGE、BLEURT 與人評流程。  
- **Reproducible Outputs**：產生統計報表、摘要結果與資料集切分，方便版本化與比較。

---

## 🧪 Results & Deliverables
- **Artifacts**：
  - 清理後文本與摘要檔（分階段輸出）  
  - 統計報表（長度分佈、詞頻等）與評估結果（BERTScore/ROUGE）  
  - 可直接訓練的資料集（train/valid/test）
- **Qualitative Outcomes**：整體摘要更聚焦、冗詞雜訊下降、長文處理更穩定（可搭配切片/RAG 強化）。

> 註：指標成效會依資料選取、預處理策略與所選模型而異。

---

## 👤 My Contributions
- 規劃與實作 **8 階段模組化 Pipeline**，強調可維護性與擴充性。  
- 設計 **LLM/Transformer 統一接口**，支援雲端與本地模型快速切換。  
- 製作 **統計/評估報表輸出** 與資料夾規範，提升重現性與團隊協作效率。

---

## 🧰 Tech Stack
Python • Transformers • PyTorch • bert-score • OpenCC • Jieba / Tokenization • Pandas / Polars • Matplotlib  
(Optional) Flask / FastAPI for service endpoints; ROUGE / BLEURT for additional metrics

---

## 📦 Dataset
- **Kaggle**: *Categorised News Dataset from Fudan University*（請至 Kaggle 下載並遵循其授權條款）  
- 建議將原始資料置於 `data/raw/`，其餘階段輸出依序放於 `data/01_restructured/`、`data/02_trad/`、`data/03_clean/`… 等目錄。

---

## 🧭 How to Run (Stages)
```bash
# 01 目錄重整
python stage01_preprocess_folder_restructure.py --src data/raw --dst data/01_restructured

# 02 簡轉繁
python stage02_text_convert_s2t.py --src data/01_restructured --dst data/02_trad

# 03 文字清理
python stage03_text_cleaning.py --src data/02_trad --dst data/03_clean

# 04 統計分析
python stage04_data_statistics_analysis.py --src data/03_clean --report out/reports/stats.json

# 05 摘要生成（透過 models/llm_model.py）
python stage05_generate_summary.py --src data/03_clean --dst data/05_summaries --model llm_default

# 06 摘要評估（BERTScore/可擴充 ROUGE）
python stage06_summary_evaluation_bertscore.py --src data/05_summaries --ref data/refs --out out/metrics/bertscore.csv

# 07 資料集切分
python stage07_dataset_preparation.py --src data/03_clean --dst data/07_dataset --split 0.8 0.1 0.1

# 08 模型訓練（可選）
python stage08_model_training.py --data data/07_dataset --out out/models/baseline
```

---

## 📜 License
**MIT License**（本程式碼採用 MIT；資料集授權依 Kaggle/原始提供方規範）

---

## 🙏 Acknowledgements
- Kaggle — *Categorised News Dataset from Fudan University*  
- 開源社群於中文 NLP、長文摘要與評估指標（BERTScore/ROUGE）的貢獻
