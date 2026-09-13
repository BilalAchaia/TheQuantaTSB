# TheQuantaTSB

> **Automated Quantitative Trading Strategy & Machine Learning Backtesting Framework**

---

## Overview
**TheQuantaTSB** is a Python-based quantitative research engine designed to build, test, and simulate algorithmic trading strategies on financial time-series data without lookahead bias.

---

## System Workflow

```
[ Market Data ] ──> [ Feature Engineering ] ──> [ ML / Strategy Logic ] ──> [ Backtester & Risk ] ──> [ Performance Metrics ]
```

---

## Project Structure

```text
TheQuantaTSB/
├── assets/                  # Performance plots and metrics
├── config/                  # Hyperparameters and strategy settings
├── data/                    # Historical market datasets
├── docs/                    # Architecture notes
├── models/                  # ML models and weights
├── scripts/                 # Utility automation scripts
├── src/                     # Core backtest and execution engine
├── strategies/              # Algorithmic trading strategies
├── tests/                   # Automated unit tests
├── training_results_auto_v7/# Benchmark logs and outputs
├── requirements.txt         # Dependencies
└── run.py                   # Main pipeline entry point
```

---

## Core Capabilities

- **Time-Series Modeling:** Automated preprocessing and feature extraction on raw financial data.
- **Pluggable Strategies:** Modular architecture to define custom technical indicators or ML-driven signals.
- **Risk & Execution Simulator:** Simulates trade fills, position sizing, and maximum drawdown constraints.
- **Experiment Logs:** Historical evaluation and metrics saved automatically in `training_results_auto_v7/`.

---

## Quickstart

### 1. Setup Environment
```bash
git clone https://github.com/BilalAchaia/TheQuantaTSB.git
cd TheQuantaTSB
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 2. Run Pipeline
```bash
python run.py
```

### 3. Run Tests
```bash
pytest tests/
```

---

## Disclaimer
This project is strictly for **academic and research purposes**. It is not financial or investment advice.

---

## Author
- **Bilal Achaia** — [@BilalAchaia](https://github.com/BilalAchaia)
```
