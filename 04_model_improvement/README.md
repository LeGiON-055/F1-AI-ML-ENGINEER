# Part 4 — Feature Engineering & Model Improvement

Taking the Part 3 skeleton model and improving it
significantly using better features and XGBoost.

## What changed from Part 3

| Thing | Part 3 | Part 4 |
|-------|--------|--------|
| Model | RandomForest | XGBoost |
| Features | 5 basic features | 10+ engineered features |
| Tuning | None | GridSearchCV |

## New features added

- Rolling driver form (avg finish last 5 races)
- Rolling constructor form
- Tyre compound history per circuit
- Circuit type encoding (street, power, technical)
- Pit stop count from previous races
- Weather flag (dry/wet)

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
# Open feature_engineering.ipynb and run each cell
```