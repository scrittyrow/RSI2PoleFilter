📘 RSI-2Pole-Filtered: Smoothed Momentum Indicator with Tunable Feedback
Overview
This project implements a custom momentum indicator by applying a second-order IIR (2-pole) digital filter to the classic Relative Strength Index (RSI). It’s designed for traders and analysts who want a smoother, more reliable momentum signal that reduces noise and false triggers common in raw RSI.

While RSI smoothing is common (via EMA or RMA), this implementation offers full control over filter behavior, including:

Smoothing intensity

Lag compensation

Feedback vs feedforward response

📌 This filtering method is not found in conventional trading tools, and to the author's knowledge, this is the first application of a 2-pole recursive filter to RSI in Pine Script.

💡 Why This Matters
RSI is a widely used momentum oscillator, but it often suffers from:

Excessive sensitivity in sideways markets (whipsaws)

Poor signal quality in low-volume conditions

Lack of tunability beyond the length parameter

This project solves that by introducing true recursive filtering from digital signal processing — enabling smoother RSI curves without sacrificing responsiveness.

🔍 Technical Summary
The filtered RSI is computed using the following difference equation:

y[n] = b0 * x[n] + b1 * x[n−1] + b2 * x[n−2] − a1 * y[n−1] − a2 * y[n−2]
Where:

x[n] is the raw RSI input

y[n] is the smoothed output

b0, b1, b2 are feedforward coefficients

a1, a2 are feedback coefficients

The filter is fully tunable, allowing users to trade off:

Smoothing vs lag

Reactivity vs noise suppression

📈 Use Cases
Momentum confirmation

RSI signal filtering for trend trading

Reducing whipsaws in mean-reverting strategies

Visual trend smoothing for discretionary traders

Feeding cleaner signals into automated systems

🧪 Example Configuration
pinescript
Copy
Edit
b0 = 0.4
b1 = 0.2
b2 = 0.1
a1 = -0.3
a2 = 0.05
This produces a moderately smoothed RSI with low overshoot and fast recovery. You can adjust these to fit your asset and timeframe.

🚀 Getting Started
Copy the Pine Script from the rsi_2pole_filter.pine file.

Paste into TradingView → Pine Editor.

Add to chart and tune coefficients to match your asset.

Optionally add alerts or strategy logic.

✅ Features
Drop-in replacement for RSI in any strategy

Fully tunable second-order IIR filter

Compatible with TradingView

Built-in overbought/oversold thresholds

Clear code structure for future expansion


👤 Author
Created by Scrittyrow
