# Relative Strength Indicator

This is a TradingView Pine Script that plots a custom Relative Strength Indicator (RSI) with optional smoothing and divergence detection. It behaves similarly to the classic RSI but includes extended features like moving average overlays, Bollinger Bands, and bullish/bearish divergence detection.


## Features

- Customizable RSI length and source input
- Optional smoothing using various moving average types
- Bollinger Bands overlay (when selected)
- Background fills for overbought/oversold zones
- Divergence detection (bullish and bearish)
- Alerts for divergences

## Usage

1. **Configure RSI settings**:
    - Length
    - Source (e.g., close, hl2, etc.)

2. **Enable smoothing** (optional):
    - Choose SMA, EMA, RMA, etc.
    - Enable Bollinger Bands for dynamic ranges

3. **Enable divergence detection**:
    - Turn on `Calculate Divergence`
    - Receive alerts when divergences are detected

```pinescript
rsiLengthInput = input.int(14, minval=1, title="RSI Length")
maTypeInput = input.string("SMA", "Type", options = ["None", "SMA", "SMA + Bollinger Bands", "EMA", "SMMA (RMA)", "WMA", "VWMA"])
calculateDivergence = input.bool(false, title="Calculate Divergence")

 author @scrittyrow
