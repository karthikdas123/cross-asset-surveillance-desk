# Cross-Asset Market Surveillance & Electronic Risk Desk

A real-time institutional cross-asset market surveillance dashboard monitoring 17 global instruments across US Equities, Indian NSE, Forex, and Commodities. Built with Python (FastAPI, WebSockets), HTML5, Chart.js, and browser-native voice synthesis.

## Features
- **Statistical Baselines**: Calibrated Time-of-Day expected volume ($\mu$), standard deviation ($\sigma$), 14-day ATR, and 30-day ADV.
- **Microstructure Anomaly Detection**:
  - Volume Bursts ($Z$-score $\ge 4.0\sigma$)
  - Flash Price Dislocations ($> 2.5\times ATR_{14}$)
  - Spoofing & Layering Signatures (Cancel-to-Replace $> 90\%$ + short resting lifetimes)
- **Automated Electronic Risk Controls**:
  - ⛔ Session Kill-Switches
  - 📉 Dynamic Clip Caps (clamping allowable order lots)
  - ⏳ Rate-Limit Throttles (5 msgs/sec cooldown)
- **Interactive UI**: Sub-second telemetry charts, row focus inspection, audio speech alarms, and real-time anomaly injection buttons.

## Quickstart

```bash
# 1. Install dependencies
pip install -r requirements.txt

# 2. Run the Surveillance Desk
python surveillance_desk.py
