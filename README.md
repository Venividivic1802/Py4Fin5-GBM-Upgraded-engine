# GBM Upgraded Engine

A Geometric Brownian Motion (GBM) Monte Carlo simulation engine for stock price forecasting, built as part of the Python for Finance series.

## Overview

The notebook downloads historical price data for a target stock (AAPL by default) via `yfinance`, estimates annualized drift (`mu`) and volatility (`sigma`) from historical daily returns, and simulates future price paths using the GBM stochastic process:

```
S(t) = S(0) * exp((mu - sigma^2 / 2) * t + sigma * W(t))
```

## Features

- Historical data download via `yfinance`
- Annualized drift and volatility estimation from daily log/percentage returns
- Vectorized Monte Carlo simulation of GBM price paths (`numpy`)
- Summary statistics (mean/std of simulated returns) and median-path selection

## Requirements

- numpy
- pandas
- matplotlib
- yfinance

Install with:

```bash
pip install numpy pandas matplotlib yfinance
```

## Usage

Open `Py4Fin5_GBM upgraded engine.ipynb` in Jupyter and run all cells. Adjust the ticker, date range, or simulation parameters (`days`, `n_paths`, `dt`) in the `simulate_gbm` call as needed.
