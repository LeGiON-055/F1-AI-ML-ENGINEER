# Part 2 — FastF1 Telemetry Visualisations

Real F1 telemetry data pulled directly from Formula 1's
official data feed using the FastF1 Python library.

## What I built

- Speed trace for the fastest qualifying lap
- Side-by-side driver speed comparison (top 5 qualifiers)
- Tyre strategy plot for race top 10 finishers

## Key insight

> Fill in after running — e.g.
> "Verstappen's speed advantage over Hamilton was most
> visible in sector 2 at Monza 2023"

## Files

| File | Description |
|------|-------------|
| telemetry.ipynb | Main visualisation notebook |
| tyre_strategy.py | Reusable tyre strategy plot script |
| README.md | This file |

## Output charts

- `speed_trace_monza_2023.png`
- `driver_speed_comparison_monza.png`
- `tyre_strategy_monza_2023.png`

## How FastF1 works

FastF1 connects to F1's official timing data and downloads
lap-by-lap telemetry including speed, throttle, brake,
gear and GPS position for every car in every session.

## How to run
```bash
f1_env\Scripts\activate.bat
# Open telemetry.ipynb and run each cell
```