# **Regime-Based Portfolio Optimization Using Hidden Markov Models (HMMs)**

### **Project Overview**
This project explores the use of Hidden Markov Models (HMMs) to classify market regimes and optimize portfolio returns based on sector-specific performance. Inspired by the paper **"Regime-Switching Models and Applications in Portfolio Optimization" by M. Wang et al.**, the project analyzes daily returns and volatility of selected S&P 500 sectors to identify distinct market regimes (bull, bear, neutral) and uses these insights to dynamically allocate weights to sectors, enhancing portfolio performance.

### **Key Highlights**
- **Market Regime Classification**: 
  - A 3-state HMM was trained to identify bull, bear, and neutral market regimes using historical data.
  - Regime identification was validated against a 5-state model, with the 3-state model proving more robust and interpretable.
  
- **Portfolio Optimization**:
  - Sector-based returns from **Technology (XLK)**, **Utilities (XLU)**, **Financials (XLF)**, **Energy (XLE)**, and **Healthcare (XLV)** were analyzed.
  - Dynamic portfolio weights were assigned based on sector performance within each regime.
  - Benchmarked against an equal-weighted portfolio.

- **Performance Metrics**:
  - **Sharpe Ratio**: Risk-adjusted return over daily standard deviation of returns.
  - **Sortino Ratio**: Focused on downside risk.
  - **Calmar Ratio**: Annualized return to maximum drawdown.
  - **Max Drawdown**: Largest observed loss from peak to trough.

### **Results**
- **Dynamic Portfolio**:
  - Achieved higher Sharpe and Sortino ratios compared to the equal-weighted portfolio.
  - Demonstrated resilience with lower maximum drawdown in volatile market conditions.
  
- **Regime Insights**:
  - Sector-specific performance varied significantly across regimes:
    - Technology outperformed during bull markets.
    - Utilities provided stability in bear markets.

### **How It Works**
1. **Data Collection**:
   - Historical data for selected S&P 500 sectors downloaded from Yahoo Finance.
   - Daily returns and volatility computed.

2. **HMM Training**:
   - A Gaussian HMM with 3 hidden states was trained on historical data.
   - Regime labels assigned to each data point (bull, bear, neutral).

3. **Portfolio Construction**:
   - Sector performance in each regime was analyzed.
   - Weights for dynamic portfolio optimization were derived based on regime-specific performance.

4. **Performance Evaluation**:
   - Portfolio performance metrics (Sharpe, Sortino, Calmar ratios) compared against an equal-weighted benchmark.

### **Key Findings**
- Dynamic regime-based allocation consistently outperformed the equal-weighted portfolio in risk-adjusted returns.
- The regime-based strategy capitalized on sector strengths during favorable regimes while minimizing exposure to weak sectors during downturns.

### **Visualization**
- **Market Regimes**: Scatterplots showing daily returns categorized by regimes.
- **Cumulative Returns**: Growth of $1 invested in the regime-based vs. equal-weighted portfolio.
- **Sector-Specific Performance**: Visual comparisons of sector returns across different market regimes.

### **Main Libraries**
- **Python**:
  - `hmmlearn`: Hidden Markov Model implementation.
  - `pandas`, `numpy`: Data manipulation and computation.
  - `matplotlib`: Data visualization.
  - `yfinance`: Sector data extraction.

---

### **How to Run**
1. Clone the repository:
   ```bash
   https://github.com/tilaskabengele/quant_finance_project

Make sure the required libraries are installed in your environment.
