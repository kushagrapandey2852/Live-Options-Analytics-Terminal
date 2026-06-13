# Live Options Analytics Terminal

Real-time options analytics terminal with live Greeks, implied volatility surface, P&L scenario matrix, and delta-hedging simulation.

Stack
- Python
- FastAPI
- Dash
- yFinance
- Black-Scholes
- Plotly

## Features
- Fetch live options chain from market data
- Compute Delta, Gamma, Vega, Theta, Rho
- Visualize implied volatility surface
- Build a P&L scenario matrix for option positions
- Simulate delta-hedging and hedging performance
- Minimal aesthetic frontend with responsive charts

## Install

Create a virtual environment and install dependencies:

```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

## Run

```bash
python app/main.py
```

Then open `http://127.0.0.1:8050`.

## Notes
- Uses `yfinance` for live market data (prototype; subject to rate limits).
- Greeks and prices are Black-Scholes for European options.
- Implied volatility is taken from the chain when available, otherwise estimated via Newton iterations.
- Dash dashboard refreshes every ~10s (`dcc.Interval`) and FastAPI endpoints use a small in-memory TTL cache to reduce repeated yfinance calls.
- Designed as a prototype for trading desks, retail platforms, and derivatives brokers.

