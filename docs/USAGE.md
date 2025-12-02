# Usage Guide

## Adding the Strategy to TradingView

1. **Open TradingView**: Go to [TradingView.com](https://www.tradingview.com) and log in to your account.

2. **Open Pine Script Editor**: 
   - Open any chart
   - Click on "Pine Editor" at the bottom of the screen

3. **Create New Script**:
   - Click "Open" → "New blank script"
   - Delete any existing code

4. **Copy & Paste**:
   - Copy the contents of `src/strategy.pine` (for strategy) or `src/indicator.pine` (for indicator)
   - Paste into the Pine Editor

5. **Add to Chart**:
   - Click "Add to Chart" button
   - The strategy/indicator will appear on your chart

## Configuring the Strategy

### Strategy Settings

| Parameter | Description | Default |
|-----------|-------------|---------|
| Enable Long Positions | Allow long entries | true |
| Enable Short Positions | Allow short entries | true |

### Indicator Settings

| Parameter | Description | Default |
|-----------|-------------|---------|
| Fast MA Length | Period for fast moving average | 10 |
| Slow MA Length | Period for slow moving average | 20 |

### Risk Management

| Parameter | Description | Default |
|-----------|-------------|---------|
| Stop Loss % | Stop loss percentage from entry | 2.0% |
| Take Profit % | Take profit percentage from entry | 4.0% |

## Backtesting

1. After adding the strategy to your chart, click on "Strategy Tester" tab
2. Review the performance metrics:
   - Net Profit
   - Percent Profitable
   - Profit Factor
   - Max Drawdown
3. Adjust parameters and re-test to optimize

## Best Practices

1. **Always backtest** before using real money
2. **Use appropriate timeframes** - this strategy works best on higher timeframes (1H+)
3. **Paper trade first** - use TradingView's paper trading feature
4. **Adjust position sizing** - modify `default_qty_value` based on your risk tolerance
