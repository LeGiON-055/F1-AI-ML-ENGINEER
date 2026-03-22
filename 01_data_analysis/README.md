# Part 1 — F1 Data Analysis

Exploratory data analysis on 70+ years of Formula 1 race
history using Python, pandas, matplotlib and seaborn.

## What I explored

- How the number of races per year has grown since 1950
- Which drivers have the most wins of all time
- Which constructors dominated each decade
- Whether grid position (qualifying) actually predicts race finish

## Key findings

> Fill in after running the notebook — e.g.
> "Pole position converts to a win 40% of the time
> in the turbo hybrid era (2014–2023)"

## Files

| File | Description |
|------|-------------|
| analysis.ipynb | Main analysis notebook — run this |
| visualizations.py | Reusable plotting functions |
| README.md | This file |

## Output charts

All charts are saved to the `outputs/` folder:
- `races_per_year.png`
- `top_drivers_wins.png`
- `constructor_dominance.png`
- `grid_vs_finish.png`

## Dataset used

Files from the Kaggle Ergast dataset:
- `races.csv`
- `drivers.csv`
- `results.csv`
- `constructors.csv`

## How to run
```bash
# Make sure venv is active
f1_env\Scripts\activate.bat

# Open notebook in VS Code
# Click on analysis.ipynb
# Run each cell with Shift+Enter
```