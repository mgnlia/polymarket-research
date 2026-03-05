# Polymarket Week-1 Numeric Risk Guardrails

_Date: 2026-03-05_

## Hard Guardrails
1. **Quote-width cap:** 
   - Operational spread <= **80% of rewardsMaxSpread**.
   - Example: max 3.5c => quote <= 2.8c.

2. **Two-sided uptime:**
   - Midpoint in [0.10, 0.90]: both sides live >= **95%** of quote-life.
   - Midpoint <0.10 or >0.90: both sides live **100%** (or exit market).

3. **Per-market capital cap:**
   - Max **35%** in a single market (core market cap).
   - Max **10%** in edge-zone markets (>0.90 or <0.10 midpoint).

4. **Low-flow reward cap:**
   - Total allocation to low-volume but rewarded markets <= **20%**.

5. **Event-risk freeze window:**
   - Stop passive quoting **24h before known binary catalysts** where adverse selection spikes.

6. **Inventory imbalance limits (per market):**
   - Warning at net delta > **8%** of total portfolio notional.
   - Hard stop at > **12%**, skew/flatten immediately.

7. **Rebate diversification:**
   - Keep **25–35%** of deployed capital in rebate-eligible categories (crypto/NCAAB/Serie A) where available.

8. **Daily realized PnL instrumentation:**
   - Track rebates via `rebates/current` endpoint daily.
   - Track positions + PnL via user positions endpoint.
   - If 2-day realized reward <50% of expected model reward, rotate out of bottom 1–2 markets.

## KPI Targets (Week-1)
- Positive daily USDC net PnL: >= 5 of 7 days.
- Reward collection consistency: >= 6 of 7 daily payouts.
- Mean quoted spread compliance: >= 90% time within cap.
- Inventory breach incidents: <= 1 hard-stop breach/week.

## Source references
- Liquidity rewards mechanics: https://docs.polymarket.com/market-makers/liquidity-rewards
- Maker rebates: https://docs.polymarket.com/market-makers/maker-rebates
- Holding rewards: https://help.polymarket.com/en/articles/13364459-holding-rewards
- Rebates endpoint: https://docs.polymarket.com/api-reference/rebates/get-current-rebated-fees-for-a-maker
- Positions endpoint: https://docs.polymarket.com/api-reference/core/get-current-positions-for-a-user
