QuantPort — Quantitative Portfolio Risk & Return Analysis
A Python-based quantitative finance toolkit for analysing portfolio risk, return, and performance metrics using real or simulated market data.

 Features
Module	Description
Expected Returns	Annualised mean log-returns with rolling 30-day chart
Risk-Return Analysis	Volatility vs return scatter plot per asset
Sharpe Ratio & Risk-Free Rate	Sharpe ratio per asset + Capital Market Line
Efficient Frontier	Monte-Carlo simulation (5,000 portfolios) with Max-Sharpe & Min-Variance optimisation
Maximum Drawdown	Per-asset and portfolio drawdown curves + comparison chart
VaR & CVaR	95% Value-at-Risk and Conditional VaR with return distribution plot

 Output Charts
`expected\_returns.png` — Annualised returns & rolling return chart
`risk\_return.png` — Risk vs return scatter (individual assets)
`sharpe\_cml.png` — Sharpe ratio bars & Capital Market Line
`efficient\_frontier.png` — Efficient frontier & optimal weights
`maximum\_drawdown.png` — Drawdown curves & comparison bar
`var\_cvar.png` — Return distribution with VaR & CVaR

Installation
1. Clone the repository
```bash
git clone https://github.com/pritamvarma61-droid/QuantPort.git
cd QuantPort
```
2. Install dependencies
```bash
pip install -r requirements.txt
```
---
 Usage
```bash
python portfolio\_risk\_analysis\_fixed.py
```
The script will automatically:
Fetch real market data via `yfinance` (if installed)
Fall back to synthetic GBM data if yfinance is unavailable
Generate and save all 6 charts to the project folder

Configuration
Edit these variables at the top of the script to customise the analysis:
```python
TICKERS      = \["AAPL", "MSFT", "GOOGL", "AMZN", "TSLA"]  # Assets to analyse
START        = "2020-01-01"   # Start date
END          = "2024-12-31"   # End date
RF\_ANNUAL    = 0.05           # Risk-free rate (5%)
TRADING\_DAYS = 252            # Trading days per year
N\_PORTFOLIOS = 5\_000          # Monte-Carlo simulations
```
Dependencies
```
numpy
pandas
matplotlib
seaborn
scipy
yfinance
```
Install all at once:
```bash
pip install -r requirements.txt
```
 Project Structure

QuantPort/
│
├── portfolio_risk_analysis_fixed.py   # Main script
├── requirements.txt                   # Dependencies
├── README.md                          # Project documentation
│
└── output charts (generated on run)
├── expected_returns.png
├── risk_return.png
├── sharpe_cml.png
├── efficient_frontier.png
├── maximum_drawdown.png
└── var_cvar.png
Key Concepts
Expected Return — Annualised mean of daily log-returns
Volatility — Annualised standard deviation of returns
Sharpe Ratio — Excess return per unit of risk: `(Return - Risk-Free Rate) / Volatility`
Efficient Frontier — Set of optimal portfolios offering max return for a given risk level
Maximum Drawdown — Largest peak-to-trough decline in portfolio value
VaR — Maximum expected loss at a given confidence level (95%)
CVaR — Average loss beyond the VaR threshold (tail risk)

Author
Pritam Varma
[GitHub](https://github.com/pritamvarma61-droid)

License
This project is licensed under the MIT License — free to use, modify, and distribute.
