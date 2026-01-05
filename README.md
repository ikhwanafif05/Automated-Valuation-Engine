# Automated Valuation & Comps Engine

### 🚀 Overview
**Market data automation tool designed to eliminate manual "spreading comps" for Investment Banking workflows.** This engine fetches live financial data via the Yahoo Finance API, calculates key trading multiples (EV/EBITDA, P/E, Net Debt/EBITDA), and automatically generates client-ready Excel models with **peer-group benchmarking** and **conditional formatting**.

### 📸 Output Demo
*<img width="872" height="181" alt="Demo_Screenshot" src="https://github.com/user-attachments/assets/6998e195-6c02-4b74-94b9-1f3ca1450674" />*
> *Automated Excel output showing Big Tech peer group with algorithmic heatmaps (Green = Discount to Mean).*

### ⚡ Key Features
* **Zero Manual Entry:** Instantly scrapes Price, Market Cap, Enterprise Value, and Debt metrics.
* **Dynamic Logic:** Automatically calculates **Sector Mean & Median** to establish valuation benchmarks.
* **Banker-Ready formatting:** Exports to Excel with professional formatting ($0.00, 0.0x) and heatmaps (Red/Green) to identify relative value anomalies immediately.
* **Defensive Coding:** Handles missing data points (NaNs) and sector-specific nuances (e.g., EBITDA proxies) without crashing.

### 🛠 Tech Stack
* **Python:** Core logic & API handling.
* **Pandas:** Data manipulation & vectorization.
* **yfinance:** Real-time market data retrieval.
* **XlsxWriter:** Conditional formatting & Excel automation.

### 📉 Usage
```python
# Define your peer group
tech_peers = ['AAPL', 'MSFT', 'GOOGL', 'AMZN', 'NVDA']

# Run the engine
df = build_commercial_comps(tech_peers)
export_client_ready_excel(df, "Tech_Valuation_Output.xlsx")
