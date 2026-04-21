# Part 4 - Model Improvement

## Overview
Advanced model improvement over Part 3 using hyperparameter tuning,
cross validation, SHAP explainability, and model export.

## Files
| File | Description |
|------|-------------|
| `model_improvement.ipynb` | Main notebook - all 6 cells |
| `best_f1_model.pkl` | Final saved model (XGBoost or RF) |
| `shap_explainability.png` | SHAP beeswarm, bar, dependence plots |
| `part4_summary_card.png` | Visual summary card |
| `ml_improvement_summary.txt` | Text summary of all results |

## What Was Done

### Feature Engineering (21 Features)
Expanded from 15 features in Part 3 to 21:
- grid, grid_squared, is_pole, is_front_row
- driver_avg_points, driver_form_3, driver_form_5
- recent_win_rate, win_rate_at_circuit, avg_points_at_circuit
- constructor_avg_points, constructor_form_3
- championship_position, championship_points
- dnf_rate, round, driver_avg_finish, driver_win_rate
- typical_gain, num_pitstops, avg_pitstop_time

### Hyperparameter Tuning
- GridSearchCV with StratifiedKFold (5 folds)
- XGBoost: tuned n_estimators, max_depth, learning_rate,
  subsample, colsample_bytree, scale_pos_weight
- Random Forest: tuned n_estimators, max_depth,
  min_samples_split, min_samples_leaf, class_weight

### Cross Validation
- 5-Fold Stratified Cross Validation
- Stratified to handle class imbalance (only ~5% winners)
- F1 score used as primary metric

### SHAP Explainability
- Beeswarm plot - per prediction feature impact
- Bar chart - global mean absolute SHAP importance
- Dependence plot - Grid Position vs SHAP value
- Dependence plot - Driver Avg Points vs SHAP value

### Model Export
- Best model saved as best_f1_model.pkl
- Includes model, feature list, metadata, timestamp

## Train / Test Split
- Train: 2021-2023 seasons
- Test: 2024 season (unseen data)
- Target: is_winner (binary - 1 if P1 finish)

## Results
See ml_improvement_summary.txt for full metrics.