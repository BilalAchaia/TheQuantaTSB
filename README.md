# TheQuantaTSB
Quantitative Trading Strategy and Machine Learning Backtesting Framework

## Overview
TheQuantaTSB is a Python-based quantitative research and backtesting framework designed for modeling, evaluating, and simulating algorithmic trading strategies on financial time-series data. 

The architecture separates data preprocessing, predictive modeling, strategy formulation, and backtest execution into isolated modules, enabling systematic evaluation of trading hypotheses while minimizing lookahead and survivorship biases.

## System Architecture

The pipeline operates sequentially across four primary stages:

1. Data Ingestion and Preprocessing:
   Loads historical market data, handles missing records, and computes domain-specific technical indicators and statistical features.

2. Statistical and Machine Learning Models (`models/`):
   Trains and evaluates predictive algorithms on processed historical features to generate market regime or price direction signals.

3. Strategy and Execution Logic (`strategies/`):
   Applies deterministic risk rules, entry/exit criteria, and position sizing based on model inference and technical thresholds.

4. Backtesting and Metric Logging (`src/`, `training_results_auto_v7/`):
   Simulates order execution and outputs quantitative performance indicators, including cumulative returns, maximum drawdown, and volatility metrics.

## Repository Structure

TheQuantaTSB/
├── assets/                  # Architecture diagrams and performance charts
├── config/                  # Configuration parameters and hyperparameters
├── data/                    # Historical and processed datasets
├── docs/                    # Technical documentation
├── models/                  # ML models, training scripts, and serialized weights
├── scripts/                 # Automation and utility scripts
├── src/                     # Core backtesting engine, data loaders, and metrics
├── strategies/              # Quantitative trading strategy implementations
├── tests/                   # Unit and integration tests
├── training_results_auto_v7/# Backtest logs, performance reports, and outputs
├── requirements.txt         # Project dependencies
└── run.py                   # Main pipeline entry point
Core Modules
1. Data Processing (src/data/)
Handles data cleaning, normalization, and feature generation (e.g., moving averages, volatility indicators, and momentum oscillators) stored under data/.
2. Strategy Engine (strategies/)
Contains modular classes defining trading rules. Each strategy implements standardized interfaces for receiving market updates and emitting trade signals.
3. Model Training (models/)
Integrates time-series forecasting and classification models. Hyperparameters and runtime configurations are decoupled into config/ files.
4. Backtest Evaluation (training_results_auto_v7/)
Contains the output of historical simulation runs, including trade logs, equity curves, and performance summaries across test horizons.
Getting Started
Requirements
Python 3.9+
Linux, macOS, or Windows
Installation
Clone the repository:
code
Bash
git clone https://github.com/BilalAchaia/TheQuantaTSB.git
cd TheQuantaTSB
Create and activate a virtual environment:
code
Bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install dependencies:
code
Bash
pip install -r requirements.txt
Execution
To run the primary backtest and modeling pipeline:
code
Bash
python run.py
To run the test suite:
code
Bash
pytest tests/
Research Disclaimer
This software is developed strictly for academic, educational, and research purposes. It does not constitute financial, investment, or trading advice.
Author
Bilal Achaia
GitHub: @BilalAchaia
