# Part 3 — ML Race Winner Prediction

A machine learning model trained to predict Formula 1
race winners using historical race data.

## Problem

Given pre-race information (grid position, championship
standings, circuit), can we predict which driver will win?

## Approach

- Built a structured dataset from the Kaggle Ergast CSVs
- Trained a RandomForestClassifier
- Evaluated using accuracy, precision, recall and F1 score

## Results

| Metric | Score |
|--------|-------|
| Accuracy | [fill in] |
| Precision | [fill in] |
| Recall | [fill in] |
| F1 Score | [fill in] |

## Features used

- Grid position (qualifying result)
- Driver championship points before race
- Constructor championship points before race
- Circuit ID (encoded)
- Driver ID (encoded)

## Files

| File | Description |
|------|-------------|
| dataset_builder.py | Builds ML dataset from raw CSVs |
| model_training.ipynb | Trains, evaluates and saves model |
| README.md | This file |

## How to run
```bash
f1_env\Scripts\activate.bat

# Step 1 — build the dataset
python dataset_builder.py

# Step 2 — open and run model_training.ipynb
```