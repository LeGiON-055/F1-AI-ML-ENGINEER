# Part 2 — FastF1 Live Telemetry Visualisations (2024 Season)

Real F1 telemetry pulled live from Formula 1's official
data feed using the FastF1 API — 2024 season races.

## What I built

- Speed trace for fastest 2024 qualifying lap
- Driver head-to-head telemetry comparison (2024 race)
- Tyre strategy plot — 2024 race top 10 finishers
- Lap time delta between teammates (2024 season)

## Races covered

- 2024 Bahrain GP (season opener)
- 2024 Monaco GP (street circuit)
- 2024 British GP (Silverstone)
- 2024 Italian GP (Monza — highest speed circuit)

## Key insight

> Fill in after running — e.g.
> "Verstappen's top speed advantage at Monza 2024
> was +12 km/h over Hamilton in sector 2"

## Files

| File | Description |
|------|-------------|
| telemetry.ipynb | Main visualisation notebook |
| tyre_strategy.py | Reusable tyre strategy plot |
| README.md | This file |

## Output charts

- `speed_trace_2024.png`
- `driver_comparison_2024.png`
- `tyre_strategy_2024.png`
- `lap_delta_teammates_2024.png`

## How FastF1 works

FastF1 connects directly to F1's live timing system
and downloads lap-by-lap telemetry — speed, throttle,
brake, gear and GPS for every car in every session.
No manual download needed — it fetches automatically.

## How to run
```bash
f1_env\Scripts\activate.bat
# Open telemetry.ipynb
# Data downloads automatically on first run
# (needs internet connection)

```