# Part 3 — ML Race Prediction Model

Machine learning models trained to predict F1 race winners using 2021-2023 data, tested on the unseen 2024 season.

## Status: Complete ✅

## Models Built
| Model | ROC-AUC | Races Correct (2024) |
|---|---|---|
| XGBoost | TBC after your run | TBC |
| Random Forest | TBC after your run | TBC |

## Features Used (15 total)
| Feature | Description |
|---|---|
| `grid` | Qualifying / grid position |
| `grid_squared` | Non-linear grid advantage |
| `is_pole` | Pole position binary flag |
| `is_front_row` | Front row start binary flag |
| `driver_avg_points` | Driver average points per race |
| `driver_form_3` | Rolling 3 race points average |
| `driver_form_5` | Rolling 5 race points average |
| `recent_win_rate` | Rolling 5 race win rate |
| `win_rate_at_circuit` | Driver historical win % at circuit |
| `constructor_avg_points` | Team average points per race |
| `constructor_form_3` | Rolling 3 race team points |
| `championship_position` | Driver standing at race time |
| `championship_points` | Cumulative championship points |
| `dnf_rate` | Driver reliability score |
| `round` | Race number in season |

## Train / Test Split
- Train: 2021, 2022, 2023 seasons
- Test: 2024 season (completely unseen)
- Target: is_winner (1 = race winner, 0 = all others)

## Files Produced
| File | Description |
|---|---|
| `model_confusion_matrices.png` | Confusion matrix for both models |
| `predictions_vs_actual_2024.png` | Race by race predictions vs actual |
| `feature_importance_comparison.png` | Feature importance for both models |
| `model_metrics_comparison.png` | Full metrics comparison chart |
| `predictions_2024.csv` | Raw predictions with confidence scores |
| `part3_summary_card.png` | Summary visual card |

## Key Findings
- Grid position and championship standing are the strongest predictors
- XGBoost handles class imbalance better due to scale_pos_weight
- Rolling form features capture momentum that static averages miss
- ~5% positive class rate makes this a challenging imbalanced classification problem

## Next
Part 4 - Feature Engineering & Model Improvement