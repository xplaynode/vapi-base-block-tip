# Base Block Tip

A minimal paid API endpoint built on the [x402](https://x402.org) payment protocol.

`POST /paid` returns the current Base mainnet block number, timestamp, and block hash, fetched live at call time.

- **Price:** 0.005 USDC on Base (eip155:8453), paid per call via x402
- **Unpaid requests** get HTTP `402` with a `PAYMENT-REQUIRED` header carrying the payment offer
- **Payments** are verified and settled through the x402.org facilitator
- `GET /` returns a small service descriptor; `GET /openapi.json` returns an OpenAPI document with the x402 payment info

## Deploy

Deploy: Deno Deploy → New App → from this GitHub repo (entry point: `main.ts`).
