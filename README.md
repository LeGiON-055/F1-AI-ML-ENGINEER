# F1 AI/ML Engineer Project

A complete Formula 1 AI and Machine Learning project covering
data analysis, FastF1 telemetry, race prediction, model
explainability, and an AI race engineer chatbot - built with Python.

## GitHub
https://github.com/LeGiON-055/F1-AI-ML-ENGINEER

## Project Structure

F1 Ai&ML Project/
- data/                         Kaggle F1 CSVs (1950-2024)
- cache/                        FastF1 telemetry cache
- 01_data_analysis/             COMPLETE
- 02_fastf1_visualizations/     COMPLETE
- 03_race_prediction/           COMPLETE
- 04_model_improvement/         COMPLETE
- 05_ai_race_engineer/          COMPLETE
- README.md

## Parts Overview

### Part 1 - Data Analysis (COMPLETE)
Folder: 01_data_analysis/
Notebook: analysis.ipynb

Exploratory data analysis of the 2020-2024 F1 seasons.
- Driver wins 2020-2024 (horizontal bar chart)
- Constructor championship points 2020-2024
- Points progression 2023 and 2024
- Grid position vs race finish (scatter + heatmap)
- Pit stop strategy trends (3 panel layout)

Key outputs:
- driver_wins_2020_2024.png
- constructor_points_2020_2024.png
- points_progression_2023_2024.png
- grid_vs_finish_2020_2024.png
- pitstop_strategy_2020_2024.png
- part1_summary_card.png

---

### Part 2 - FastF1 Visualizations (COMPLETE)
Folder: 02_fastf1_visualizations/
Notebook: visualizations.ipynb

Live telemetry analysis using the FastF1 library.
Race analyzed: 2024 Monaco Grand Prix
- Full race tyre strategy for all drivers
- P1 vs P2 speed trace with throttle, brake, gear panels

Key outputs:
- monaco_2024_tyre_strategy.png
- monaco_2024_speed_trace.png
- part2_summary_card.png

---

### Part 3 - Race Prediction (COMPLETE)
Folder: 03_race_prediction/
Notebook: race_prediction.ipynb

Binary classification model to predict race winners.
- Target: is_winner (1 if P1 finish, 0 otherwise)
- Train: 2021-2023 | Test: 2024
- Models: XGBoost vs Random Forest
- 15 engineered features
- Race by race predictions vs actual 2024 results

Key outputs:
- model_confusion_matrices.png
- predictions_vs_actual_2024.png
- feature_importance_comparison.png
- model_metrics_comparison.png
- part3_summary_card.png

---

### Part 4 - Model Improvement (COMPLETE)
Folder: 04_model_improvement/
Notebook: model_improvement.ipynb

Advanced improvements over Part 3 models.
- 21 engineered features (up from 15)
- GridSearchCV hyperparameter tuning
- 5-Fold Stratified Cross Validation
- SHAP explainability (beeswarm, bar, dependence plots)
- Best model saved as best_f1_model.pkl

Key outputs:
- shap_explainability.png
- part4_summary_card.png
- ml_improvement_summary.txt

---

### Part 5 - AI Race Engineer (COMPLETE)
Folder: 05_ai_race_engineer/
Notebook: race_engineer.ipynb

AI-powered race engineer chatbot using real F1 data and Groq LLM.
- Real 2020-2024 F1 data injected as AI context
- llama-3.3-70b-versatile model via Groq (free)
- Full conversation memory per session
- Interactive loop - ask unlimited strategy questions
- Answers questions on tyres, pit stops, race craft, drivers

Key outputs:
- chat_log.txt
- part5_summary_card.png

---

## Dataset
Kaggle Formula 1 World Championship dataset (1950-2024)

| File | Description |
|------|-------------|
| races.csv | All race info by year and round |
| results.csv | Race results and finishing positions |
| drivers.csv | Driver info and nationalities |
| constructors.csv | Constructor/team info |
| qualifying.csv | Qualifying results |
| pit_stops.csv | Pit stop timings |
| driver_standings.csv | Championship standings per race |
| constructor_standings.csv | Constructor standings per race |
| circuits.csv | Circuit info and locations |
| lap_times.csv | Individual lap times |
| status.csv | Finish status codes |

## Libraries Used
- pandas, numpy, matplotlib, seaborn
- fastf1, scipy
- scikit-learn, xgboost, shap
- groq, python-dotenv
- jupyter, ipykernel, pickle

## Setup

1. Clone the repo:
git clone https://github.com/LeGiON-055/F1-AI-ML-ENGINEER.git

2. Create and activate virtual environment:
python -m venv f1_env
f1_env\Scripts\activate

3. Install all libraries:
pip install pandas numpy matplotlib seaborn fastf1 scikit-learn
pip install xgboost shap jupyter ipykernel requests python-dotenv
pip install groq

4. Add API keys:
- Create 05_ai_race_engineer/.env
- Add: GROQ_API_KEY=your-key-here
- Get free key at https://console.groq.com

5. Run notebooks in order (01 through 05)

## Theme
All visualizations use a dark F1 theme:
- Background : #1a1a2e
- Titles     : #FFD700 (gold)
- Accent     : #4ecdc4 (teal)

## Project Status
- Part 1 - Data Analysis         - COMPLETE
- Part 2 - FastF1 Visualizations - COMPLETE
- Part 3 - Race Prediction       - COMPLETE
- Part 4 - Model Improvement     - COMPLETE
- Part 5 - AI Race Engineer      - COMPLETE
- Bonus  - 2026 Predictor        - UPCOMING