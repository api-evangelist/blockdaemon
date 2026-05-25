# Blockdaemon

API Evangelist catalog entry for **Blockdaemon** — institutional blockchain infrastructure, staking, indexed data, DeFi, custody, and tokenization across 80+ protocols.

- Website: <https://www.blockdaemon.com>
- Docs: <https://docs.blockdaemon.com>
- Status: <https://status.blockdaemon.com>
- LLMs.txt index: <https://docs.blockdaemon.com/llms.txt>
- MCP server: <https://docs.blockdaemon.com/mcp>
- GitHub: <https://github.com/Blockdaemon>

Founded in 2017 by Konstantin Richter. Trusted by 400+ institutional customers including Goldman Sachs, Microsoft, JP Morgan, and Citi Ventures. SOC 2 Type II (June 2025) and ISO 27001 (July 2022) certified. $110B+ digital assets secured; $10B+ staked on Blockdaemon validators; 250K+ nodes launched.

## APIs profiled in this repo

| API | Surface |
|---|---|
| Data API (Ubiquity) | Unified REST data across 50+ chains — blocks, transactions, balances, UTXO, fees, protocols |
| RPC API | Shared and dedicated JSON-RPC and WebSocket nodes for Bitcoin, Ethereum, Solana, Polygon, Cosmos, Polkadot, NEAR, Cardano, Stellar, XRP, Tron, Monad, Hyperliquid, and Layer-2s |
| Staking API | Validator creation and signed staking intents across Ethereum, Solana, Cosmos, Polkadot, Polygon, NEAR, Cardano, Avalanche, Binance |
| Staking Reporting API | Standardized rewards, validator status, and yield reports for audit and accounting |
| DeFi API (expand.network) | DEX swaps, bridge swaps, lending/borrowing on Aave V2/V3 and Compound V2/V3 with EIP-5792/EIP-7702 batching |
| Token Pricing API | Token metadata, tags, and pricing (Beta) |
| Chain Watch Events API | Real-time on-chain event streaming via webhook, Kafka, or WebSocket targets with rules and variables |
| Management API | Compute Unit and request usage metrics plus organization audit logs |
| Wallet Transact API | Wallet-application toolbox for scaling multi-chain wallet operations |
| Builder Vault TSM | MPC wallet platform with EVM Web3 provider, Helm chart, and reference integrations |
| Institutional Vault | Self-hosted MPC vault with Automated Approver Service |

See [`apis.yml`](apis.yml) for the full APIs.json catalog entry.

## Artifacts

- [`apis.yml`](apis.yml) — APIs.json catalog entry
- [`capabilities/`](capabilities) — Naftiko capabilities for the Data, RPC, Staking, Staking Reporting, DeFi, Chain Watch, and Management APIs
- [`plans/blockdaemon-plans-pricing.yml`](plans/blockdaemon-plans-pricing.yml) — API Commons Plans for Free, Starter, Growth, and Enterprise tiers
- [`rate-limits/blockdaemon-rate-limits.yml`](rate-limits/blockdaemon-rate-limits.yml) — Per-product RPS/RPM limits, Compute Unit costs, and 429 handling
- [`finops/blockdaemon-finops.yml`](finops/blockdaemon-finops.yml) — FOCUS-aligned FinOps definition for Compute Unit metering
- [`json-ld/blockdaemon-context.jsonld`](json-ld/blockdaemon-context.jsonld) — JSON-LD context mapping Blockdaemon concepts
- [`json-schema/`](json-schema) — JSON Schemas for balance, validator, and unified event records
- [`vocabulary/blockdaemon-vocabulary.yml`](vocabulary/blockdaemon-vocabulary.yml) — Operational vocabulary across protocols, validators, vaults, and DeFi
- [`examples/`](examples) — Example request/response payloads for balances, staking intents, and Chain Watch events

## Authentication

Three modes are supported:

- `Authorization: Bearer <YOUR_API_KEY>`
- `X-API-Key: <YOUR_API_KEY>`
- Query parameter `?apiKey=<YOUR_API_KEY>`

API keys are issued from the Blockdaemon dashboard after KYB.

## Pricing model

The Blockdaemon API Suite meters every call in **Compute Units** (XS=1, S=5, M=10, L=50, XL=100). Subscriptions bundle a monthly CU allotment, a Requests-Per-Second ceiling, and a support SLA:

| Plan | CU/month | RPS | Support |
|---|---|---|---|
| Free | 3M | 5 | 8h weekday |
| Starter | 65M | 100 | 24h weekday |
| Growth | 365M | 200 | 24/7 |
| Enterprise | Custom | Custom | 24/7/365 dedicated |

Staking API is rate-limited at 250 RPM; Staking Reporting is 1 CU per request; Dedicated Nodes have no rate limit.
