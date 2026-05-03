<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Formula+1+Display&size=40&duration=3000&pause=1000&color=FFD700&center=true&vCenter=true&width=800&lines=F1+AI+%26+ML+Engineer;Formula+1+Race+Prediction+%26+AI+Strategy" alt="Typing SVG" />

<br/>

![Python](https://img.shields.io/badge/Python-3.10+-FFD700?style=for-the-badge&logo=python&logoColor=black)
![XGBoost](https://img.shields.io/badge/XGBoost-Model-FF6B35?style=for-the-badge&logo=python&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-LLM-00D4AA?style=for-the-badge&logo=groq&logoColor=white)
![FastF1](https://img.shields.io/badge/FastF1-Telemetry-E8002D?style=for-the-badge&logo=f1&logoColor=white)
![SHAP](https://img.shields.io/badge/SHAP-Explainability-4ecdc4?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

<br/>

> **An end-to-end Formula 1 AI and Machine Learning project — from raw data analysis to an AI-powered race engineer chatbot — built entirely in Python.**

<br/>

[View Project](#project-overview) • [Notebooks](#notebooks) • [Setup](#setup) • [Results](#results) • [Tech Stack](#tech-stack)

<br/>

---

</div>

## What Is This?

This project transforms **14 raw F1 CSV files** (1950-2024) and **live FastF1 telemetry** into:

- 📊 Deep data visualizations of the modern F1 era (2020-2024)
- 🏎️ Live telemetry analysis from the 2024 Monaco Grand Prix
- 🤖 A machine learning model that predicts race winners
- 🔬 Advanced model improvement with SHAP explainability
- 🎙️ An AI race engineer chatbot that answers strategy questions

<br/>

---

## Project Overview

F1 Ai&ML Project/
├── 📁 data/                         ← Kaggle F1 CSVs (1950-2024)
├── 📁 cache/                        ← FastF1 telemetry cache
├── 📁 01_data_analysis/             ← COMPLETE
├── 📁 02_fastf1_visualizations/     ← COMPLETE
├── 📁 03_race_prediction/           ← COMPLETE
├── 📁 04_model_improvement/         ← COMPLETE
├── 📁 05_ai_race_engineer/          ← COMPLETE
└── 📄 README.md

<br/>

---

## Notebooks

### Part 1 — Data Analysis
> `01_data_analysis/analysis.ipynb`

Exploratory data analysis across **106 races and 2100+ entries** from the 2020-2024 F1 seasons.

| Visualization | Description |
|---|---|
| Driver Wins 2020-2024 | Horizontal bar chart of all race winners |
| Constructor Points | Championship points by team across 5 seasons |
| Points Progression | Side by side 2023 vs 2024 season comparison |
| Grid vs Finish | Scatter plot and heatmap of starting vs finishing position |
| Pit Stop Strategy | 3-panel layout of strategy trends across seasons |

**Theme:** Custom dark F1 theme (`#1a1a2e` background, `#FFD700` titles)

<br/>

---

### Part 2 — FastF1 Telemetry Visualizations
> `02_fastf1_visualizations/visualizations.ipynb`

Live telemetry pulled directly from the **2024 Monaco Grand Prix** using the FastF1 library.

| Visualization | Description |
|---|---|
| Tyre Strategy Chart | Full race tyre strategy for every driver |
| Speed Trace | P1 vs P2 speed comparison with throttle, brake, gear panels |

**Libraries:** `fastf1`, `scipy` (for interpolation)

<br/>

---

### Part 3 — Race Prediction Model
> `03_race_prediction/race_prediction.ipynb`

Binary classification model — predicts whether a driver will **win the race** (P1 = 1, else = 0).

| Detail | Value |
|---|---|
| Target | `is_winner` (binary) |
| Train set | 2021-2023 seasons |
| Test set | 2024 season (unseen) |
| Models | XGBoost vs Random Forest |
| Features | 15 engineered features |

**15 Features engineered:**
`grid`, `grid_squared`, `is_pole`, `is_front_row`, `driver_avg_points`,
`driver_form_3`, `driver_form_5`, `recent_win_rate`, `win_rate_at_circuit`,
`constructor_avg_points`, `constructor_form_3`, `championship_position`,
`championship_points`, `dnf_rate`, `round`

<br/>

---

### Part 4 — Model Improvement
> `04_model_improvement/model_improvement.ipynb`

Significant improvement over Part 3 with advanced tuning and explainability.

**What was done:**

- Expanded from **15 to 21 engineered features** (added pit stop efficiency, typical position gain, circuit averages)
- **GridSearchCV** hyperparameter tuning across hundreds of combinations
- **5-Fold Stratified Cross Validation** to handle class imbalance (~5% winners)
- **SHAP explainability** — beeswarm, global bar chart, and dependence plots
- Best model exported as `best_f1_model.pkl` for reuse

| SHAP Plot | What It Shows |
|---|---|
| Beeswarm | Per-prediction feature impact (red = pushed prediction up) |
| Bar Chart | Global feature importance ranked by mean absolute SHAP |
| Dependence (Grid) | How grid position SHAP value changes from P1 to P20 |
| Dependence (Points) | How driver quality impacts winning probability |

<br/>

---

### Part 5 — AI Race Engineer Chatbot
> `05_ai_race_engineer/race_engineer.ipynb`

An interactive AI race engineer powered by **real F1 data + Groq LLM**.

**How it works:**

Real F1 CSVs
↓
Compute driver stats, constructor stats, pit stop averages
↓
Build data context string (injected as system prompt)
↓
User asks strategy question
↓
Groq API (llama-3.3-70b-versatile) answers using real data
↓
Full conversation history sent every turn (AI has memory)

**Example questions you can ask:**
Who has been the most dominant driver from 2020 to 2024?
What is the ideal pit stop strategy for a 2-stop race at Monaco?
If Verstappen starts P3 at Monza what strategy would you recommend?
Which constructor has the best pit stop performance?
When is the best lap to pit under a safety car?
What tyre strategy works best in wet conditions?

<br/>

---

## Results

| Metric | Value |
|---|---|
| Races analyzed | 106 (2020-2024) |
| Race entries | 2100+ |
| Pit stop records | 8500+ |
| Features engineered | 21 |
| CV Folds | 5-Fold Stratified |
| Best model | XGBoost (tuned) |
| AI model | llama-3.3-70b-versatile |

<br/>

---

## Dataset

**Kaggle Formula 1 World Championship Dataset (1950-2024)**

| File | Description |
|---|---|
| `races.csv` | All race info by year and round |
| `results.csv` | Race results and finishing positions |
| `drivers.csv` | Driver info and nationalities |
| `constructors.csv` | Constructor and team info |
| `qualifying.csv` | Qualifying results |
| `pit_stops.csv` | Pit stop timings |
| `driver_standings.csv` | Championship standings per race |
| `constructor_standings.csv` | Constructor standings per race |
| `circuits.csv` | Circuit info and locations |
| `lap_times.csv` | Individual lap times |
| `status.csv` | Finish status codes |

<br/>

---

## Tech Stack

| Category | Libraries |
|---|---|
| Data | `pandas`, `numpy` |
| Visualization | `matplotlib`, `seaborn` |
| Telemetry | `fastf1`, `scipy` |
| Machine Learning | `scikit-learn`, `xgboost` |
| Explainability | `shap` |
| AI Chatbot | `groq`, `python-dotenv` |
| Environment | `jupyter`, `ipykernel` |

<br/>

---

## Setup

**1. Clone the repo**
```bash
git clone https://github.com/LeGiON-055/F1-AI-ML-ENGINEER.git
cd F1-AI-ML-ENGINEER
```

**2. Create and activate virtual environment**
```bash
python -m venv f1_env
f1_env\Scripts\activate
```

**3. Install all libraries**
```bash
pip install pandas numpy matplotlib seaborn fastf1 scipy
pip install scikit-learn xgboost shap
pip install groq python-dotenv jupyter ipykernel
```

**4. Add your Groq API key**
```bash
# Create this file: 05_ai_race_engineer/.env
GROQ_API_KEY=your-free-key-here
# Get free key at https://console.groq.com
```

**5. Run notebooks in order**
01_data_analysis/analysis.ipynb
02_fastf1_visualizations/visualizations.ipynb
03_race_prediction/race_prediction.ipynb
04_model_improvement/model_improvement.ipynb
05_ai_race_engineer/race_engineer.ipynb

<br/>

---

## Project Status
- Part 1 - Data Analysis         - COMPLETE
- Part 2 - FastF1 Visualizations - COMPLETE
- Part 3 - Race Prediction       - COMPLETE
- Part 4 - Model Improvement     - COMPLETE
- Part 5 - AI Race Engineer      - COMPLETE
- Bonus  - 2026 Predictor        - COMPLETE

<br/>

---

<div align="center">

**Built with passion for Formula 1 and Machine Learning**

⭐ Star this repo if you found it useful!

</div>