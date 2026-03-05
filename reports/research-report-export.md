# Exported Research Report: Polymarket Week-1 Deployment Brief — Money + Airdrop Farming

- Project ID: `ZAesQp0XyHy6AQIoZcyzc`
- Report ID: `nXgZxMF1xk0Fi9lJa9rdQ`
- Exported on: 2026-03-05

---

# Polymarket Week-1 Deployment Brief — Money + Airdrop Farming

## Goal
Maximize sustainable USDC income while building clean, durable on-platform activity for potential POLY airdrop eligibility.

## Ranked Week-1 Market Universe

### Tier A (Core)
1. **Will the Iranian regime fall before 2027?** (`0xbb4d51...a1f3b`)
   - Rewards: **300/day**, min size **200**, max spread **3.5c**, midpoint ~0.50.
   - Best reward density + midpoint profile for two-sided quoting.

2. **Will Republicans control the Senate after 2026 midterms?** (`0x86bfb5...d72587`)
   - Rewards: **70/day**, min size **200**, max spread **3.5c**, midpoint ~0.58.
   - Strong reward pool with better tradability than many long-tail markets.

### Tier B (Selective)
3. **Will Manchester City win EPL 2025–26?** (`0xfb1835...3a1573`)
   - Rewards: **10/day**, min size **200**, max spread **4.5c**, midpoint ~0.18.
   - Use smaller sizing because edge-adjacent midpoint increases asymmetry risk.

4. **Low-rate diversifiers (1–3/day)**
   - Examples observed: Discord IPO 30B+, Fetterman run before 2027, NH GOP primary, CT governor.
   - Good for category diversity/activity history; weak as core ROI engines.

## Numeric Risk Guardrails
1. **Quote width cap:** operational width <= **80% of rewardsMaxSpread** (3.5c -> 2.8c).
2. **Two-sided uptime:** >= **95%** in midpoint band [0.10, 0.90]; **100%** near extremes.
3. **Per-market capital cap:** <= **35%** core; <= **10%** for edge-zone (>0.90 or <0.10) markets.
4. **Low-flow rewarded market cap:** <= **20%** of total capital.
5. **Catalyst freeze:** halt passive quoting in final **24h** pre-event when adverse selection rises.
6. **Inventory hard-stop:** flatten/skew aggressively if net delta > **12%** of portfolio notional.
7. **Revenue diversification:** allocate **25–35%** to maker-rebate eligible categories (crypto/NCAAB/Serie A) where possible.

## Deployment Templates
- **$1k:** 40% Tier A#1, 35% Tier A#2, 10% Tier B, 10% diversifiers, 5% buffer.
- **$5k:** 35% Tier A#1, 30% Tier A#2, 20% rebate-eligible markets, 10% Tier B/diversifiers, 5% buffer.

## Day-1 Adjustment Logic
- Promote markets with realized >=90% expected reward and stable inventory.
- Hold markets at 60–90% expected.
- Demote/exit markets <60% expected for 2 days or with repeat spread-cap noncompliance.

## Current Limitation / Unblock
- Missing wallet-specific realized telemetry (fills, realized rewards/rebates) for precision ranking.
- Fallback used now: public reward metadata + spread/volume/liquidity state.
- Once 24h wallet telemetry exists, precise rotation note ETA: **<30 minutes**.

## Key Sources
- Rewarded markets snapshot: https://clob.polymarket.com/sampling-markets?limit=120
- Liquidity rewards math: https://docs.polymarket.com/market-makers/liquidity-rewards
- Maker rebates: https://docs.polymarket.com/market-makers/maker-rebates
- Holding rewards: https://help.polymarket.com/en/articles/13364459-holding-rewards
- Rebates endpoint: https://docs.polymarket.com/api-reference/rebates/get-current-rebated-fees-for-a-maker
- Positions endpoint: https://docs.polymarket.com/api-reference/core/get-current-positions-for-a-user
