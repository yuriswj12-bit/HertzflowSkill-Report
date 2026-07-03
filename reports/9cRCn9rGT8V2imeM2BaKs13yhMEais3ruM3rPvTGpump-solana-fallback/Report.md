# SOL_MEME (Solana meme 9cRCn9...pump) — On-chain Decision Briefing

> ⚠️ **Main chain likely out of coverage (mirror-slice warning)**: This token is also deployed on solana — a chain this tool cannot do transfer-level on-chain forensic on, so holdings/distribution/sell-out there are invisible to this report. If solana is the token's real home (with the Alpha listing chain Solana only a mirror), this report covers just the mirror slice and the risk read is incomplete — the conclusions and verdict below are based on the Solana side only, not the token as a whole.
> ⚠️ **Real-time market data not ready**: neither surf `project-detail` nor the Binance Alpha API returned a live price for this token. The "Token market" table below is skipped. Verify temporarily via the chain explorer + the main pool address.

> ℹ️ **Solana on-chain detection coverage note**: surf's `onchain-sql` currently **does not cover** Solana
> (the `agent.solana_transfers` / `_dex_trades` tables do not exist;
> surf only provides on-chain SQL on BSC / Ethereum / Arbitrum / Base / Polygon / Optimism).
> This report **automatically skips** the following forensic sections, which depend on surf SQL transfers tables:
> - Pre-launch insider distribution trace (Rule 11 deployer trace)
> - Confirmed sell-out quantification (dump_tracker top sellers)
> - Recent 72h anomaly large transfers (anomaly transfer SQL)
> - Wash setup detection (wash_infra detector)
> - LP 24h net flow + LP creation time (lp_24h_flow / TGE first-trade SQL)
>
> **Kept**: Alpha API real-time market data (price/vol/mcap/FDV/holder count), surf `token-holders` (top-50 holdings + Arkham labels), section_alloc, monitoring_paste export.
>
> **Manual verification**: use Solscan / Birdeye / DEX Screener for depth + holder distribution; use the Helius / Shyft APIs to pull SPL Token Program mint / transfer instructions.
_Tool version 1.2.6 · Main chain Solana · Alpha listed N/A_

_Total supply 999,991,818 · Circulating 999,991,818 (100.0%) · Type MEME_LIKELY_
_Tier S1 · S1 —_

## 📋 Decision summary

| Item | Value |
|---|---|
| **🎯 Risk score** | **⬜⬜⬜⬜⬜⬜⬜⬜⬜⬜ (0/10)** |
| **On-chain state label** | **No significant trigger** — No significant on-chain detection trigger |
| Primary chain | solana |
| **Entry cap (LP 5% depth)** | **—** |
| Near-term catalysts | None |
| Blind spots you must cross-check yourself | Solana meme fallback: surf onchain-sql is unavailable; holder snapshot uses surf token-holders REST.; 主战场 solana 的链上 SQL 不在 surf 覆盖, forensic SQL 段全部跳过, 仅保留 Alpha 实时 + token-holders 快照 |

> 🎯 **Meaning of the 5 on-chain-state labels** (deterministically derived at render time, describing on-chain detection state only, not trading advice):
> - **No significant trigger** — no significant on-chain detection signal (risk 0-2)
> - **Watching** — some activity but no primary signal triggered (risk 2-5)
> - **Distributed and exited** — historical operator already distributed; on-chain historical sell-pressure released (risk 4-7)
> - **Dormant insider, undistributed** — dormant insider wallets have not distributed; timing unpredictable (risk 6-9)
> - **Recent distribution** — large on-chain activity in the last 72h (risk 7-10)

> This run is a Solana meme fallback, not a Binance Alpha full forensic. The pipeline captured supply and current top holders, but Solana SQL detectors are unavailable. The main actionable signal is concentration: one unlabeled wallet controls roughly 58.66% of circulating supply, while the top-50 snapshot covers about 71.68% as unclassified holder balance.



## 🎯 On-chain state: No significant trigger (risk score 0/10)

**No significant on-chain detection trigger**


