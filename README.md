# 📊 Bitcoin Market Sentiment vs Trader Performance

## Project Overview
This project analyzes the relationship between **Bitcoin market sentiment (Fear vs Greed)** and **real trader behavior and performance** using historical trading data.  
Instead of predicting prices, the focus is on **behavioral finance** — understanding how emotions influence trading activity, risk exposure, and profitability.

The goal is to extract **actionable insights** that can support **smarter, sentiment-aware trading strategies**.

---

## Objectives
- Analyze how Fear and Greed impact trader behavior
- Study risk-taking patterns under different sentiment regimes
- Evaluate trader performance and loss concentration
- Translate findings into practical trading recommendations

---

## Datasets Used

### 1️⃣ Bitcoin Market Sentiment (Fear–Greed Index)
**Columns:**
- `date`
- `classification` (Fear / Greed)

### 2️⃣ Historical Trader Data (Hyperliquid)
**Key Columns:**
- `account`
- `symbol`
- `side`
- `size_usd`
- `execution_price`
- `timestamp`
- `closedPnL` (realized profit & loss)

---

## Project Structure

### 1️⃣ data/
- Stores all datasets used in the project  
- Raw data is never modified to maintain data integrity  

**Subfolders:**
- **raw/**
  - Original trader execution dataset (`historical_data.csv`)
  - Bitcoin Fear & Greed sentiment dataset (`fear_greed_index.csv`)
- **processed/**
  - Cleaned and merged dataset used for all analysis (`merged_trader_sentiment.csv`)

---

### 2️⃣ notebooks/
- Contains all Jupyter notebooks used for analysis and insight generation  
- Notebooks follow a logical execution flow from data preparation to insights  

**Notebooks:**
- **data_loading_and_cleaning.ipynb**
  - Data loading and schema inspection  
  - Timestamp standardization and dataset merging  

- **sentiment_analysis_overview.ipynb**
  - Distribution of Fear vs Greed  
  - Temporal sentiment trends and regime persistence  

- **trader_behavior_analysis.ipynb**
  - Trade frequency analysis  
  - Position size and directional bias under sentiment regimes  

- **performance_vs_sentiment.ipynb**
  - Profit and loss (PnL) comparison  
  - Win-rate and loss severity analysis  

- **leverage_risk_analysis.ipynb**
  - Extreme loss concentration analysis  
  - Drawdown and risk proxy evaluation  

- **insights_and_strategy_recommendations.ipynb**
  - Consolidated insights from all analyses  
  - Actionable, sentiment-aware trading strategy recommendations  

---

### 3️⃣ visuals/
- Stores plots and figures exported from notebooks  
- Used for documentation, presentations, and reports (optional)

---

### 4️⃣ README.md
- Project documentation  
- Explains problem statement, methodology, insights, and conclusions  





---

## Analysis Workflow

### 🔹 Step 1: Data Loading & Cleaning
- Standardized column names
- Unified timestamp formats
- Merged sentiment and trader data by date
- Created a clean processed dataset for reproducibility

---

### 🔹 Step 2: Sentiment Landscape Analysis
- Distribution of Fear vs Greed periods
- Temporal sentiment trends
- Sentiment regime persistence (streaks)

---

### 🔹 Step 3: Trader Behavior Analysis
- Trade frequency under Fear vs Greed
- Position size comparison
- Buy/Sell directional bias
- Risk proxies used when leverage data was unavailable

---

### 🔹 Step 4: Performance vs Sentiment
- Mean vs median PnL comparison
- Win rate by sentiment regime
- Loss severity analysis
- Trade size vs PnL relationship

---

### 🔹 Step 5: Risk & Drawdown Analysis
- Bottom 5% extreme loss concentration
- Account-level drawdown proxy
- Relationship between trade size and loss magnitude

---

### 🔹 Step 6: Insights & Strategy Recommendations
- Behavioral patterns translated into trading strategies
- Sentiment-aware risk controls
- Rule-based risk overlay concepts

---

## Key Insights

- **Trading activity increases significantly during Greed**, indicating overconfidence and FOMO
- **Extreme losses cluster during Greed regimes**, increasing downside risk
- **Median PnL is often better during Fear**, despite lower activity
- Larger trade sizes do **not guarantee higher profitability**
- Emotional regimes impact outcomes more than trade direction alone

---

## Strategy Recommendations

- Reduce position sizes during Greed phases  
- Introduce trade frequency limits during high-sentiment periods  
- Favor risk–reward setups during Fear regimes  
- Monitor extreme-loss thresholds as early warning signals  

---

## Why This Project Stands Out
- Focuses on **behavioral finance**, not price prediction
- Uses **real trader execution data**
- Adapts intelligently to missing leverage data using risk proxies
- Emphasizes **explainability and decision-making insights**
- Designed like a real-world analytics project, not a toy dataset

---

## Tech Stack
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Jupyter Notebook

---

## Conclusion
Market sentiment significantly influences trader behavior, risk exposure, and performance.  
By integrating sentiment-aware controls into trading systems, traders can **reduce downside risk without relying on price forecasting models**.

---


