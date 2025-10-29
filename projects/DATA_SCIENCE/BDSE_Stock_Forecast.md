# BDSE Stock Forecast Platform — Multi-Model US Stock Prediction (美股漲跌預測平台)
**GitHub Repo:** [🔗 Open Project](./BDSE34_第二組_美股股價AI預測.pdf)

This project is a **multi-model ensemble forecasting system** predicting U.S. stock trends using RNN, SVM, and MLP,  
optimized via Bayesian tuning and GPU acceleration (cuML).  
本專案結合多模型堆疊、貝葉斯優化與 GPU 加速，實現美股漲跌預測平台。

---

## Overview
Built as part of the BDSE Data Science Program, this project predicts stock direction across sectors using technical and macroeconomic indicators,  
and deploys results to an interactive visualization web application.

---

## Objectives
- Combine multiple ML models (RNN, SVM, MLP) into an ensemble stacking architecture.  
- Replace GridSearch with **Bayesian Optimization** for hyperparameter tuning.  
- Accelerate model training using NVIDIA RAPIDS (cuDF / cuML).  
- Build a web-based dashboard for visualization and real-time prediction.

---

## Architecture

Data Collection (Yahoo Finance) → Feature Engineering → Multi-Model Training → Stacking → Flask Web App


---

## Key Features
- **RNN Temporal Model:** captures time dependencies in stock series.  
- **SVM & MLP Classifiers:** capture nonlinear decision boundaries.  
- **Stacking Layer:** Logistic Regression meta-model integrates base outputs.  
- **Bayesian Tuning:** faster convergence with Optuna.  
- **GPU Acceleration:** 4× faster training vs CPU baseline.

---

## Results & Achievements
- Accuracy: **80% (Finance)**, **74% (Tech)**  
- End-to-end pipeline deployed on Flask web app.  
- Received BDSE Program Excellence recognition (Top 3 team).

---

## My Contributions
- Led data preprocessing and model ensemble integration.  
- Implemented Bayesian optimization pipeline with Optuna.  
- Integrated dashboard front-end for model performance comparison.

---

## 🧰 Tech Stack
Python • cuML • cuDF • Optuna • MySQL • Flask • Plotly • Scikit-learn • TensorFlow

---
