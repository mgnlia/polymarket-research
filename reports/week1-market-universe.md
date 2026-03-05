# Polymarket Week-1 Market Universe (Money + Airdrop Farming)

_Date: 2026-03-05_

## Objective
Maximize sustainable USDC income (liquidity rewards + rebates + spread capture) while preserving clean behavior for future POLY airdrop eligibility.

## Ranking Method
Rank = reward density (daily rate) × tradability (tight spread + volume) × risk-adjusted midpoint suitability.

## Tier A (Core deployment)
1. **Will the Iranian regime fall before 2027?**  
   - Condition: `0xbb4d51...a1f3b`
   - Rewards: **300/day**
   - Min size: **200**
   - Max spread: **3.5c**
   - Midpoint: ~0.50 (best for two-sided quoting)
   - Why: Highest reward density and midpoint-friendly scoring.

2. **Will Republicans control the Senate after 2026 midterms?**  
   - Condition: `0x86bfb5...d72587`
   - Rewards: **70/day**
   - Min size: **200**
   - Max spread: **3.5c**
   - Midpoint: ~0.58
   - Why: Strong reward pool + reasonable two-sided market state.

## Tier B (Selective add-ons)
3. **Will Manchester City win EPL 2025–26?**  
   - Condition: `0xfb1835...3a1573`
   - Rewards: **10/day**
   - Min size: **200**
   - Max spread: **4.5c**
   - Midpoint: ~0.18 (edge-adjacent risk)
   - Why: Moderate reward, but use smaller size due asymmetric risk.

4. **Low-rate diversification slots (1–3/day markets)**
   - Examples observed: Discord IPO 30B+, Fetterman run before 2027, CT governor (Dem), NH GOP primary candidate.
   - Why: Useful for category diversity and activity history, **not** core reward ROI.

## Allocation Templates
### If capital = $1,000
- Tier A #1: 40%
- Tier A #2: 35%
- Tier B #3: 10%
- Diversification slots: 10%
- Cash/holding buffer: 5%

### If capital = $5,000
- Tier A #1: 35%
- Tier A #2: 30%
- Rebate-eligible markets (crypto / NCAAB / Serie A): 20%
- Tier B #3 + other diversifiers: 10%
- Cash/holding buffer: 5%

## Exclusions (Week-1)
- Markets with midpoint >0.90 or <0.10 as core holdings.
- Very low-flow markets as primary capital sink.
- Markets where live spread frequently sits above rewards max spread without reliable top-of-book access.

## Sources
- https://clob.polymarket.com/sampling-markets?limit=120
- https://docs.polymarket.com/market-makers/liquidity-rewards
- https://docs.polymarket.com/market-makers/maker-rebates
