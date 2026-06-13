# Live Options Analytics Terminal - Implementation Checklist

## Plan items
- [x] Step 1: Refactor `app/finance.py` to add plot-ready outputs, optional caching-friendly signatures, and add utilities for scenario + hedging dataframes/lists.
- [x] Step 2: Extend `app/api.py` with caching/TTL and add plot-ready scenario/hedging endpoints (or enhance existing `/scenario`).
- [x] Step 3: Update `app/dash_app.py` UI:

  - [x] Add real-time refresh via `dcc.Interval`.
  - [x] Add user controls for option type/strike/quantity/expiration/IV.
  - [x] Add charts for P&L scenario matrix + delta-hedging simulation.

- [x] Step 4: Update `README.md` with new usage instructions and refresh/cache behavior.

- [ ] Step 5: Install deps + run server + quick smoke test of endpoints and dashboard rendering.


