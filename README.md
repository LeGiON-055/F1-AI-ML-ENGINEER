# 🏎️ F1 AI/ML Engineer Project

![Python](https://img.shields.io/badge/Python-3.11-blue)
![FastF1](https://img.shields.io/badge/FastF1-3.x-red)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.4-orange)
![XGBoost](https://img.shields.io/badge/XGBoost-latest-green)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)

## What this project is about

The 2020s have been the most data-rich era in Formula 1 history.
This project uses that data — live telemetry, race results,
tyre strategy, and driver performance — to build an end-to-end
AI/ML pipeline that analyses, predicts, and answers questions
about modern F1 racing.

**Data focus: 2020–2024 season (Verstappen era)**

## Project structureF1-AI-ML-Engineer/
│
├── 01_data_analysis/         ← 2020–2024 EDA with pandas
├── 02_fastf1_visualizations/ ← Live 2024 telemetry via FastF1
├── 03_race_prediction/       ← ML model trained on 2020–2024
├── 04_model_improvement/     ← XGBoost + feature engineering
├── 05_ai_race_engineer/      ← AI chatbot with live FastF1 RAG
│
├── data/                     ← Kaggle CSVs (not in repo)
├── outputs/                  ← Saved charts and plots
├── models/                   ← Saved ML models
└── src/                      ← Reusable utility scripts

## Project Progress

| Part | Topic | Status |
|---|---|---|
| 1 | Data Analysis (Kaggle) | Complete ✅ |
| 2 | FastF1 Telemetry Visualisations | In Progress 🔄 |
| 3 | Race Prediction ML Model | Upcoming |
| 4 | Feature Engineering & Model Improvement | Upcoming |
| 5 | AI Race Engineer Chatbot | Upcoming |

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
  — filtered to 2020–2024 for all analysis and ML
- FastF1 API — live 2024 telemetry, auto-downloaded by scripts

> Download the Kaggle dataset and place all CSV files inside the `data/` folder.

## Why 2020–2024?

This era covers:
- Max Verstappen's 4 consecutive world championships
- Mercedes dominance collapse and Red Bull rise
- Ferrari resurgence under Leclerc and Sainz
- New ground effect regulations from 2022
- The most competitive midfield in F1 history

This makes for the most interesting and relevant ML
and data analysis in the sport's history.

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