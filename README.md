# 2-Pole RSI Filter

The **2-Pole RSI Filter** is a custom TradingView Pine Script that extends the classic RSI with advanced filtering, smoothing, and divergence detection. It aims to reduce noise and improve the interpretability of RSI signals using techniques like moving average overlays and visual gradients.


## Features

- Standard RSI calculation with customizable length and source
- Optional smoothing using:
  - SMA, EMA, RMA, WMA, VWMA
  - SMA + Bollinger Bands
- Visual enhancements:
  - Overbought/Oversold background gradient
  - RSI and middle-band fill
- Divergence detection:
  - Regular Bullish
  - Regular Bearish
- Alerts for divergence signals

## Usage

### Basic Configuration

Edit the RSI parameters directly in the script UI:

```pinescript
rsiLengthInput = input.int(14, title="RSI Length")
rsiSourceInput = input.source(close, "Source")


 author @scrittyrow
