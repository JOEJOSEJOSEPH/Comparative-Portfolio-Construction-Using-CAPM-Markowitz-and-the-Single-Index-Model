# Comparative-Portfolio-Construction-Using-CAPM-Markowitz-and-the-Single-Index-Model

📘 README.md
📌 Project Title

Comparative Portfolio Construction Using CAPM, Markowitz, and the Single Index Model

📌 Project Overview

This project implements and compares classical asset pricing and portfolio construction models to study how different assumptions about risk and covariance affect portfolio optimization and performance. Using Indian equity market data, the project evaluates CAPM, Markowitz mean–variance optimization, and the Single Index Model (SIM) in a unified and reproducible Python pipeline.

The objective is to understand the risk–return trade-off, estimation risk, and practical robustness of each model.

📌 Motivation

While Markowitz mean–variance optimization is theoretically optimal, it is highly sensitive to estimation errors in expected returns and covariances. This project investigates whether simpler factor-based models like the Single Index Model provide more stable and practical portfolio allocations, and how CAPM-implied expected returns compare with historical averages.

📌 Data

Source: Yahoo Finance

Market: Indian equity market

Assets: RELIANCE, TCS, INFY, HDFCBANK, ICICIBANK

Market Index: NIFTY 50 (^NSEI)

Frequency: Daily

Period: 2018–2023

Returns: Log returns

📌 Methodology
1️⃣ Data Preparation

Download adjusted closing prices

Align trading calendars

Compute daily log returns

Perform basic diagnostics and visualization

2️⃣ CAPM (Capital Asset Pricing Model)

Estimate asset betas using time-series regressions

Interpret systematic vs idiosyncratic risk

Compute CAPM-implied expected returns

3️⃣ Markowitz Mean–Variance Optimization

Estimate full covariance matrix

Construct the efficient frontier

Identify Minimum Variance and Tangency portfolios

Analyze portfolio weights and concentration

4️⃣ Single Index Model (SIM)

Decompose returns into market and residual components

Construct factor-based covariance matrix

Build SIM minimum variance portfolio

Compare stability and risk with Markowitz portfolios

5️⃣ Performance Evaluation

Compare portfolios using:

Annualized return

Annualized volatility

Sharpe ratio

Maximum drawdown

Benchmark against equal-weighted portfolio

📌 Key Findings

Markowitz portfolios achieve minimum theoretical variance but are sensitive to estimation error.

SIM portfolios exhibit more stable and interpretable weights due to reduced covariance estimation noise.

Equal-weight portfolios remain strong benchmarks due to their robustness.

CAPM explains systematic risk well but does not fully capture cross-sectional return differences.

📌 Folder Structure
data/
├── prices.csv
├── asset_returns.csv
├── market_returns.csv
├── capm_parameters.csv
├── markowitz_weights.csv
├── sim_vs_markowitz_weights.csv
└── final_performance_comparison.csv

notebooks/
├── 01_data_collection_and_returns.ipynb
├── 02_CAPM_beta_estimation.ipynb
├── 03_Markowitz_portfolio_optimization.ipynb
├── 04_single_index_model.ipynb
└── 05_performance_evaluation.ipynb

📌 How to Run

Clone the repository

Run notebooks sequentially from 01 to 05

All intermediate outputs are saved to the data/ folder

No notebook requires re-downloading data once prepared

📌 Tools & Libraries

Python

pandas, numpy

matplotlib

statsmodels

scipy

yfinance

📌 Extensions (Future Work)

Out-of-sample backtesting

Rolling beta estimation

Transaction cost modeling

Multi-factor asset pricing models

📌 Conclusion

This project demonstrates how classical asset pricing models translate into practical portfolio construction decisions. By comparing Markowitz, CAPM, and SIM frameworks, the project highlights the trade-off between theoretical optimality and practical robustness in portfolio management.

🎯 INTERVIEW PREPARATION STORY (MEMORIZE THIS)
How did you come up with this project?

I wanted to revise my Security Analysis and Portfolio Management concepts by implementing them in a practical and interview-relevant way. So I built a complete pipeline starting from data collection to portfolio construction and performance evaluation using classical asset pricing models.

Walk me through your project.

I first collected Indian equity data from Yahoo Finance and constructed clean log return series. I then estimated CAPM betas using time-series regressions to understand systematic risk. Using these returns and covariances, I implemented Markowitz mean–variance optimization and constructed the efficient frontier. Since Markowitz is sensitive to estimation error, I also implemented the Single Index Model, which uses a factor-based covariance structure. Finally, I compared the performance of these portfolios using risk-adjusted metrics and drawdowns.

Why did you use SIM instead of Markowitz?

Markowitz requires estimating a full covariance matrix, which becomes unstable with limited data. SIM reduces estimation risk by modeling covariances through a single market factor, producing more stable and interpretable portfolios.

What did you learn from this project?

I learned that theoretical optimality does not always translate into practical performance. Simpler models often perform competitively because they avoid overfitting and estimation noise.

If given more time, how would you improve it?

I would add out-of-sample testing, transaction costs, and extend the framework to multi-factor models such as Fama–French.

🏁 FINAL ONE-LINER (USE THIS IN INTERVIEWS)

“I built an end-to-end portfolio construction framework comparing CAPM, Markowitz, and the Single Index Model using Indian equity data, focusing on risk–return trade-offs and estimation risk.”
