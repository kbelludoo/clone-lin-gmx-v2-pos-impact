# clone-lin-gmx-v2-pos-impact

Experimental LIN clone of GMX V2 `capPositiveImpactUsdByMaxPositionImpact` (uint64-scale, FLOAT' = 1e6).

- **Upstream:** [gmx-io/gmx-synthetics](https://github.com/gmx-io/gmx-synthetics) `contracts/market/MarketUtils.sol` commit `a85ea3491c19c93bb4b5a002d9b358fb769b7849` (GPL-2.0-or-later after BUSL Change Date 2026-08-31).
- **LIN kernel:** [`src/lin_gmx_v2_pos_impact.lin`](src/lin_gmx_v2_pos_impact.lin)
- **Proofs (lin-open only):** [kbelludoo/lin-open](https://github.com/kbelludoo/lin-open) `examples/gmx_v2_pos_impact/` and `python3 test/prove_gmx_v2_pos_impact_external.py`
- **Class:** EXPERIMENTAL. Not Arbitrum GMX V2 uint256 / FLOAT=1e30. Not a production replacement.

Named goldens (uint64-scale): clip **100000000** vs uncapped **150000000**; stay **50000000**; equal **100000000**; negative passthrough **-200000000** vs symmetric abs **-100000000**; pos-factor clamp **50000000** vs noclamp **100000000**; factor 0 **0** vs stay **150000000**; pool-based **150000000** vs sizeDelta **100000000**; 128-bit wrap **14000000000000** vs naive i64 **-4446744073709**.
