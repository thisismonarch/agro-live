# Agrofix

Agrofix is a commodity market intelligence terminal for African agricultural markets, with synthetic markets and an on-chain settlement design on Solana.

**Live demo:** https://agro-terminal.vercel.app
**Backend (market data API, in progress):** https://github.com/thisismonarch/agro-live-backend

> This is a prototype. Prices, positions, and wallet connections are demo data. Nothing is settled on-chain yet. See the status table below.

## What's in this repo

`index.html` is the whole frontend: a single static file with HTML, CSS and JavaScript. It has no build step.

Tabs:
- **Overview:** commodity intelligence cards, price charts, regional price comparison, daily market brief
- **Routes, Compliance, Weather:** trade routes, tariff and certification status, weather impact
- **Trading:** quick trade and advanced order forms (UI only)
- **Synthetic Markets:** long/short exposure to agro commodity prices, with position limits enforced in the demo
- **Portfolio, Watchlist, Collateral Valuation, Margin Calculator:** portfolio tracking, alerts, collateral and margin tools
- **Terminal:** AI market Q&A interface

## Status

| Feature | Status |
|---|---|
| Commodity dashboard (8 commodities) | Demo data |
| Price charts, volatility, RSI/SMA | Demo data |
| Regional price comparison | Demo data |
| Oracle price display | Demo (simulated, not connected to a price feed) |
| Synthetic Markets: long/short, position limits, margin checks | Demo (positions stored in browser) |
| Synthetic Markets: USDC settlement on Solana | Coming soon |
| Wallet connection | Demo (not connected to a real wallet) |
| Trading and portfolio | UI only (orders recorded in browser, not sent on-chain) |
| Bank transfer settlement | Coming soon |
| Live commodity prices | Coming soon (backend in progress) |
| Physical deal feedback into the oracle | Coming soon |

## Run it locally

No install needed. Open `index.html` in a browser, or serve the folder:

```
python3 -m http.server 8000
```

Then visit http://localhost:8000.

## Roadmap

1. Connect the frontend to the backend `/api/market` endpoint for live commodity, FX and weather data
2. Replace the simulated oracle with a multi-source African price feed (Oracle v1: maize and sorghum)
3. Real wallet connection and USDC settlement on Solana
4. Enforce position limits on-chain

## Notes for contributors

- The backend repo also contains a copy of the terminal in `public/index.html`. Keep one copy as the source of truth to avoid drift.
- Demo values live in the `products` object in `index.html`. Replace these with API data when the backend is connected.

## Contact

Built by MONARCH. Contact details:theagrofix@gmail.com
