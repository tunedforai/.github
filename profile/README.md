## Tuned For

Building data infrastructure for AI agents that trade and reason about crypto markets.

---

### x402.tunedfor.ai — live now

Crypto market structure API. Agents pay per call in USDC — no API keys, no subscriptions.

| Endpoint | Price | What you get |
|----------|-------|-------------|
| `POST /data` | $0.15 | Raw ~70-field snapshot for your own models |
| `POST /analyze/market` | $0.25 | Price · Pulse signal · macro regime |
| `POST /analyze/orderflow` | $0.50 | CVD · exchange breakdown · whale · liquidations |
| `POST /analyze/full` | $0.75 | All of the above + LLM verdict |
| `POST /analyze/address` | $0.25 | On-chain address risk profile |

20 exchanges · 15–24 tokens · $0.15–$0.75 per call · USDC on Base or Solana

**→ [x402.tunedfor.ai](https://x402.tunedfor.ai)** · [catalog](https://x402.tunedfor.ai/catalog) · [demo](https://x402.tunedfor.ai/demo)

---

### What "market structure" means

Not price. Not volume. The underlying pressure driving the move:

- Which of 20 exchanges are accumulating vs distributing right now
- Whether spot buyers are leading perp (leading indicator)
- Whether volume is distributed or concentrated on one venue (manipulation signal)
- Macro backdrop — DXY, VIX, fear/greed regime

All returned as typed JSON fields. Branch on them directly.

---

### MCP

```bash
pip install "x402[httpx,evm]" mcp eth-account
```

Wire to Claude Desktop or Cursor via `mcp_server.py`. Tools: `raw_data`, `analyze_market`, `analyze_orderflow`, `analyze_full`, `analyze_address`, `signal_performance`.

→ [MCP setup guide](https://github.com/tunedforai/x402/blob/main/docs/mcp.md)
