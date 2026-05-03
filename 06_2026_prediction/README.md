# Bonus - 2026 F1 Championship Predictor

## Overview
Uses the trained XGBoost model from Part 4 to predict
race winners and championship standings for the full
2026 F1 season - 22 races, 11 teams, 22 drivers.

## Files
| File | Description |
|------|-------------|
| `prediction_2026.ipynb` | Main notebook - all 7 cells |
| `race_predictions_2026.csv` | Predicted winner per race |
| `championship_standings_2026.csv` | Final standings |
| `championship_standings_2026.png` | 4 panel standings chart |
| `race_winners_2026.png` | All 22 race winners chart |
| `points_progression_2026.png` | Season points progression |
| `part6_summary_card.png` | Visual summary card |
| `prediction_2026_summary.txt` | Full text summary |

## 2026 Grid
11 teams, 22 drivers including:
- Cadillac (new team debut)
- Audi (rebranded from Sauber)
- 22 race calendar (Bahrain and Saudi Arabia cancelled)

## How It Works
- Loads best_f1_model.pkl from Part 4
- Builds 2026 driver features from 2020-2024 history
- Predicts win probability for every driver in every race
- Simulates full championship points across 22 races
- Outputs predicted World Champion and Constructors Champion