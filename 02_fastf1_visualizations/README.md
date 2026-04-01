# Part 2 — FastF1 Telemetry Visualisations (2024 Monaco GP)

Real telemetry data analysis using the FastF1 API on the 2024 Monaco Grand Prix.

## Status: Complete ✅

## Charts Produced
| Chart | File |
|---|---|
| Tyre Strategy — all drivers full race | `monaco_2024_tyre_strategy.png` |
| Speed Trace — P1 vs P2 fastest lap | `monaco_2024_speed_trace.png` |
| Part 2 Summary Card | `part2_summary_card.png` |

## Key Insights
- Monaco 2024 was a classic one-stop race dominated by tyre management
- Speed trace reveals where each driver gains and loses time across the lap
- Throttle, brake and gear data shows driving style differences lap to lap
- Telemetry data is the foundation for the feature engineering in Part 4

## Tech Used
- FastF1 API for live telemetry and session data
- Matplotlib for all visualisations
- scipy for telemetry interpolation on speed delta fills

## Session
- Race: 2024 Monaco Grand Prix
- Circuit: Circuit de Monaco, Monte-Carlo
- Data: Laps, stints, tyre compounds, speed, throttle, brake, gear

## Next
Part 3 - ML Race Prediction Model