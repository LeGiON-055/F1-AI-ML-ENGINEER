# 🏎️ Formula 1 AI Platform: Race Prediction & Strategy Intelligence

An end-to-end Machine Learning system built on real Formula 1 data, combining predictive modeling, telemetry analysis, and an AI-powered race engineer chatbot.

![Project Banner](visuals/part5_summary_card.png)

---

## 🚀 Overview

This project simulates a modern F1 analytics stack:

- 📊 Data Analysis (2020–2024 seasons)  
- 📡 Telemetry Insights (FastF1)  
- 🤖 Race Winner Prediction Models  
- 🧠 Model Explainability (SHAP)  
- 🗣️ AI Race Engineer Chatbot (LLM-powered)  

Built entirely using Python with real-world datasets and production-style workflows.

---

## 📈 Key Highlights

- Analyzed **106 races** and **2100+ race entries**
- Engineered **21 high-impact ML features**
- Trained **XGBoost & Random Forest models**
- Achieved **ROC-AUC ~0.97 on unseen 2024 data**
- Implemented **SHAP explainability (global + local)**
- Built a **context-aware AI chatbot (Groq + LLaMA 3.3)**

---

## 🧱 Project Architecture
F1-AI-ML-ENGINEER/
│
├── data/ # Kaggle dataset (1950–2024)
├── cache/ # FastF1 telemetry cache
│
├── 01_data_analysis/ # EDA & visualizations
├── 02_fastf1_visualizations/ # Telemetry analysis
├── 03_race_prediction/ # ML baseline models
├── 04_model_improvement/ # Tuning + SHAP
├── 05_ai_race_engineer/ # LLM chatbot
│
├── models/ # Saved ML models
├── visuals/ # Generated plots
├── README.md
└── requirements.txt

---

## 🧩 Project Breakdown

### 📊 Part 1 – Data Analysis

- Explored 2020–2024 seasons
- Driver wins, constructor dominance
- Grid vs finish correlation (strong ML signal)
- Pit stop strategies and trends  

![Data Analysis](visuals/part1_summary_card.png)

---

### 📡 Part 2 – FastF1 Telemetry

- Monaco GP 2024 analysis
- Tyre strategy visualization
- Speed trace comparison (P1 vs P2)
- Throttle, brake, and gear telemetry  

![Telemetry](visuals/part2_summary_card.png)

---

### 🤖 Part 3 – Race Prediction

- Binary classification (Winner vs Not Winner)
- Models: XGBoost, Random Forest
- 15 engineered features
- Train: 2021–2023 | Test: 2024  

![Model Evaluation](visuals/model_confusion_matrices.png)

---

### ⚙️ Part 4 – Model Improvement

- Expanded to **21 features**
- GridSearchCV hyperparameter tuning
- Stratified 5-Fold Cross Validation
- SHAP explainability:
  - Feature importance
  - Beeswarm plots
  - Dependence plots  

![SHAP](visuals/shap_explainability.png)

---

### 🗣️ Part 5 – AI Race Engineer

- LLM-powered chatbot (Groq + LLaMA 3.3)
- Injected real F1 statistics into system context
- Maintains conversation memory
- Answers strategy queries (tyres, pit stops, drivers)  

![AI Engineer](visuals/part5_summary_card.png)

---

## 📊 Model Performance

| Model          | ROC-AUC |
|---------------|--------|
| XGBoost       | 0.975  |
| Random Forest | 0.9746 |

- Evaluated on **fully unseen 2024 season**
- Balanced using **stratified cross-validation**

---

## 🧠 Explainability (SHAP)

Key influencing factors:

- Circuit win rate  
- Grid position  
- Championship position  
- Recent performance  
- Pit stop efficiency  

Provides transparency into **why predictions are made**, not just results.

---

## 🗂️ Dataset

Source: Kaggle Formula 1 World Championship Dataset (1950–2024)

Includes:

- Race results, drivers, constructors  
- Pit stops, qualifying, standings  
- Circuits, lap times, status codes  

---

## 🛠️ Tech Stack

**Languages & Libraries**

- Python, Pandas, NumPy  
- Scikit-learn, XGBoost  
- SHAP, SciPy  
- Matplotlib, Seaborn  

**Specialized Tools**

- FastF1 (telemetry)  
- Groq API (LLM integration)  

---

## ⚙️ Setup

```bash
git clone https://github.com/LeGiON-055/F1-AI-ML-ENGINEER.git
cd F1-AI-ML-ENGINEER

python -m venv f1_env
f1_env\Scripts\activate

pip install -r requirements.txt

## 🎨 Visualization Theme

- **Background:** `#1a1a2e`  
- **Primary:** `#FFD700` (F1 gold)  
- **Accent:** `#4ecdc4`  

---

## 🚧 Future Work

- 🏁 2026 race prediction system  
- 📊 Interactive dashboard (Streamlit)  
- 🌐 API deployment (FastAPI)  

---

## 📌 Why This Project Matters

This project demonstrates:

- End-to-end ML system design  
- Strong feature engineering  
- Real-world evaluation strategy  
- Model interpretability  
- AI application integration  