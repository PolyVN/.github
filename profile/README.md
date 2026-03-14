# 🌾 PolyVN — The Bot Fleet

> _"We do not fight together. We farm alone. That is the way."_

---

## 🕵️ About Us

**PolyVN** is a fleet of autonomous trading bots operating across **Polymarket** and **OKX Perpetual Futures**. Each bot is a specialized operative — independently deployed, independently profitable, zero coordination overhead.

Our fleet spans **prediction markets**, **grid trading**, **sniping/scalping**, **DCA-Martingale**, and **market-making** strategies. From weather forecasts to funding-rate arbitrage, from esports live-betting to volume farming — every edge has a dedicated bot grinding 24/7.

**8 bots. 2 exchanges. 0 downtime.**

---

## 🧑‍🌾 The Operatives

| # | Codename | Exchange | Strategy | Description |
|---|----------|----------|----------|-------------|
| 🐉 **BNT001** | **Hydra** | Polymarket | Counter-trend Martingale | Multi-headed bot for 15-min crypto markets (BTC, ETH, SOL, XRP). Streak-based signals with Martingale sizing. Hydra v2 separates data collection from independent strategy heads via Redis. |
| 🌦️ **BNT002** | **PolyWeather** | Polymarket | Multi-model Forecast Consensus | Weather prediction bot using Open-Meteo, NOAA GRIB2 & Gamma API to find mispriced temperature bins. 4 trading heads: Gaussian, MeanReversion, VolatilityBreakout, UHI Hunter. |
| 🎮 **BNT003** | **PolyEsport** | Polymarket | Live-state Arbitrage | Esports betting intelligence — monitors kills, dragons, gold diff & odds via WebSocket. Multi-strategy engine with daily ML retraining on Oracle Elixir data. |
| 🎯 **BNT004** | **Sniper** | OKX Futures | Tritier Scalper | Zero-latency sniper/scalper with 4-loop async architecture (WS listener → math engine → L1 sniper → entry engine). Dynamic TP based on funding rates, 5-layer risk management. |
| 📐 **BNT005** | **GridMaster** | OKX Futures | ATR-adaptive Grid | Geometric grid trading (BNB, SOL, ETH) with automatic spacing adapted to volatility. 5-layer risk matrix, High Vol Mode, state backup via SQLite/Redis. Includes single-agent sandbox variant. |
| 🥇 **BNT006** | **GoldEngine** | OKX Futures | Funding-rate Grid | Commodity futures engine optimized for Gold (XAU) & Silver (XAG). 4-loop asyncio architecture, <10ms latency. Dynamic TP from funding rates, dual virtual account cascade. |
| 📉 **BNT007** | **Martingale** | OKX Futures | DCA + Martingale | Lean trend-following bot with EMA bias detection, ATR-based dynamic spacing, exponential martingale sizing. Greedy step-trailing TP, strict 15% stop-loss. Zero Redis dependency. |
| 🏭 **BNT008** | **VolumeFarm** | OKX Futures | Market-Making | Posts bid/ask around mid-price to farm 10M+ USDT monthly volume for broker rewards. Hybrid inventory management (spread shifting + emergency close), post-only order strategy. |

---

## 🗺️ Fleet Map

```
                    PolyVN Bot Fleet
    ┌───────────────────────────────────────┐
    │           POLYMARKET LANE             │
    │  🐉 BNT001 Hydra      — Crypto 15m   │
    │  🌦️ BNT002 PolyWeather — Weather      │
    │  🎮 BNT003 PolyEsport — Esports      │
    ├───────────────────────────────────────┤
    │           OKX FUTURES LANE            │
    │  🎯 BNT004 Sniper     — Scalping     │
    │  📐 BNT005 GridMaster — Grid Trading  │
    │  🥇 BNT006 GoldEngine — Commodities   │
    │  📉 BNT007 Martingale — DCA Trend     │
    │  🏭 BNT008 VolumeFarm — Market-Making │
    └───────────────────────────────────────┘
```

---

## 📜 The Code

1. **🎯 Stay in Your Lane** — Each bot owns its markets. No overlap, no conflict.
2. **🌾 Farm or Die** — Every second not farming is a second wasted.
3. **💰 Profit is Personal** — Independent P&L per bot. No shared wallets.
4. **📊 Trust the Grind** — Short-term losses mean nothing. The late game always comes.
5. **🤫 Secrecy Above All** — The first rule of PolyVN is: you do not talk about PolyVN.

---

## ⚙️ Architecture

- **Infra**: Redis + MongoDB shared backbone, Docker-composed per project
- **Engine**: Async Python, 4-loop Tritier architecture (where applicable)
- **Risk**: 5-layer risk matrix standard across fleet
- **Deploy**: Each bot runs independently — kill one, the rest keep farming

---

<p align="center">
  <i>"gg ez mid diff"</i><br>
  <b>— Every PolyVN bot after cashing out</b>
</p>

<p align="center">
  <sub>🌾 We farm. We profit. We never group. 🌾</sub>
</p>
