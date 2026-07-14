# Arbitrum Builder

A multi-page Web3 educational website built for the **Arbitrum Builder Pods** assignment. It covers Layer 2 scaling, core blockchain concepts, live crypto prices, and an interactive block mining simulator — all in one cohesive, responsive site.

## Pages

| Page | File | Description |
|------|------|-------------|
| **Home / Landing** | `index.html` | Arbitrum & Layer 2 themed landing page with hero, features, L2 explainer, and call-to-action sections |
| **Concepts** | `concepts.html` | Visual comparison cards for Web2 vs Web3, Ethereum vs Bitcoin, Public Key vs Private Key, and Blockchain vs Traditional Databases |
| **Live Prices** | `prices.html` | Real-time crypto price dashboard fetching ETH, BTC, SOL, MATIC, and ARB from the CoinGecko API |
| **Block Simulator** | `simulator.html` | Interactive SHA-256 mining simulator demonstrating nonces, hashing, proof-of-work, and chain immutability |

## Tech Stack

- HTML5, CSS3, Vanilla JavaScript
- [CoinGecko Public API](https://www.coingecko.com/en/api) (no API key required)
- Web Crypto API (SHA-256) for block hashing
- Google Fonts (Inter)

## How to Run Locally

No build step or dependencies required.

### Option 1: Open directly in browser

Double-click `index.html` or open it in your browser. All pages work with `file://` protocol.

> **Note:** The Live Prices page requires internet access. CoinGecko API calls work from `file://` in most browsers, but if you hit CORS issues, use Option 2.

### Option 2: Local development server (recommended)

**Python 3:**
```bash
cd "Arbitrum Builder"
python -m http.server 8080
```
Then open [http://localhost:8080](http://localhost:8080)

**Node.js (npx):**
```bash
cd "Arbitrum Builder"
npx serve .
```

**VS Code / Cursor:**
Install the "Live Server" extension and click "Go Live" from the status bar.

## Project Structure

```
Arbitrum Builder/
├── index.html          # Home / Landing page
├── concepts.html       # Web3 concepts comparison cards
├── prices.html         # Live crypto price dashboard
├── simulator.html      # Block mining simulator
├── assets/
│   └── logo.svg        # Arbitrum Builder logo
├── css/
│   └── styles.css      # Shared styles (light theme)
├── js/
│   ├── nav.js          # Navigation & mobile menu
│   ├── prices.js       # CoinGecko API integration
│   └── simulator.js    # SHA-256 mining logic
└── README.md
```

## Screenshots

Add screenshots of each page here before submission:

1. `screenshots/home.png` — Home / Landing page
2. `screenshots/concepts.png` — Concepts page
3. `screenshots/prices.png` — Live Prices page
4. `screenshots/simulator.png` — Block Simulator page

## Customization

Before submitting, update the footer on all pages with your details:

- **Your Name** — replace with your actual name
- **GitHub link** — replace `https://github.com/Namra0001/arbitrum-builder` with your repo URL
- **Batch name** — update if different from "Arbitrum Builder Pods"

## Known Issues & Future Improvements

- **CoinGecko rate limits:** The free API allows ~10–30 requests/minute. Rapid clicking Refresh may temporarily fail — wait a few seconds and retry.
- **Mining speed:** Block mining runs in the browser main thread. On slower devices, mining may take a few seconds.
- **Future improvements:**
  - Add dark mode toggle
  - Coin search bar on the prices page
  - Price sparkline charts using CoinGecko historical data
  - Deploy to GitHub Pages or Vercel for a live demo URL

## License

Built for educational purposes as part of the Arbitrum Builder Pods program.
