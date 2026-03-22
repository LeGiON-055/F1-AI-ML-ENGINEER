# Part 1 — F1 Data Analysis (2020–2024)

Exploratory data analysis focused on the modern Formula 1
era — the Verstappen/ground effect period from 2020 to 2024.

## What I explored

- Constructor championship battle 2020–2024
  (Mercedes → Red Bull dominance shift)
- Driver win counts in the hybrid/ground effect era
- Points progression across the 2023 and 2024 seasons
- Grid position vs race finish in the modern era
- Pit stop strategy trends 2020–2024

## Key findings

> Fill in after running the notebook — e.g.
> "Verstappen won 19 out of 22 races in 2023 —
> the highest win rate in modern F1 history"

## Files

| File | Description |
|------|-------------|
| analysis.ipynb | Main analysis notebook — run this |
| visualizations.py | Reusable plotting functions |
| README.md | This file |

## Output charts

All charts saved to `outputs/` folder:
- `wins_2020_2024.png`
- `constructor_points_2020_2024.png`
- `points_progression_2023.png`
- `grid_vs_finish_modern.png`

## Dataset

Kaggle Ergast dataset filtered to 2020–2024:
- `races.csv`
- `drivers.csv`
- `results.csv`
- `constructors.csv`
- `driver_standings.csv`

## How to run
```bashf1_env\Scripts\activate.bat
Open analysis.ipynb in VS Code
Run each cell with Shift+Enter