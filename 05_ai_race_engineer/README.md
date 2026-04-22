# Part 5 - AI Race Engineer Chatbot

## Overview
An AI-powered F1 Race Engineer chatbot that uses real F1 data
from 2020-2024 seasons combined with a free Groq LLM to answer
strategy questions, tyre management queries, and race craft advice.

## Files
| File | Description |
|------|-------------|
| `race_engineer.ipynb` | Main notebook - all 4 cells |
| `chat_log.txt` | Saved chat session log |
| `part5_summary_card.png` | Visual summary card |
| `.env` | API key (never pushed to GitHub) |

## How It Works

### Step 1 - Load Real F1 Data
Loads all Kaggle F1 CSVs and computes:
- Driver stats (wins, podiums, avg finish, total points)
- Constructor stats (wins, podiums, total points)
- Pit stop statistics (avg stops, avg time, fastest, slowest)

### Step 2 - Build AI Context
Summarizes real F1 data into a context string that is injected
into every API call as a system prompt. This gives the AI real
data to base its answers on.

### Step 3 - Groq API Integration
Uses the Groq API (free) with llama-3.3-70b-versatile model.
Every question includes:
- Full F1 data context (system prompt)
- Complete conversation history (AI has memory)

### Step 4 - Interactive Chatbot Loop
User types F1 strategy questions and gets expert AI responses.
Commands available:
- Type any F1 question to get an answer
- Type 'clear' to reset conversation history
- Type 'quit' or 'exit' to stop

## Tech Stack
| Component | Technology |
|-----------|------------|
| LLM Model | llama-3.3-70b-versatile |
| API Provider | Groq (Free tier) |
| Data Source | Kaggle F1 Dataset 2020-2024 |
| Memory | Full conversation history per session |
| Libraries | groq, pandas, python-dotenv, matplotlib |

## Data Loaded Into AI Context
- Seasons covered : 2020-2024
- Total races     : 106
- Race entries    : 2120+
- Pit stop records: 8500+
- Qualifying rows : 2100+

## Example Questions You Can Ask
- Who has been the most dominant driver from 2020 to 2024?
- What is the ideal pit stop strategy for Monaco?
- If Verstappen starts P3 at Monza what strategy wins?
- Which constructor has the best pit stop performance?
- How does grid position affect race win probability?
- What tyre strategy works best in wet conditions?
- Compare Hamilton vs Verstappen head to head stats
- When is the best lap to pit under a safety car?

## Setup
1. Get a free Groq API key at https://console.groq.com
2. Create a .env file with: GROQ_API_KEY=your-key-here
3. Install groq: pip install groq
4. Run all cells in race_engineer.ipynb