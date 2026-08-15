<div align="center">

<img src="https://moyuquant.cc/static/moyuquant_logo.png" width="120" height="120" alt="MoyuQuant Logo">

# MoyuQuant

### Crypto Perpetual Futures Quant Trading System

[![License](https://img.shields.io/badge/license-Proprietary-blue)]()
[![Exchange](https://img.shields.io/badge/Exchange-OKX%20%2B%20Binance-orange)]()
[![Network](https://img.shields.io/badge/Network-TRC--20-green)]()
[![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey)]()

[Website](https://moyuquant.cc) · [Twitter](https://x.com/MoyuQuant) · [Discord](https://discord.gg/ZtsY4cJWXE)

</div>

---

## Overview

MoyuQuant is a deterministic algorithmic trading system for crypto perpetual futures on **OKX** and **Binance**. Built on condition-based strategies — no machine learning, no black boxes. Every strategy is verified against 8.7 years of market data, and the live engine matches the backtest at 100% parity across 79 trades.

**Currently shipping two built-in strategies, ready to run out of the box.**

---

## Strategies

### XIN001 — Multi-Period Trend Strategy

Condition-engine based long-only strategy using multi-timeframe resonance with MA7/MA21/ATR/volume/MA-angle filters.

| Metric | Value |
|--------|-------|
| Backtest Period | 8.7 years |
| Annual CAGR | +14.39% |
| Strategy Type | Condition-based, no parameters to tune |

### xin-dca-101 — DCA with Trailing Take-Profit

Hedging martingale strategy with automated trailing TP. Locks in gains while letting winners run.

| Metric | Value |
|--------|-------|
| Win Rate | 95.7% |
| Backtest Period | 8.7 years |
| Annual CAGR | +11.39% |

---

## Key Features

- **100% Backtest Parity** — The live engine and backtest share the exact same codebase. 79 trades replayed through the live engine matched 79/79.
- **Crash Recovery** — Full state serialization on every tick. Power outage, network failure, server restart — zero data loss.
- **Multi-Exchange** — OKX and Binance supported with equal priority. WebSocket real-time data with REST fallback.
- **Non-Custodial** — Your funds never leave the exchange. API keys with trade permission only, never withdrawal.
- **Online License Verification** — Hardware-independent licensing with 72-hour offline grace period.

---

## Quick Start

### 1. Download

Download the latest release from the [Releases page](../../releases).

### 2. Extract and Run

```
Unzip the downloaded file
Run MoYuQuantFree.exe
```

No installation required. No Python or dependencies needed.

### 3. Configure

1. Create API keys on OKX or Binance (enable Futures trading, **disable withdrawal**)
2. Launch the app and enter your API keys
3. Select a strategy and set your capital
4. Click Start

---

## Free Version vs Commercial Version

| Feature | Free Version | Commercial Version |
|---------|:---:|:---:|
| XIN001 Trend Strategy | ✅ | ✅ |
| DCA with Trailing TP | ✅ | ✅ |
| OKX + Binance | ✅ | ✅ |
| Crash Recovery | ✅ | ✅ |
| Unlimited Pairs | ✅ | ✅ |
| License Verification | ❌ | ✅ |
| Priority Support | ❌ | ✅ |
| Early Access Features | ❌ | ✅ |

The free version has no time limit and no feature restrictions on trading. The commercial version adds online license verification, priority support, and early access to new features.

---

## Pricing

| Plan | Price | Duration |
|------|-------|----------|
| Monthly | $29 | 30 days |
| Quarterly | $79 | 90 days |
| Yearly | $99 | 365 days |
| Referral | Free | 30 days + extendable |

Pay with USDT (TRC-20). Deposit once, subscribe multiple times without extra transfer fees.

**Earn a free license through referrals:** Register on OKX or Binance using our referral link, submit your UID, and get a 30-day license. Keep trading to extend it by one day per active day.

- OKX Referral: [https://www.okx.com/join/2177090](https://www.okx.com/join/2177090)
- Binance Referral: [https://www.binance.com/en/register?ref=BBBFWA4A](https://www.binance.com/en/register?ref=BBBFWA4A)

---

## Tech Stack

- Python 3.10 + PySide6 (GUI)
- ccxt (Exchange API)
- NumPy (Indicator computation)
- SQLite (State persistence)
- PyInstaller (Packaging, zero source code in release)

---

## Architecture

```
┌─────────────────────────────────────────────┐
│              Strategy Layer                   │
│  (Built-in condition-based strategies)        │
├─────────────────────────────────────────────┤
│           Condition Engine                    │
│  (Evaluates entry/exit conditions per tick)   │
├─────────────────────────────────────────────┤
│            Indicator Layer                    │
│  (MA7/MA21/ATR/Volume/RSI/MACD/BOLL/KDJ)     │
├─────────────────────────────────────────────┤
│          Order Monitor + Execution            │
│  (WebSocket real-time + REST fallback)        │
├─────────────────────────────────────────────┤
│         Persistence + Crash Recovery          │
│  (session.json snapshot every tick)           │
└─────────────────────────────────────────────┘
```

---

## Community

- **Website:** [moyuquant.cc](https://moyuquant.cc)
- **Twitter/X:** [@MoyuQuant](https://x.com/MoyuQuant)
- **Discord:** [Join our community](https://discord.gg/ZtsY4cJWXE)
- **Contact:** contact@moyuquant.cc

---

## Risk Disclaimer

Trading cryptocurrencies involves significant risk of loss. Past performance does not guarantee future results. This software is provided for informational and educational purposes only and is not financial advice. You are solely responsible for your trading decisions.

<div align="center">

© 2026 MoyuQuant. All rights reserved.

</div>
