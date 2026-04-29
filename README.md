Markdown
# Financial-Sentiment-Analysis
This project uses **PyTorch** and **FinBERT** to automate the sentiment analysis of financial news. It is designed to validate signals for algorithmic trading.

---

## 🔍 Quality Architect Analysis: Signal Validation
In my experience with AI Data Governance (Cogito/Flipkart), I've learned that raw model output can be misleading. Below is a "Failure Case" I identified where the AI's sentiment doesn't match the market reality.

### **Edge Case Audit**
* **Headline:** "Tesla is forced to slash prices of its Model 3 to clear inventory."
* **Model Prediction:** `Negative` (Confidence: 94%)
* **Business Reality:** `Positive / Bullish` (Aggressive inventory turnover and market share capture).

### **Reverse Engineering the Error**
The model is over-weighting keywords like "forced" and "slash." It lacks the contextual "Business Logic" to see price-cutting as a competitive strategy.

### **The "High-Alpha" Solution**
As a Portfolio Strategist, I would implement a **Validation Layer** that flags "Price Change" events for manual review or cross-references them with sales volume data. This prevents the portfolio from selling a stock based on a "False Negative" sentiment.
