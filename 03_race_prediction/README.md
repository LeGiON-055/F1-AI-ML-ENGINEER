# Part 3 — ML Race Winner Prediction (2020–2024)

A machine learning model trained to predict Formula 1
race winners using 2020–2024 race data.

## Problem

Given pre-race information available before lights out
(grid position, championship standings, circuit),
can we predict which driver will win?

## Why 2020–2024 only?

Using only the modern era means the model learns from
current car regulations, tyre compounds and team
performance — not 1970s data that's irrelevant today.

## Approach

- Built structured dataset from Kaggle Ergast 2020–2024
- Trained RandomForestClassifier as baseline model
- Evaluated with accuracy, precision, recall, F1 score

## Results

| Metric | Score |
|--------|-------|
| Accuracy | [fill in after running] |
| Precision | [fill in after running] |
| Recall | [fill in after running] |
| F1 Score | [fill in after running] |

## Features used

- Grid position (qualifying result)
- Driver championship points before race
- Constructor championship points before race
- Circuit ID (encoded)
- Driver ID (encoded)

## Files

| File | Description |
|------|-------------|
| dataset_builder.py | Builds ML dataset from 2020–2024 CSVs |
| model_training.ipynb | Trains, evaluates and saves model |
| README.md | This file |

## How to run
```bash
f1_env\Scripts\activate.bat

# Step 1 — build the dataset
python dataset_builder.py

# Step 2 — open and run model_training.ipynb
```