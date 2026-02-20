# Data-Science-Analytics-Intern-Round-0-Assignment-
# Trader Performance vs Market Sentiment (Hyperliquid × Fear & Greed Index)

This project analyzes how market sentiment (Fear/Greed Index) relates to trader behavior and performance on Hyperliquid.  
The goal is to uncover patterns that can inform sentiment-aware trading strategies and platform risk controls.

## 📊 What’s Inside
- Jupyter Notebook with full analysis (`notebook.ipynb`)
- Raw datasets (`data/`)
- Output charts (`outputs/`)
- Summary of methodology, insights, and strategy recommendations

## ⚙️ Setup
```bash
pip install pandas numpy matplotlib


---

## 📄 1-Page Write-up (Add as Markdown Section in Notebook or README)

```markdown
## Short Write-up: Methodology, Insights & Strategy Recommendations

### Methodology
- Aligned Hyperliquid trade data with daily Fear & Greed Index values.
- Engineered daily trader metrics: PnL, trades/day, leverage, trade size, win-rate proxy, and drawdown proxy.
- Analyzed performance and behavior across sentiment regimes.
- Segmented traders into: high vs low leverage, frequent vs infrequent, and consistent vs inconsistent winners.

### Key Insights
1. **Performance is regime-dependent:**  
   Fear regimes show the highest average and median daily PnL compared to Greed and Neutral regimes.

2. **Behavior shifts with sentiment:**  
   Trading activity peaks during Fear regimes, while leverage usage spikes during Greed/Extreme Greed regimes.  
   Higher leverage during Greed does not translate to better performance.

3. **Trader heterogeneity matters:**  
   High-leverage and consistent traders outperform on average, but only with higher activity and historical win rates.

### Strategy Recommendations
- **Fear Regimes:** Allow higher trade frequency but cap leverage (e.g., reduce max leverage by ~30–40%).  
- **Greed/Extreme Greed Regimes:** Enforce stricter leverage limits for low win-rate traders; allow higher leverage only for consistent traders.

### Limitations
- Analysis uses aggregated daily PnL and does not account for transaction costs or slippage.
- Some directional labels were sparse; long/short bias should be interpreted cautiously.
