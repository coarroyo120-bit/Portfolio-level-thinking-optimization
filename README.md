# 📘 Project 2: BTC–ETH Portfolio Optimization (2018–2025)

This project builds on the BTC vs ETH performance analysis by exploring how **different allocations between Bitcoin and Ethereum** affect long-term return, risk, and investor survivability.

Instead of asking *“Which coin is better?”*, this project answers a more practical question:

> **How should an investor allocate between BTC and ETH to maximize returns while controlling risk?**

---

## 🎯 Objectives

This analysis evaluates how mixed BTC/ETH portfolios behave under different weightings, from conservative to aggressive:

- **100% BTC / 0% ETH**
- **50% BTC / 50% ETH**
- **0% BTC / 100% ETH**
- And 9 intermediate allocations (10% increments)

For each portfolio, we compute:

- **Annualized Return (CAGR)**
- **Annualized Volatility**
- **Sharpe Ratio** (risk-adjusted return)
- **Maximum Drawdown** (worst crash)

We then visualize the **Efficient Frontier**, showing the risk–return tradeoff across all allocations.

---

## 📊 Data Source

Same clean dataset used in Project 1:

- BTC: `BTC-USD`
- ETH: `ETH-USD`
- Frequency: Daily price history
- Date range: **2018–2025**
- Source: Yahoo Finance via `yfinance`

---

## 🧠 Methodology

### 1️⃣ Download BTC & ETH daily prices  
Using the `yfinance` API.

### 2️⃣ Compute daily returns  
Percentage changes for BTC and ETH.

### 3️⃣ Build portfolios  
Portfolio returns =  
`w_BTC * BTC_returns + w_ETH * ETH_returns`

Weights tested in **10% increments**.

### 4️⃣ Compute performance metrics  
For each portfolio:
- CAGR (annualized return)
- Volatility (annualized standard deviation)
- Sharpe ratio (risk-adjusted)
- Maximum drawdown (peak-to-trough loss)

### 5️⃣ Plot the Efficient Frontier  
Risk (volatility) on X-axis  
Return (CAGR) on Y-axis  
Each point = one BTC–ETH allocation.

---

## 📈 Key Findings

### ✔ A mixed BTC–ETH portfolio improves risk-adjusted performance  
Portfolios between **40–70% BTC** typically show:

- **Higher Sharpe ratios** than pure BTC or pure ETH  
- **Lower volatility** than holding ETH alone  
- **Less severe drawdowns**

### ✔ 100% ETH has highest upside **but catastrophic crashes**  
ETH still delivers the strongest bull-market performance,  
but also suffered a **–94% drawdown** — emotionally devastating for most investors.

### ✔ 100% BTC is the most stable with the lowest drawdown  
BTC remains the **psychological anchor** of the portfolio.

### ✔ A 50/50 BTC–ETH portfolio often balances growth and survival  
In several time periods, it offers:

- Better Sharpe ratio  
- Reduced drawdown  
- Strong long-term compounding  

This suggests that **portfolio construction > single-asset picking**.

---

## 📉 Efficient Frontier (Risk vs Return)

The Efficient Frontier chart visualizes how risk and return evolve as we change BTC/ETH weightings.

- Left side → lower risk portfolios (more BTC)  
- Right side → higher risk portfolios (more ETH)  
- Upper curve → optimal risk-return combinations

This is one of the most widely used tools in portfolio theory — and now you can apply it to crypto.

*Chart file exported as:*  
`charts/btc_eth_efficient_frontier.png`

---
🧩 Interpretation

This project demonstrates that risk-adjusted returns improve when BTC and ETH are combined, compared to holding either one alone.

Key insight:

The optimal crypto portfolio isn’t “BTC or ETH.”
It’s “BTC AND ETH — in the right proportion.”

This reinforces a core principle of portfolio design:

Bitcoin = stability

Ethereum = upside

Blending them = strategy

🚀 Future Enhancements

Add ETH staking yield to improve ETH total return

Include more assets (SOL, AVAX, ADA, stablecoins)

Perform rebalancing backtests (monthly, quarterly)

Plot rolling Sharpe ratio over time

Build an interactive Streamlit dashboard for end users

Explore a 3-asset efficient frontier (BTC–ETH–SOL)

📬 Contact

Insights Vault — Data-driven crypto, not hype
TikTok: @insights.vault
Instagram: @insights.vault
YouTube: @InsightsVault

⚠️ Disclaimer

This analysis is for educational purposes only.
It is not financial advice.
