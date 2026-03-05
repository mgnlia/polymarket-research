# Polymarket Pilot Day-1 Adjustments (Template + Initial Guidance)

_Date: 2026-03-05_

## What to measure at end of Day-1
Per market:
1. Realized liquidity rewards (USDC)
2. Realized maker rebates (USDC)
3. Net spread capture / slippage estimate
4. Fill count and inventory drift
5. Quote-time compliance vs spread cap

## Adjustment Rules (D+1)
- **Promote** market if:
  - realized reward >= 90% of expected share model
  - no hard inventory breach
  - spread cap compliance >= 90%

- **Hold** market if:
  - realized reward between 60–90% of expected
  - manageable inventory drift

- **Demote/exit** market if:
  - realized reward < 60% expected for 2 consecutive days
  - frequent non-compliance with max-spread threshold
  - edge-zone probability with repeated adverse fills

## Expected Week-1 Rotations
- Keep 2 core high-rate anchors.
- Rotate 1–2 low-rate diversifiers daily based on realized reward efficiency.
- Add rebate-eligible markets if reward-only markets underperform realized terms.

## Missing metric to finalize precision right now
- Wallet-specific realized rewards/rebates and exact fill telemetry are not included in current snapshot-only research pull.
- Proxy used: public reward metadata + spread/volume/liquidity state.

## Revised ETA for tighter Day-1 note
- After first 24h of wallet telemetry, publish quantified rotation decisions in <30 minutes.

## Key APIs for Day-1 automation
- Rebates current: https://docs.polymarket.com/api-reference/rebates/get-current-rebated-fees-for-a-maker
- Positions: https://docs.polymarket.com/api-reference/core/get-current-positions-for-a-user
- Rewarded market snapshot: https://clob.polymarket.com/sampling-simplified-markets?limit=300