| Decision anchor | Value | Status |
|---|---|---|
| Alpha 5% slippage cap | Unknown | 🔴 Very thin |
| DEX main pool USD liquidity | — | 🔴 |
| Pool token 24h net throughput (NOT LP add/remove) | — | 🟢 |


## 🧠 Current on-chain behaviour profile

> ℹ️ **No major behaviour profile triggered** — all 10 on-chain detection signal detectors returned OFF. This usually happens with: (a) Solana / non-EVM chain aborts (no surf SQL coverage); (b) freshly-deployed unlisted tokens (insufficient data); (c) genuinely clean tokens. Read it together with the 🎯 on-chain state above and the top on-chain-detection-limit callout.


## 🔴 Confirmed sell-out (insider lower bound)

### 🎯 Pump counterparty check

> **⚡ Quick read**: circulating 637.4M tokens · **non-operator sell-pressure 8.0%** (50,778,546 tokens = verifiable within top 100 holders 8.0%) · operator ammo 92.0% (⚠️ Alpha API reports 1000M circulating, on-chain dumpable 637M = 0.64x, Alpha overstates (includes mint authority / vesting lockup)) · relay·liquidity pool (CEX deposits + DEX pools — operator-added vs retail-traded, unsplittable) 0.0% (0 CEX / DEX pools) · insider confirmed realization $0 (0.0% of circulating) ⚠️ **detector did not identify operator sells** — on-chain net sell = 0 means the detector threshold was not met (mining_fed / mint_authority / m6 insider DEX swap all uncaptured); it does not mean there were no sells — see the funding_attribution + 24h vol sections.

> ⚠️ **Three-bucket sanity check triggered** — the following buckets are ≈ 0%, investigate:
> - **relay·liquidity pool 0%**: Mainstream BSC Alpha tokens usually reach Binance/Gate/Bitget. Check: (a) is the surf top_holders cex category empty? (b) are the cex_hot_wallet labels complete (Arkham)? (c) the CEX source addresses detected by cex_fanout hubs should be in cex_pool
> When the operator wants to pump, **the potential sellers = the held chips that don't belong to the operator**. The smaller this is, the more confident the operator is to pump (less fear of being dumped on); the larger, the more cautious.

| Chip bucket | Tokens | % of current circulating | Interpretation |
|---|---:|---:|---|
| 🟣 **Operator / project-controlled chips** | **586,641,676** | **92.0%** | **High control** — low theoretical pump resistance, but also strong active-distribution capacity |
| 🔥 **Verifiable non-operator sell-pressure** | **50,778,546** | **8.0%** | **Moderate external sell-pressure** (includes retail whales + protocol contracts + bridge transit) |
| 🟦 **relay·liquidity pool (CEX + DEX, neutral · unsplittable)** | **0** | **0.0%** | 0 exchange hot/cold/deposit wallets. On-chain it is **impossible to distinguish** retail deposit aggregation vs project custody reserve. During a pump it may flow out from either side |

### Key judgment

**High control + light external counterparty** — the operator has active-distribution capacity and low pump resistance, but the distribution pace determines the one-sided move.

<details>
<summary>🔍 Expand: operator-ammo 11-sub-bucket detail (with raw total + overlap note)</summary>

| Sub-bucket | Tokens | % of circulating | Note |
|---|---:|---:|---|
| ①a Public lockup / treasury / airdrop contract outside m6 lineage | 0 | 0.0% | Sablier / Hedgey / custom lockups. Public release schedule, **won't dump immediately during a pump**. Lower bound after subtracting the 0 unminted reserve |
| ①b Movable multisig outside m6 lineage | 0 | 0.0% | Gnosis Safe Proxy etc. The operator can transfer today with one signature |
| ② m6 lineage portion in circulation | 0 | 0.0% | m6 lineage total holdings 0 minus lockup 0. Includes pure insiders (0) |
| ⚠️ ③ Exchange-withdrawal distribution (net control not computable) | — | — | Gross inflow; phase-2 SQL truncated; net fan-out cannot be computed.  |
| ⑥'' Heuristic hidden ammo (top-100 unclassified ≥ 3%) | 586,641,676 | 92.0% | 1 wallets. **The 3% threshold risks false positives** — cross-check via monitoring_paste |
| ━━━━━ | ━━━━━ | ━━━━━ | ━━━━━ |
| Operator ammo raw total | 586,641,676 | 92.0% | Sum of buckets assuming no overlap. Upper-bound estimate |

