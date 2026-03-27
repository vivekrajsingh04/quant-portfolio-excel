# 📊 Quantitative Portfolio Analysis — Excel Models

> Portfolio Optimization, Monte Carlo Simulation & Bollinger Bands analysis built entirely in Excel (Google Sheets compatible).

---

## 📌 Project Overview

This project demonstrates **quantitative finance concepts** using a single Excel workbook with multiple analysis sheets. The models are built on **NIFTY 50 historical data** and a **2-asset portfolio (SBIN + ICICI Bank)**.

### Key Analyses

| Analysis | Description |
|----------|-------------|
| **Portfolio Optimization** | Markowitz Mean-Variance optimization for a 2-asset portfolio |
| **Monte Carlo Simulation** | 25 simulated price paths over 20 days to estimate future risk |
| **Bollinger Bands** | NIFTY 50 price with ±2 standard deviation bands for trend analysis |
| **Efficient Frontier** | Risk vs. Return tradeoff curve across different weight combinations |

---

## 🧠 Concepts & Methodology

### 1. Portfolio Optimization (Markowitz Model)
- Computed **daily returns** for SBIN and ICICI Bank
- Calculated **standard deviation**, **covariance**, and **correlation**
- Built a **covariance matrix** to quantify asset co-movement
- Generated **50 portfolio combinations** with varying weights (0% → 100%)
- Computed **portfolio return** and **portfolio risk (std dev)** for each combination
- Plotted the **Efficient Frontier** to identify optimal risk-return tradeoffs

### 2. Monte Carlo Simulation
- Simulated **25 independent price paths** over 20 trading days
- Starting price: ₹18,065 (NIFTY 50)
- Used **random normal returns** calibrated to historical volatility
- Result: Distribution of possible future prices to estimate **Value at Risk (VaR)**

### 3. Bollinger Bands
- Calculated **20-day moving average** of NIFTY 50 closing prices
- Plotted **upper band** (MA + 2σ) and **lower band** (MA − 2σ)
- Used to identify **overbought/oversold conditions** and **mean reversion signals**

---

## 📸 Screenshots

### Bollinger Bands — NIFTY 50
![Bollinger Bands — NIFTY 50 with ±2 Std Dev Bands](images/bollinger_bands.svg?v=2)

### Efficient Frontier — Portfolio Return vs. Risk
![Efficient Frontier — Portfolio Return vs STD Dev](images/efficient_frontier.svg?v=2)

---

## 📂 Project Structure

```
quant-portfolio-excel/
├── data/                        # Raw data exports (CSV)
├── excel/
│   └── SFM_03 MonteCarlo.xlsm  # Full workbook with all sheets
├── images/
│   ├── bollinger_bands.svg      # Bollinger Bands chart
│   └── efficient_frontier.svg   # Efficient Frontier chart
├── .gitignore
└── README.md
```

---

## 📋 Sheets in the Workbook

| Sheet | What it Contains |
|-------|-----------------|
| Historical Data | NIFTY 50 daily closing prices with date index |
| Returns & Stats | Daily returns, std dev, covariance for SBIN & ICICI |
| Portfolio Weights | 50 weight combinations with portfolio return & risk |
| Efficient Frontier | Chart plotting risk vs. return for all portfolios |
| Monte Carlo | 25 simulated price paths over 20 days |
| Bollinger Bands | NIFTY 50 with 20-day MA ± 2σ bands |

---

## ⚙️ Tools & Formulas Used

- **Excel / Google Sheets** — primary tool
- Key formulas: `STDEV`, `COVARIANCE`, `AVERAGE`, `RAND`, `NORMINV`
- Charting: Scatter plots (Efficient Frontier), Line charts (Bollinger Bands, Monte Carlo)

---

## 📈 Key Results

- **Diversification effect**: Portfolio risk is lower than individual stock risk due to imperfect correlation
- **Optimal portfolio**: Identified minimum-variance portfolio from the Efficient Frontier
- **Monte Carlo**: Price paths show wide dispersion — demonstrates importance of risk management
- **Bollinger Bands**: Price tends to revert to the mean after touching the bands

---

## 🚀 Future Improvements

- [ ] Convert Excel models to **Python** (pandas, numpy, matplotlib)
- [ ] Add **Sharpe Ratio** optimization
- [ ] Increase Monte Carlo simulations to **10,000 paths**
- [ ] Add **VaR (Value at Risk)** and **CVaR** calculations
- [ ] Implement **Black-Scholes** option pricing model

---

## 👤 Author

**Vivek**

---

## 📜 License

This project is open source and available under the [MIT License](LICENSE).
