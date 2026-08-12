<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/MCP-Protocol-8b5cf6?style=for-the-badge" />
  <img src="https://img.shields.io/badge/NSE/BSE-Live_Data-22c55e?style=for-the-badge" />
  <img src="https://img.shields.io/badge/AI_Agents-6_Debaters-f59e0b?style=for-the-badge" />
  <img src="https://img.shields.io/badge/License-MIT-blue?style=for-the-badge" />
</p>

<h1 align="center">📈 MarketPulse MCP</h1>
<h3 align="center">95 Free Financial Intelligence Tools for AI Agents</h3>
<p align="center"><em>Indian + Global Markets • MCP-Native • Works with Claude, Cursor & any MCP client</em></p>

---

## 🎯 What is MarketPulse MCP?

**MarketPulse MCP** is an open-source Model Context Protocol (MCP) server that gives AI assistants like Claude real-time access to **95 financial data tools** — covering Indian equities (NSE/BSE), global markets, options analytics, AI-driven stock debates, portfolio analysis, and more.

Ask one question like `"Should I buy Reliance?"` and get a 6-agent debate, sentiment analysis, smart-money detection, risk assessment, peer context, and a consensus BUY/HOLD/SELL — all in one response.

```bash
pip install finstack-mcp
```

### What You Can Ask

```text
"Give me a full stock brief on Reliance"
→ 6 AI agents debate: FII Desk + Algo Trader + Value Investor + Retail Pulse + Macro Analyst + Options Flow
→ Consensus: BUY/HOLD/SELL with reasoning

"Is someone accumulating HDFC Bank quietly?"
→ Checks OI buildup + block deals + promoter buying + volume spike simultaneously

"What's the social buzz on TCS before results?"
→ StockTwits + Reddit + Economic Times → 67% bullish | Signal: HOLD

"Will Nifty go up tomorrow?"
→ RSI + FII flow + PCR + VIX + G-Sec + GIFT Nifty → 63% probability up

"Give me the 8:15 AM F&O brief"
→ GIFT Nifty + VIX + NIFTY setup + BANKNIFTY setup → ready-to-forward morning note
```

---

## 🏗️ Architecture Overview

```
┌─────────────────────────────────────────────────────────────────────┐
│                      MarketPulse MCP Architecture                   │
├──────────┬──────────────┬──────────────┬────────────┬──────────────┤
│  Data    │    Tools     │   AI Intel   │  Portfolio │   MCP Layer  │
│ Sources  │   (95+)      │   Engine     │  Analytics │              │
│          │              │              │            │              │
│ NSE/BSE  → Indian Mkt  → Stock Brief  → XIRR/P&L  → Claude       │
│ yfinance → Global Mkt  → Stock Debate → Risk Flags → Cursor       │
│ Brokers  → Options     → Sentiment    → Sec. Conc. → Windsurf     │
│ CoinGecko→ Crypto/FX   → Smart Money  → Overlap   → Any MCP CLI  │
└──────────┴──────────────┴──────────────┴────────────┴──────────────┘
```

---

## 💰 What This Replaces

| Tool | What You Pay | MarketPulse MCP |
|---|---|---|
| Bloomberg Terminal | $31,980/yr | **FREE** |
| Bloomberg ESG + Credit | $24,000/yr | **FREE** |
| Sensibull (Options Greeks) | ₹15,600/yr | **FREE** |
| Morningstar (MF flows) | $17,500/yr | **FREE** |
| Screener.in Pro | ₹4,999/yr | **FREE** |
| Trendlyne Pro | ₹4,950/yr | **FREE** |

---

## 🚀 Quick Start (2 minutes)

### Install

```bash
pip install finstack-mcp
```

### Connect to Claude Desktop

Add to `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "marketpulse": {
      "command": "python",
      "args": ["-m", "finstack.server"]
    }
  }
}
```

Restart Claude Desktop. Done.

### Connect to Cursor / Windsurf / Cline

```json
{
  "mcpServers": {
    "marketpulse": {
      "command": "python",
      "args": ["-m", "finstack.server"]
    }
  }
}
```

---

## 🔧 95 Tools Across 10 Categories

### 🇮🇳 Indian Markets (Live Data)
- NSE/BSE real-time quotes, OHLCV history, market status
- Nifty 50, Bank Nifty, Sensex indices
- FII/DII institutional flows (daily + historical)
- Bulk & block deals, circuit breaker scanner, 52W high/low
- Mutual fund NAV, corporate actions, earnings calendar, IPO calendar

