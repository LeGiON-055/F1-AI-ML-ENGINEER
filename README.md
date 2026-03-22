# 🏎️ F1 AI/ML Engineer Project

![Python](https://img.shields.io/badge/Python-3.11-blue)
![FastF1](https://img.shields.io/badge/FastF1-3.x-red)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.4-orange)
![XGBoost](https://img.shields.io/badge/XGBoost-latest-green)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)

## What this project is about

Can we use 70+ years of Formula 1 data to analyse driver
performance, predict race winners with machine learning, and
build an AI assistant that answers race analytics questions?

This project explores that question end-to-end — from raw
CSV data all the way to a working AI chatbot.

## Project structureF1-AI-ML-Engineer/
│
├── 01_data_analysis/        ← EDA with pandas & matplotlib
├── 02_fastf1_visualizations/ ← Live telemetry with FastF1
├── 03_race_prediction/      ← ML model with RandomForest
├── 04_model_improvement/    ← XGBoost + feature engineering
├── 05_ai_race_engineer/     ← AI chatbot with LLM + RAG
│
├── data/                    ← Kaggle CSVs (not in repo)
├── outputs/                 ← Saved charts and plots
├── models/                  ← Saved ML models
└── src/                     ← Reusable utility scripts

## What I built

| Part | Topic | Tech | Status |
|------|-------|------|--------|
| 01 | F1 data analysis | pandas, matplotlib, seaborn | 🔄 In Progress |
| 02 | Telemetry visualisations | FastF1, matplotlib | ⏳ Coming soon |
| 03 | ML race prediction | scikit-learn, RandomForest | ⏳ Coming soon |
| 04 | Feature engineering | XGBoost, GridSearchCV | ⏳ Coming soon |
| 05 | AI race engineer chatbot | LLM API, RAG, FastF1 | ⏳ Coming soon |

## Results

> Charts and accuracy numbers will be added as each part is completed.

## Setup
```bashClone the repo
git clone https://github.com/LeGiON-055/F1-AI-ML-Engineer
cd F1-AI-ML-EngineerCreate and activate virtual environment
python -m venv f1_envWindows
f1_env\Scripts\activate.batMac/Linux
source f1_env/bin/activateInstall all dependencies
pip install -r requirements.txt

## Dataset

- [Ergast F1 World Championship Dataset — Kaggle](https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020)
- FastF1 API — live telemetry data, auto-downloaded by scripts

> Download the Kaggle dataset and place all CSV files inside the `data/` folder.

## Tech stack

- Python 3.11
- pandas, numpy
- matplotlib, seaborn
- FastF1
- scikit-learn
- XGBoost
- LLM API (Claude / OpenAI)

## Author

**Samarth Gupta** — [GitHub](https://github.com/LeGiON-055)