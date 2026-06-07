# MLB Stats Chatbot

An AI-powered chatbot that lets users ask natural-language questions about historical MLB batting statistics and receive pandas-based answers.

## Overview

MLB Stats Chatbot helps users explore historical MLB player batting data using natural-language questions. The project uses Gemini to interpret a user’s question, generate a pandas query, run that query against an MLB dataset, and return a short explanation of the result.

Example questions:
- Who had the most home runs in 1990?
- Which players had the best OPS with at least 400 at-bats?
- Who were the top base stealers in 1988?

## Features

- Ask natural-language questions about MLB batting stats
- Uses Gemini to generate pandas queries
- Runs generated code against a pandas DataFrame
- Includes a data dictionary explaining available MLB statistics
- Calculates advanced stats such as:
  - Batting Average
  - On-Base Percentage
  - Slugging Percentage
  - OPS
  - Home runs per game
  - Strikeout rate

## Dataset

The chatbot uses historical MLB batting data with one row per player, season, and team stint. The dataset is a combination of two datasets downloaded from Kaggle and it covers seasons from 1871 through 2015 and contains about 101,332 rows.

Important note: players traded mid-season may appear more than once for the same season, so season and career leaderboards need to account for multiple stints.

## Tech Stack

- Python
- pandas
- Google Gemini API
- Jupyter Notebook
- HTML export

## How It Works

1. The user asks a baseball stats question.
2. The app builds a prompt using:
   - the user’s question
   - dataset rules
   - a data dictionary
3. Gemini generates a short pandas query.
4. The query runs against the MLB DataFrame.
5. The chatbot returns a concise answer.

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/mlb-stats-chatbot.git
cd mlb-stats-chatbot
