# TradingView Strategy

A TradingView strategy/indicator project built with Pine Script v6.

> This is a strategy that begins as a randomizer then improves from there.

## 📁 Project Structure

```
tradingview-strat-2/
├── src/                    # Pine Script source files
│   ├── strategy.pine       # Main trading strategy
│   └── indicator.pine      # Standalone indicator
├── docs/                   # Documentation
│   ├── USAGE.md           # How to use the strategy
│   └── DEVELOPMENT.md     # Development guidelines
├── examples/              # Example configurations
│   └── README.md          # Sample parameter sets
└── README.md              # This file
```

## 🚀 Getting Started

### Prerequisites

- A [TradingView](https://www.tradingview.com) account (free or paid)
- Basic understanding of trading concepts

### Quick Start

1. **Clone this repository**
   ```bash
   git clone https://github.com/culveyhouse/tradingview-strat-2.git
   ```

2. **Open TradingView** and navigate to any chart

3. **Open Pine Editor** (click "Pine Editor" at the bottom of the screen)

4. **Copy & Paste** the contents of `src/strategy.pine` into the editor

5. **Click "Add to Chart"** to compile and apply the strategy

## 📊 Features

- **Pine Script v6**: Built with the latest version for best performance
- **Configurable Parameters**: Easy-to-adjust inputs for customization
- **Risk Management**: Built-in stop loss and take profit
- **Long/Short Support**: Enable or disable either direction
- **Visual Signals**: Clear entry/exit indicators on chart

## ⚙️ Configuration

### Strategy Settings

| Parameter | Description | Default |
|-----------|-------------|---------|
| Enable Long Positions | Allow long entries | true |
| Enable Short Positions | Allow short entries | true |

### Indicator Settings

| Parameter | Description | Default |
|-----------|-------------|---------|
| Fast MA Length | Fast moving average period | 10 |
| Slow MA Length | Slow moving average period | 20 |

### Risk Management

| Parameter | Description | Default |
|-----------|-------------|---------|
| Stop Loss % | Stop loss from entry | 2.0% |
| Take Profit % | Take profit from entry | 4.0% |

## 📖 Documentation

- [Usage Guide](docs/USAGE.md) - Detailed instructions on using the strategy
- [Development Guide](docs/DEVELOPMENT.md) - Guidelines for contributing and development
- [Examples](examples/README.md) - Sample configurations for different trading styles

## 🧪 Backtesting

After adding the strategy to your chart:

1. Click on the **"Strategy Tester"** tab at the bottom
2. Review performance metrics:
   - Net Profit / Loss
   - Win Rate
   - Profit Factor
   - Maximum Drawdown
3. Adjust parameters and re-test

## ⚠️ Disclaimer

**This strategy is for educational purposes only.** Trading involves substantial risk of loss. Past performance is not indicative of future results. Always:

- Backtest thoroughly before live trading
- Paper trade first
- Only risk capital you can afford to lose
- Consider consulting a financial advisor

## 📝 License

This Pine Script™ code is subject to the terms of the Mozilla Public License 2.0 at https://mozilla.org/MPL/2.0/

## 🤝 Contributing

Contributions are welcome! Please read our [Development Guide](docs/DEVELOPMENT.md) before submitting changes.

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request
