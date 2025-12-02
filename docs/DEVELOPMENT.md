# Development Guide

## Pine Script v6 Overview

This project uses Pine Script v6, the latest version of TradingView's programming language.

### Key Features in v6

- Improved type system
- Better error messages
- Enhanced libraries support
- More consistent syntax

### Documentation

- [Pine Script v6 User Manual](https://www.tradingview.com/pine-script-docs/)
- [Pine Script v6 Reference Manual](https://www.tradingview.com/pine-script-reference/)

## Project Structure

```
├── src/
│   ├── strategy.pine    # Main strategy file
│   └── indicator.pine   # Standalone indicator (optional)
├── docs/
│   ├── USAGE.md         # User guide
│   └── DEVELOPMENT.md   # Developer guide
├── examples/
│   └── README.md        # Example configurations
└── README.md            # Project overview
```

## Code Style Guidelines

### Naming Conventions

- **Inputs**: Prefix with `i_` (e.g., `i_length`)
- **Variables**: Use camelCase (e.g., `fastMA`)
- **Constants**: Use UPPER_SNAKE_CASE (e.g., `MAX_BARS`)

### Code Organization

1. License header
2. Version directive
3. Strategy/Indicator declaration
4. Input definitions (grouped by category)
5. Indicator calculations
6. Signal logic
7. Strategy execution
8. Plotting

### Comments

- Use `// ═══...═══` for section separators
- Keep comments concise and meaningful
- Document complex calculations

## Testing Your Changes

1. Copy your code to TradingView's Pine Editor
2. Click "Add to Chart" to compile
3. Review for any compilation errors
4. Test on different timeframes and symbols
5. Use Strategy Tester for backtesting

## Version Control Best Practices

- Commit frequently with descriptive messages
- Use branches for new features
- Tag releases with version numbers
