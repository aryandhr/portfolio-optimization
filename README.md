# Blockhouse Work Trial

10 additional features: [RL-PPO-v2(6)](RL-PPO-v2 (6).ipynb)

### 1. Arrival cost
Simple intuitive way to calculate slippage. Difference between price at the time of order placement and price at which order is filled.

### 2. Half-spread cost
Difference between best ask price and best bid price, divided by 2. Suggests transaction cost taking into account potential price movement after order is filled.

Detailed explanations for #1 and #2 in [transaction costs guide](transation-costs-guide.pdf)

### 3. Weighted mid-price
Used to construct micro-price which can beconsidered to be the ‘fair’ price of an asset. The micro-price may be expressed as an adjustment to the mid-price that takes into account the bid-ask spread and the imbalance.

### 4. Bid-ask bounce
Measure of where trade price falls within bid-ask spread. Values closer to 0 or 1 may indicate higher urgency.
Value = 0: The trade occurred exactly at the bid price.
Value = 1: The trade occurred exactly at the ask price.

### 5. Momentum
Captures recent price trends. Strong momentum may lead to larger slippage as the market moves quickly.

### 6. Price impact ratio
Relative price movement caused by last trade compared to spread. Higher ratio suggests last trade significantly impacted price.

### 7. Liquidity consumption rate
Measures liquidity depletion rate. Higher consumption rates indicate potential for higher slippage.

### 8. Time between trades
Time elapsed since last trade. Smaller time gaps suggest higher market activity, potentially leading to higher slippage due to faster execution prioritization over price.

### 9. TWAP
Average price over time period. Used in algorithms to trade while minimizing market impact.

### 10. VWAP
Average price weighted with volume. Helps understand true market value by accounting for volume of trades.