### 🧠 AI Intelligence (Unique)
- **`get_stock_brief`** — 6 AI agents debate → BUY/HOLD/SELL consensus
- **`get_stock_debate`** — 3-round sequential debate with rebuttals
- **`get_social_sentiment`** — StockTwits + Reddit + ET RSS → sentiment signal
- **`detect_unusual_activity`** — OI buildup + block deals + volume spike
- **`get_nifty_outlook`** — 6-signal probability model for next session
- **`get_fno_trade_setup`** — NIFTY/BANKNIFTY options call with ATM strike
- **`predict_earnings`** — Beat/miss probability before quarterly results

### 📊 Research & Ranking
- **`scan_watchlist`** — Batch-rank watchlist, surface top buys and risks
- **`get_stock_signal_score`** — Automation-friendly score with factor impacts
- **`get_stock_timeline`** — News, results, insider, sentiment in one feed
- **`get_sector_peer_context`** — Sector strength + peer rank

### 💼 Portfolio & Risk
- **`analyze_portfolio`** — P&L, XIRR, sector concentration, diversification
- **`get_mf_overlap`** — Fund overlap % from AMFI disclosures
- **`get_pledge_alert`** — Promoter pledge early warning
- **`detect_pump`** — Pump-and-dump pattern detector for small caps

### 🔗 Broker Integrations (Zero-Delay)
- Angel One SmartAPI — live quotes, Level 2 depth, intraday candles
- Fyers API v3 — live quotes + candles
- ICICI Breeze / Dhan / Upstox — all supported

### 📐 Options & Greeks
- Full NSE options chain with PCR, Open Interest, Max Pain
- Black-Scholes Greeks: Delta, Gamma, Theta, Vega, Rho

### 🌍 Global + Crypto + Tax
- US, EU, global equities — quotes + history
- Crypto: BTC, ETH, SOL, 100+ coins (CoinGecko)
- Forex: USD/INR, EUR/INR, 50+ pairs
- **LTCG/STCG tax calculator** (post-July 2024 Budget rules)

### 🇮🇳 India-Specific (Never-Built-Before)
- **`correlate_gst_to_stocks`** — GST data as sector leading indicator
- **`get_telegram_tracker`** — Tip channel accuracy + pump scoring
- **`analyze_budget_live`** — Paste FM speech → instant sector signals
- **`get_insider_signal`** — SEBI SAST pattern vs forward returns

---

## 🔬 Data Sources

| Source | Covers | Key Needed |
|---|---|---|
| yfinance | NSE/BSE/US equities, crypto, forex | None |
| NSE direct API | FII/DII, options chain, insider trading | None |
| BSE India API | Credit ratings, ESG/BRSR | None |
| SEC EDGAR | US filings (10-K, 10-Q, 8-K) | None |
| CoinGecko | Crypto market data | None |
| AMFI / mfapi.in | Mutual fund NAV, AUM | None |
| StockTwits | Trader sentiment | None |
| Angel One SmartAPI | Real-time NSE, Level 2 depth | Free account |

---

## 🛠️ Development

```bash
git clone https://github.com/tanmaymish/MarketPulse-MCP.git
cd MarketPulse-MCP
pip install -e .[dev]
pytest -q
```

PRs welcome. Adding a new broker: create `src/finstack/data/broker_X.py` and register in `tools/`.

---

## 📈 Comparison vs Market Tools

| Feature | MarketPulse MCP | Screener.in | Tickertape | Sensibull | Trendlyne |
|---|---|---|---|---|---|
| AI agents debate a stock | ✅ | ❌ | ❌ | ❌ | ❌ |
| Social sentiment | ✅ | ❌ | ❌ | ❌ | ❌ |
| Nifty direction probability | ✅ | ❌ | ❌ | ❌ | ❌ |
| Telegram tip tracker | ✅ | ❌ | ❌ | ❌ | ❌ |
| Options Greeks | ✅ free | ❌ | ❌ | ✅ ₹1,300/mo | ❌ |
| Works inside Claude/Cursor | ✅ | ❌ | ❌ | ❌ | ❌ |
| **Price** | **Free** | ₹4,999/yr | ₹2,800/yr | ₹15,600/yr | ₹4,950/yr |

---

## 📜 License

MIT License — Free to use, modify, and distribute.

---

## 📬 Contact

**Tanmay Mishra**
📧 [tanmaymish78@gmail.com](mailto:tanmaymish78@gmail.com)
🔗 [LinkedIn](https://www.linkedin.com/in/tanmay-mishra-0308a8207)
🐙 [GitHub](https://github.com/tanmaymish)

---

<p align="center">⭐ Star this repo if you found it useful!</p>
