# Drift Protocol (Drift V2)  
> On‑chain, cross‑margined perpetual futures & spot trading on Solana  

## Table of Contents  
- [Introduction](#introduction)  
- [Key Features](#key‑features)  
- [Architecture & How it Works](#architecture‑how‑it‑works)  
- [Getting Started](#getting‑started)  
  - [Wallet Setup](#wallet‑setup)  
  - [Deposit / Collateral](#deposit‑collateral)  
  - [Trading / Opening Positions](#trading‑opening‑positions)  
- [Supported Products](#supported‑products)  
- [Security & Risk Management](#security‑risk‑management)  
- [Developer & SDK/API Access](#developer‑sdkapi‑access)  
- [Contributing](#contributing)  
- [License](#license)  

## Introduction  
Drift Protocol is a decentralized exchange built on Solana, designed to bring derivatives (perpetual futures) and spot margin trading into a non‑custodial, transparent environment. :contentReference[oaicite:2]{index=2}  

Users retain control of their assets through their wallet, while accessing features like cross‐collateral, borrow/lend, yield‑earning, and leveraged trading. :contentReference[oaicite:3]{index=3}  

## Key Features  
- **High speed & low latency execution**: leveraging Solana’s ~100 ms finality for fast transactions. :contentReference[oaicite:4]{index=4}  
- **Cross‐margin & yield‐bearing collateral**: deposit a variety of supported tokens, use them as collateral for trading, and also earn yield via lending. :contentReference[oaicite:5]{index=5}  
- **Deep liquidity model** via hybrid architecture:
  - Just‑in‑Time (JIT) auction liquidity  
  - Decentralised Limit Order Book (DLOB)  
  - Automated Market Maker (AMM) as backstop :contentReference[oaicite:6]{index=6}  
- **Perpetual futures markets**: Trade major assets with leverage (e.g., SOL‑PERP, BTC‑PERP). :contentReference[oaicite:7]{index=7}  
- **Transparent, on‑chain operations**: every trade, deposit, borrow is executed via smart contracts. :contentReference[oaicite:8]{index=8}  

## Architecture & How it Works  
### Liquidity Model  
The protocol uses a three‑tier liquidity model to ensure efficient fills and minimal slippage:  
1. **Just‑in‑Time (JIT) Auctions** – Market orders spark a brief auction (~5 seconds) where liquidity providers compete. :contentReference[oaicite:9]{index=9}  
2. **Decentralised Limit Order Book (DLOB)** – Users place limit orders on‑chain, keepers monitor triggers and fill orders when conditions are met. :contentReference[oaicite:10]{index=10}  
3. **AMM Backstop** – If no other liquidity fills, the AMM provides the price to guarantee execution. :contentReference[oaicite:11]{index=11}  

### Risk Engine & Collateral  
- All deposited collateral can be used for trading and/or lending. :contentReference[oaicite:12]{index=12}  
- Cross‑margin means one collateral pool supports multiple positions, increasing capital efficiency.  
- The protocol features health checks, insurance fund, and liquidation mechanisms to protect the system. :contentReference[oaicite:13]{index=13}  

### Products  
- **Perpetual Futures / Swaps** – No expiry, up to high leverage on major assets. :contentReference[oaicite:14]{index=14}  
- **Spot Trading with Leverage** – Trade spot pairs with leverage up to ~5×. :contentReference[oaicite:15]{index=15}  
- **Lend / Borrow** – Supply collateral, borrow other assets, earn yield. :contentReference[oaicite:16]{index=16}  

## Getting Started  
### Wallet Setup  
1. Choose a Solana wallet (e.g., Phantom, Solflare, etc.). :contentReference[oaicite:19]{index=19}  
2. Connect your wallet at [app.drift.trade](https://app.drift.trade).  
3. Ensure you have some SOL for transaction fees and a supported token for collateral.

### Deposit / Collateral  
- Navigate to the “Deposit” or “Collateral” section in the UI.  
- Deposit supported tokens to your account. The deposited assets will appear as available collateral.  
- You may optionally lend them to earn yield if you are not immediately trading.

### Trading / Opening Positions  
- Select a market (e.g., SOL‑PERP, BTC‑PERP).  
- Choose your direction (Long or Short) and the leverage.  
- Monitor margin, P&L, health of your account. The “Overview”, “Positions”, “History” pages provide details. :contentReference[oaicite:20]{index=20}  
- Use the “Close” button to close a position when ready.  
- Keep track of your account health to avoid liquidation risk.

## Supported Products  
- Perpetual futures (multiple markets). :contentReference[oaicite:21]{index=21}  
- Spot trading with leverage (up to ~5×) on selected pairs. :contentReference[oaicite:22]{index=22}  
- Lending & borrowing markets for many assets. :contentReference[oaicite:23]{index=23}  
- Yield‑earning vaults, insurance fund staking, market maker programs. :contentReference[oaicite:24]{index=24}  

## Security & Risk Management  
- The protocol has been audited by top firms (e.g., Trail of Bits, Neodyme). :contentReference[oaicite:27]{index=27}  
- The insurance fund and risk engine are designed to handle extreme market events. :contentReference[oaicite:28]{index=28}  
- Users remain in control of their wallets; non‑custodial means you retain asset control (however you must still manage risk!).  
- **Important**: Leverage increases reward *and* risk — you can incur large losses. Always evaluate margin and liquidation risk.  

## Developer & SDK / API Access  
- The protocol is open‑source and welcomes contributions. :contentReference[oaicite:29]{index=29}  
- SDKs available (Typescript, Python) for interacting with the protocol programmatically. :contentReference[oaicite:30]{index=30}  
- Documentation available at [docs.drift.trade](https://docs.drift.trade) for deep dives into matching engine, AMM, keeper bots, API endpoints. :contentReference[oaicite:31]{index=31}  

## Contributing  
If you’d like to contribute:  
- Fork the repository and submit a PR.  
- Ensure you follow the coding style and include tests.  
- Check the open issues or feature requests to align your contribution.  
- Respect the existing code of conduct and licensing of the project.

## License  
Specify the license used by the project (e.g., MIT, Apache‑2.0).  
*Note: this README template assumes the license is declared in the repository.*

---

**Happy trading and building!**  
This README should give users and developers a clear overview of Drift Protocol and how to interact with it. If you’d like a customized version (e.g., for your fork, specific features you’re working on, or dev environment setup), just let me know and I can help tailor it further.
::contentReference[oaicite:32]{index=32}
