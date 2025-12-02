# Example Configurations

This folder contains example configurations and parameter sets for different use cases.

## Scalping Configuration

For short-term trading on lower timeframes (5m - 15m):

```pinescript
i_fastLength = 5
i_slowLength = 10
i_stopLossPerc = 0.5
i_takeProfitPerc = 1.0
```

## Swing Trading Configuration

For medium-term trading on higher timeframes (4H - 1D):

```pinescript
i_fastLength = 20
i_slowLength = 50
i_stopLossPerc = 3.0
i_takeProfitPerc = 6.0
```

## Conservative Configuration

Lower risk approach with tighter stops:

```pinescript
i_enableShort = false    // Long only
i_fastLength = 10
i_slowLength = 20
i_stopLossPerc = 1.5
i_takeProfitPerc = 3.0
```

## Aggressive Configuration

Higher risk approach for volatile markets:

```pinescript
i_enableLong = true
i_enableShort = true
i_fastLength = 8
i_slowLength = 21
i_stopLossPerc = 4.0
i_takeProfitPerc = 8.0
```

---

**Note**: These are example configurations only. Always backtest and paper trade before using real capital.
