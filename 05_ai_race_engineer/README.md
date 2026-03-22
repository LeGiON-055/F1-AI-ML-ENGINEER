# Part 5 — AI Race Engineer Chatbot

An AI-powered chatbot that answers natural language
questions about F1 races using live FastF1 telemetry data.

## What it does

Ask it questions like:
- "Who had the fastest lap at Monza 2023?"
- "Compare Verstappen and Hamilton tyre strategy at Silverstone"
- "Which driver had the best race pace in Singapore 2023?"

It responds with data, charts and a plain English explanation.

## How it works

1. User asks a question in natural language
2. LLM understands the intent and extracts race/driver/metric
3. FastF1 fetches the relevant live race data
4. LLM formats the answer with data and explanation

## Tech stack

- Python 3.11
- FastF1 — live F1 telemetry data
- LLM API (Claude / OpenAI)
- RAG (Retrieval Augmented Generation)

## Files

| File | Description |
|------|-------------|
| app.py | Main chatbot application |
| chatbot.ipynb | Development and testing notebook |
| README.md | This file |

## How to run
```bash
f1_env\Scripts\activate.bat

# Add your API key to .env file first:
# ANTHROPIC_API_KEY=your_key_here

python app.py
```

## Demo

> Screenshot or GIF of chatbot in action — added after completion