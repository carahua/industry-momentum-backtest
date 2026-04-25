# Industry Momentum Strategy Backtest

A systematic backtest of cross-sectional momentum strategy across 10 US industry portfolios (2019–2026), with volatility-weighted risk management.

## Strategy Logic

Each month:
1. Calculate trailing 12-month return for each industry
2. **Long** the top-performing industry
3. **Short** the worst-performing industry
4. Position size adjusted by historical volatility (target 15% annualised vol)

## Data Source

Fama-French 10 Industry Portfolios — [Kenneth French Data Library](https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html)

## Results

| | Baseline Strategy | Risk-Managed Strategy |
|---|---|---|
| Annualised Return | 31.1% | 14.8% |
| Sharpe Ratio | 0.78 | 0.85 |
| Max Drawdown | -65.4% | -29.0% |

Risk management via volatility-weighting reduced drawdown by more than half while improving the Sharpe ratio.

## Key Findings

- Momentum effect is stronger on the long side (38.2% annualised) than the short side (7.1%)
- Volatility-weighted position sizing significantly improves risk-adjusted returns
- Large drawdown in 2023 reflects momentum crash during sharp sector rotation

## Tools

Python · pandas · numpy · matplotlib · pandas_datareader
