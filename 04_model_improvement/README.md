# Part 4 — Feature Engineering & Model Improvement (2020–2024)

Improving the Part 3 model by adding domain knowledge
about modern F1 — tyre strategy, track characteristics,
driver form — and switching to XGBoost.

## What changed from Part 3

| Thing | Part 3 | Part 4 |
|-------|--------|--------|
| Model | RandomForest | XGBoost |
| Features | 5 basic | 12 engineered |
| Tuning | None | GridSearchCV |
| Data | 2020–2024 | 2020–2024 + enriched |

## New features added

- Rolling driver form (avg finish last 5 races)
- Rolling constructor form (last 5 races)
- Circuit type: street / power / technical / mixed
- Tyre compound history per circuit
- Qualifying gap to pole (seconds)
- Weather flag: dry / wet
- Whether driver is defending champion

## Results

| Model | Accuracy |
|-------|----------|
| RandomForest (Part 3) | [fill in]% |
| XGBoost (Part 4) | [fill in]% |
| Improvement | +[fill in]% |

## Files

| File | Description |
|------|-------------|
| feature_engineering.ipynb | Full feature engineering notebook |
| tuning.py | GridSearchCV hyperparameter tuning |
| README.md | This file |

## How to run
```bash
f1_env\Scripts\activate.bat
# Open feature_engineering.ipynb
# Run each cell with Shift+Enter
```