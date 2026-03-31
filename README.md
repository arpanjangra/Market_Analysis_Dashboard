# Market Analysis Dashboard
A quantitative financial analysis web application built with Python and Streamlit. This dashboard provides real-time market data extraction, statistical metric computation, and interactive visualizations to evaluate the risk and historical performance of publicly traded assets.

This project demonstrates practical applications of financial data science, focusing on tools and methodologies used in quantitative analysis and asset management.

## Project Objective

Designed as a robust analytical tool, this dashboard automates the calculation of essential risk-adjusted performance metrics. It serves to bridge the gap between statistical theory and live market applications by dynamically processing Yahoo Finance data into actionable insights through an intuitive, dark-themed UI.

## Key Features
* **Real-Time Data Pipeline:** Utilizes the yfinance API to reliably fetch historical daily market data (Open, High, Low, Close, Volume) across user-defined time horizons (1Y, 2Y, 5Y, YTD).
* **Quantitative Engine:** Implements vectorized operations via pandas and numpy to calculate critical financial statistics:
* **Daily Logarithmic Returns:** For continuous compounding analysis.
* **Annualized Volatility:** Measures historical price fluctuation and asset risk (assuming 252 trading days).
* **Sharpe Ratio:** Evaluates risk-adjusted return (defaulting to a 2% risk-free rate).
* **Maximum Drawdown:** Identifies the largest historical peak-to-trough drop.

## Financial Formulas:
* **log returns**  $$R_t = \ln( \frac{P_t}{P_{t-1}})$$
* **Sharpe Ratio:**  $$S_a = \frac{E[R_a - R_b]}{\sigma_a}$$
* **Annualized Volatility** $$\sigma_{ann} = \sigma_{daily} \times \sqrt{252}$$
* **Maximum Drawdown** $$MDD = \min \left( \frac{P_t - P_{max}}{P_{max}} \right)$$

## Interactive Visualizations:
* Candlestick price chart (Plotly)
* 50-day Moving Average overlay
* Trading Volume bar chart
* Daily Log Returns time series

## Usage Guide
1. Navigate to the Dashboard Configuration sidebar on the left.
2. Enter a valid stock ticker symbol (e.g., AAPL, MSFT, SPY).
3. Select your desired lookback window from the Time Period dropdown menu.
4. The dashboard will automatically fetch the data, compute the quantitative metrics, and update the KPI cards and interactive charts in real-time.

## Limitations
* Relies on Yahoo Finance API (data availability may vary)
* Basic single-asset analysis (no portfolio optimization yet)

## Future Enhancements 
* Portfolio Optimization (Mean-Variance, Efficient Frontier)
* Value at Risk (VaR) & Expected Shortfall
* Machine Learning-based price prediction
* Backtesting trading strategies
* Multi-asset comparison dashboard
* Factor models (CAPM, Fama-French)
