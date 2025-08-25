# Simple Moving Average (SMA) Crossover Strategy

This project implements and backtests a **Simple Moving Average (SMA) crossover** trading strategy using historical equity and crypto data.  
The strategy is compared against Buy & Hold across different time periods, assets, and SMA windows (10/50, 20/100, 50/200).

## Key Features
- Data sourced via yfinance (auto-adjusted prices)  
- Fully vectorized signal generation (no look-ahead bias)  
- Performance metrics: CAGR, volatility, Sharpe ratio, max drawdown  
- Visualizations: price with SMAs, buy/sell signals, equity curves, drawdowns  

## Results
On SPY (2000–present), SMA crossovers achieved **lower volatility and smaller drawdowns** than Buy & Hold, with a slightly lower CAGR but higher Sharpe ratio.  
Tests on other assets (AAPL, BTC-USD) and periods showed the same pattern in most cases:  
- **Bear markets:** SMA provided downside protection  
- **Bull markets:** strategy lagged due to missed rallies and whipsaws in volatile conditions  

## How to Run
```bash
pip install -r requirements.txt
jupyter lab
```
Open sma_crossover_strategy.ipynb and run all cells,
or view the pre-run version with plots: sma_crossover_strategy.rendered.ipynb

## About 
Author: William Bradbury  
Affiliation: BSc Mathematics, University of Warwick