**Notes**:
- The quick-read "operator ammo" is a **wallet-level back-calculation**: iterate the top 100 and de-dup-sum those in the operator set. Different from the raw total — raw is per-bucket upper bound (with overlap), quick-read is strictly de-duplicated.
- The quick-read "non-operator sell-pressure" includes **retail whales + protocol contracts (Wormhole / veVELVET etc.)**, not all of which is true retail. It is an upper bound.
- ①a vesting / ⑥ mint reserve → **won't dump immediately** during a pump; enters circulation only over the medium term.
- ①b multisig / ⑥' cluster → **transferable today**, different in nature from "lockup".
- Algorithm version: operator-ammo / non-operator-sell-pressure reverse algorithm v0.8.4.8.

</details>

#### 🔍 Verifiable non-operator sell-pressure wallet detail (reverse calc)

> Top-100 holders that are in neither the operator set nor the relay·liquidity pool. Operator set: m6 lineage + multisig / public lockup / treasury / airdrop contracts + heuristics + detector hits. **All CEX wallets + DEX liquidity pools are removed** (neutral "relay·liquidity pool": operator-added/retail-deposited vs retail-traded, unsplittable). Verifiable non-operator sell-pressure is mainly real retail whales + bridge + DeFi protocol contracts.

| # | Wallet | Current balance | % circulating | Type | Arkham label |
|---:|---|---:|---:|---|---|
| 1 | [`CLM6E4zpTviEC7`](https://solscan.io/account/CLM6E4zpTviEC77nWKogpVLQoXx9tgoQCYJ8NibxKg1Q) | 9,901,865 | 1.55% | Unclassified | — |
| 2 | [`Ac9Y9QLBw5evBn`](https://solscan.io/account/Ac9Y9QLBw5evBnV5X7647kHfqEcqmA2wgbuN6Sb1zSZM) | 9,500,006 | 1.49% | Unclassified | — |
| 3 | [`FnzKY6x7entQ1e`](https://solscan.io/account/FnzKY6x7entQ1eR3D225dQyT7ybfka4PskBMQhb8L3CC) | 6,310,123 | 0.99% | Unclassified | — |
| 4 | [`CxCTVjvgK3bWcg`](https://solscan.io/account/CxCTVjvgK3bWcgavMKo8PushR8ycw1atrWiSTruZrdtT) | 5,906,060 | 0.93% | Unclassified | — |
| 5 | [`HCgo8gvk99Wk13`](https://solscan.io/account/HCgo8gvk99Wk13XWbbAoyxyEx2DgzidzVDma4ny32uYC) | 4,211,693 | 0.66% | Unclassified | — |
| 6 | [`6HcrxubcevZQs1`](https://solscan.io/account/6HcrxubcevZQs1fcPTVnywzw7N2XWqsyAPxqnmg78UMg) | 4,035,725 | 0.63% | Unclassified | — |
| 7 | [`HDixbrzwwLXczh`](https://solscan.io/account/HDixbrzwwLXczhDBk1JVrurPQsuLE8FUKnW2pucSXN3o) | 3,800,062 | 0.60% | Unclassified | — |
| 8 | [`GkdYWRjFzZW3ox`](https://solscan.io/account/GkdYWRjFzZW3oxbRaPJ43C5385E4GtfgW3vwfK2ZAtac) | 3,587,446 | 0.56% | Unclassified | — |
| 9 | [`3H9LVHarjBoZ2Y`](https://solscan.io/account/3H9LVHarjBoZ2YPEsgFbVD1zuERCGwfp4AeyHoHsFSEC) | 3,525,568 | 0.55% | Unclassified | — |
| ━━━━━━━━━━━━━━━━━ | ━━━━━━━━━━━━━━━━━ | ━━━━━━━━━ | ━━━━━━━ | ━━━━━━━━━ | ━━━━━━━━━ |
| **Total verifiable non-operator sell-pressure (within top 100 holders)** | 9 wallets | **50,778,546** | **8.0%** | — | — |

> ⚠️ **Nature of non-operator sell-pressure**: mainly true retail whales + protocol contracts like Wormhole / veVELVET (user-deposited) + bridge transit. Large bare addresses (no Arkham label + > 1% circulating) are suspect as either operator aliases or true retail whales — cross-check wallet activity via monitoring_paste below.

---

| Item | Value |
|---|---|
| Tracked wallets | **0** (0 standard insiders; mining / bridge token, no pre-launch m6 lineage) |
| Insider-tree current holdings (incl. lockup, conservation anchor) | 0.0000% of supply (0 tokens, includes unreleased lockup + CEX/DEX transit balances, **not equal to the insider-controlled figure**) |
| (a) Confirmed sell-out — CEX deposit | 0 |
| (b) Confirmed sell-out — DEX swap (own wallet) | 0 (0 swaps) |
| **Confirmed gross sell-out, a+b** | **≥ 0 (circulating share unknown)** |
| **Confirmed net sell-out** | **Cannot reliably estimate** — mining / bridge token with an empty m6 lineage, so dump_tracker does not run the net algorithm. Reference: the 100 ht_dumpers' total **throughput** is 0 tokens (= 0.0x of circulating), which includes **a lot of wash, not all of which is selling**. Real selling < throughput, possibly on the order of 0.1-0.5x circulating, but depends on the operator's degree of wash |



> ⚠️ **Confirmed sell-out incomplete**: the CEX/DEX confirmation query still failed or was out of coverage, so the figures above may understate further. Re-run or verify manually on the chain explorer.


<a id="section-recent-anomaly"></a>
## 📊 Risk-signal aggregation (detectors + rhythm)

### Detector summary

| emoji | Category | Count | Interpretation |
|---|---|---|---|
| ⚪ | Pre-launch insider distribution | 0 | Skipped because Solana transfer SQL is unavailable in Surf for this pipeline. |
| ⚪ | Fully-distributed insider wallets | 0 | No full-dumper classification was produced because deployer lineage tracing was skipped. |
| ⚪ | Quiet wallets (never distributed) | 0 | No quiet-wallet set was produced; current top-holder concentration is the usable proxy. |
| ⚪ | Recent 72h anomaly large transfers | 0 | Recent 72h large-transfer SQL was skipped on Solana holder-snapshot mode. |

### Rhythm recognition

**No transfer-wave rhythm available in Solana holder-snapshot mode**



<details>
<summary>📂 <strong>📊 Full anomaly event list (raw detail, grouped by distribution wave, UTC)</strong> — 0 distribution waves, 0 events total (click to expand the full timeline + wallet flows)</summary>


</details>


## Primary chain (MULTI-CHAIN)

| Item | Value |
|---|---|
| **Primary chain** | **solana** (single-chain, no BSC mirror; Binance Alpha lists the SPL token directly) |
| Mint chain (supply_chain) | solana, totalSupply 999,991,818 |
| Trading chain (trading_venue_chain) | solana (Alpha + DEX main pool) |
| Cross-chain distribution | **Single-chain solana** — Alpha lists the SPL token directly, no BSC / EVM mirror bridge; this report covers holder snapshot + Alpha realtime ONLY, **not** the on-chain-detection SQL sections |
| Report coverage | **HOLDER_SNAPSHOT (main chain solana)** — surf does not cover `onchain-sql` for solana (no `agent.solana_transfers` table), all on-chain-detection SQL sections skipped; Alpha realtime quotes + surf token-holders REST + monitoring export retained |

⚠️ Main chain solana runs in HOLDER_SNAPSHOT mode — surf onchain-sql does not cover this chain, all on-chain-detection SQL sections skipped. Realtime quotes / holders / mcap / FDV REST data fetch normally. Insider lineage / wash / flow-whale / cross-token (4 SQL detectors) have **no data**, the top banner says so; cross-check manually via Solscan / Helius / Shyft / Vybe

**Interpretation**: This token is handled as single-chain Solana holder-snapshot coverage. Transfer-level forensic sections are skipped because Surf has no Solana SQL tables.

## Entry-price anchor (TGE)

| Time anchor | UTC | Price | vs current |
|---|---|---|---|
| LP creation first tx (DEX start) | — | — | — |
| Alpha first tx | — | — | — |
| **Current price** | 2026-06-29 | — | 1.00× |

**Interpretation**: No Alpha listing timestamp, LP creation timestamp, or price anchor was available for this non-Alpha Solana meme fallback.

<a id="section-alloc"></a>
## Project allocation power (ALLOC)

| Item | Value | Source |
|---|---|---|
| Alpha quota (officially disclosed) | **Not disclosed** | Binance Alpha API does not expose this field |
| Deployer wallet `—` current balance | Unknown | Deployer distribution trace |
| Pre-launch insider recipients 0 cumulative balance | 0 tokens (= 0.00% of supply) | Insider wallet sum |
| Quiet wallets 0 holding (core future risk) | **0 tokens (= 0.00% of supply / $—)** | Insiders that never distributed |
| Fully-distributed insiders 0 (distribution complete) | 100% distributed, 0 remaining | Insiders with ≥95% distributed |

**Interpretation**: No deployer allocation tree was available. Current holder concentration is the usable allocation proxy for this Solana run.

## Near-term CEX catalyst (CEX-TRACE)

| Exchange | Status | Time | Since |
|---|---|---|---|
| Binance | Not listed | — | — |
| Aster | Unverified | — | — |
| Bitget | Unverified | — | — |

No new catalyst within 14 days. Current S1 (Alpha only).

**Interpretation**: Binance perp was not found for the fallback symbol, and Aster/Bitget probes are unverified. This section is not a catalyst signal for the raw Solana CA.

<a id="section-liq"></a>
## Entry ceiling (LIQ)

| Anchor | Value | Note |
|---|---|---|
| **Max single buy under 5% slippage (estimated)** | — | Derived from Alpha 24h vol (vol_24h / 96 × 0.05 heuristic estimate) |
| DEX main pool liquidity | — | No main pool |
| DEX main pool 24h volume | — | surf project-detail (cross-chain CEX+DEX realtime aggregation) |
| Pool token 24h net throughput (NOT LP add/remove) | — | surf does not cover this chain (no SQL table), see Solana banner at top |
| DEX main pool address | — |  |

**Interpretation**: No realtime price, Alpha volume, or labeled DEX pool liquidity was available. Entry-size and slippage anchors cannot be computed from this run.

<a id="section-holdings"></a>
## Holdings distribution by role

**Distribution table**:

| Role | Wallet # | Current balance | % of supply | Top wallet |
|---|---|---|---|---|
| DEX main pool | 0 | 0 | —% | — |
| Deployer wallet | 0 | 0 | —% | — |
| Project / infra / distribution pool (vesting / multisig / treasury / DEX infra / CEX custody / 3rd-party distribution platform / retail claim pool, Arkham-verified) | 1 | 3,104,397 | 0.3104% | [`ASTyfSima4…`](https://solscan.io/account/ASTyfSima4LLAdDgoFGkgqoKowG1LZFDr9fAQrg7iaJZ) |
| Quiet wallet (insider, never distributed) | 0 | 0 | —% | — |
| Other (retail + unclassified) | 49 | 716,805,831 | 71.6812% | [`GV6UUmNxz2…`](https://solscan.io/account/GV6UUmNxz2RpKxmNAPadYKb7uQpszwqQAu3qLJxVdC52) |

**Key takeaways**:
- Insider tracking: **0** wallets hold **0.0%** of supply cumulatively  (mining / bridge token, no pre-launch m6 lineage).
- Insiders have on-chain-confirmed outflow of **0.0M USD** = **0.00%** of circulating, priced at the insider self-sell TWAP (not the wash quote).

<details>
<summary>📂 <strong>Backward trace (Deployer → insider lineage)</strong> — 0 insider wallets: 0 fully distributed / 0 distributing / 0 quiet (click to expand the full lineage + wallet balances + distribution rate)</summary>

**Insider wallet list (deployer distribution trace)**:

| ID | Address | Received from deployer | Current balance | Dumped % |
|---|---|---|---|---|
_Stats (full m6 lineage, **0** wallets): 0 near-zero holdings / public-lockup custody · 0 distributing · 0 fully distributed_

**m4_notes (pre-LP allocation interpretation)**:
- No deployer-side transfer lineage was produced because this non-Alpha Solana mint uses holder-snapshot fallback mode.
- Solana holder-snapshot mode found no deployer lineage because Surf does not expose Solana transfer SQL tables for this pipeline.
- Use the holder table and monitoring export as the actionable view; deployer-to-insider provenance is intentionally marked unavailable on this chain.



</details>

## 💰 High-Value Address Funding Source (mint / DEX / P2P)

Below are the high-value addresses already surfaced by the wash setup / flow operator / m6 insider / Top-30 holder sections, classified by how they ACQUIRED their tokens over the past 365 days: mint (received directly from 0x0 — covers mining contracts, bridge mint authorities, airdrop mint contracts), DEX buy (received from a known DEX main pool), or P2P (any other EOA transfer, including unidentified CEX withdrawals). Use this to distinguish: ⛏️ high mint% = mining-token operator or sockpuppet airdrop farmer; 🟢 high DEX% = real retail buyer; 🔵 high P2P% = operator aggregation hub or OTC recipient.

> ⏭️ **Funding-source section skipped** — surf_no_sql_solana.


<a id="section-monitoring"></a>
## Monitored wallets + real-time alerts


> 📊 **Monitoring priority (v0.7.27 deterministic ranker)**: 🚨 1 CRITICAL · 🔥 0 HIGH · 👀 0 NORMAL>
> Wallets in paste.json are sorted by level, 🚨 first. Prioritize CRITICAL+HIGH (1) — when these wallets move, the on-chain detection picture changes. NORMAL (0) is for bulk cross-checking, no push notification needed. 💤 NOT_TRACKED are DEX routers / public CEX hot wallets whose flow noise drowns the real signal, removed from paste.


| # | Level | Wallet | Role | primary role section | Trigger condition | Status |
|---|:-:|---|---|---|---|---|
| 1 | 🚨 CRITICAL | [`GV6UUmNxz2`](https://solscan.io/account/GV6UUmNxz2RpKxmNAPadYKb7uQpszwqQAu3qLJxVdC52) | Heuristically-flagged hidden operator ammo (reserve) | — | Tag type: heuristically-flagged hidden operator ammo (≥ 10% circulating + no Arkham label). The user can watch whether / when these three on-chain behaviours occur: (1) splitting across multiple downstream accounts, (2) transferring into an Arkham-labeled exchange deposit address, (3) on-chain matching (direct transfer-out against USDT/BNB/WBNB etc.). If (2)(3) appear, combine with this report's confirmed sell-out section insider self-sell TWAP to estimate the actual realized USD. | 🟡 |

Import the monitoring paste file and watch the critical holder for splits, exchange deposits, or rapid downstream distribution. Solana addresses are case-sensitive, so keep the exact address casing from the export.

## Machine-readable JSON (compact)

```json
{
  "schema_version": "1.2.6",
  "symbol": "SOL_MEME",
  "verdict": "ADVISORY",
  "verdict_zh": "Observe",
  "verdict_downgrade_applied": 0,
  "chain_state": "CLEAN",
  "chain_state_label": "No significant on-chain detection trigger",
  "chain_state_risk_score": 0,
  "alpha_listing_tier": "S1",
  "any_anomaly_firing": false,
  "render_provenance": {
    "rendered_by": "render_report.py (v0.6, jinja2)",
    "data_source": "report_data.json (LLM-filled, Python-validated)",
    "deterministic": true
  },
  "structural_counts": {
    "anomaly_waves": 0,
    "evidence_graph_entries": 0,
    "holdings_role_rows": 5,
    "holdings_progress_bars": 5,
    "monitoring_wallets": 1,
    "lineage_flowchart_nodes": 0,
    "lineage_flowchart_edges": 0,
    "m6_rows": 0,
    "decision_anchors": 3,
    "decision_re_entry_conditions": 1
  },
  "address_role_index": {}
}
```

---

****Data research only, not investment advice. evidence_graph contains 0 stable IDs for provenance tracing.****
