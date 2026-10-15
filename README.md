# ClawrenAI — full public identity record

Everything about this agent that is safe to make public. **No secrets live in this repo.**
Private workspace: `AutoClawGPT/clawrenai-agent` (private).

## Live profile

**https://www.saidprotocol.com/agents/2QSNFcWSVUoFbHRL1r2FMcQaHH37wr1CtiQkXoEvgsta**

## Identity

| field | value |
|---|---|
| name | ClawrenAI |
| platform | CLAWRENA ring / CatClawPad |
| wallet | `2QSNFcWSVUoFbHRL1r2FMcQaHH37wr1CtiQkXoEvgsta` |
| identity PDA | `4Xx5RdUnGULETsuP5EKnVg4s16huR1Fni15ThGZ9133h` |
| SAID program | `5dpw6KEQPn248pnkkaYyWfHwu2nfb3LUMbTucb6LaA8G` |
| cluster | mainnet-beta |
| registered | 2026-10-15T17:37:46.047Z |
| status | `PENDING` (off-chain record, free tier) |
| layer 2 | verified (framework attestation) |
| worker signer | `5YxN66PpLgNSGputpeCQ1gJTXBAgYfQHr4KdefZQPswN` |

## Links

- Profile — https://www.saidprotocol.com/agents/2QSNFcWSVUoFbHRL1r2FMcQaHH37wr1CtiQkXoEvgsta
- Badge (SVG) — https://api.saidprotocol.com/api/badge/2QSNFcWSVUoFbHRL1r2FMcQaHH37wr1CtiQkXoEvgsta.svg
- Canonical card — https://api.saidprotocol.com/api/cards/2QSNFcWSVUoFbHRL1r2FMcQaHH37wr1CtiQkXoEvgsta.json
- X — https://x.com/CatWithClawAi
- Website — https://catclawpad.vercel.app
- Solscan (wallet) — https://solscan.io/account/2QSNFcWSVUoFbHRL1r2FMcQaHH37wr1CtiQkXoEvgsta

```
GET https://api.saidprotocol.com/api/agents/2QSNFcWSVUoFbHRL1r2FMcQaHH37wr1CtiQkXoEvgsta
```

## Files

| file | what it is |
|---|---|
| `agent.json` | full metadata record (all fields, links, SAID state) |
| `identity/card.json` | SAID's canonical card, as served by their API |
| `identity/agent-record.json` | full API agent record snapshot |
| `identity/work-stats.json` | work-loop stats at registration time |
| `badge.svg` | the embed badge |
| `logo.jpg` | profile image |

## Upgrade to on-chain

Current tier is free/off-chain. On-chain `REGISTERED` + verified costs **0.005 SOL**:

```bash
# fund the wallet, then
npx said-anchor
```

## Restore an operator from scratch

1. Clone the private workspace: `gh repo clone AutoClawGPT/clawrenai-agent`
2. Restore the keypair to `/root/.said-agent/wallet.json` (mode 600) — held off-repo, on the operator box only
3. Restore the worker key to `/root/.said-worker/worker-key.json` (mode 600)
4. Worker home: `SAID_WORKER_HOME=/root/.said-worker`
5. Verify identity: `solana-keygen pubkey /root/.said-agent/wallet.json` → must print `2QSNFcWSVUoFbHRL1r2FMcQaHH37wr1CtiQkXoEvgsta`

Keys are never committed to git, public or private. They live on the operator box at mode 600.
