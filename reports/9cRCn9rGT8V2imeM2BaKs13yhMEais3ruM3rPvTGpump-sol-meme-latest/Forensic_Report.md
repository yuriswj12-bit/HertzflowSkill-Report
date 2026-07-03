# ANSEM (The Black Bull) — 链上决策简报

## 🎯 一屏结论

> 本段由 GMGN holder/trader/tag 样本和 HertzFlow Solana forensic view 确定性推导，不构成买卖建议。详细证据在下方各段。

| 维度 | 结论 | 关键证据 |
|---|---|---|
| **当前阶段** | 🔴 MM/机器人主导的分发交易 | MM 候选 181 个; 可见卖出下界 $5.57M |
| **筹码结构** | 🟣 高控盘 | Top10 持仓 63.24%; Top1 持仓 58.66% |
| **资金/分发结构** | 🔴 多集群同源分发 | 最大分发源 `E99pfU...HUTe` 连接 72 个下游 |
| **做市/MM 地址集群** | 🔴 已显著浮现 | bundler 钱包 1000 个; 前 5 分发集群 MM 命中 73 个 |
| **派发/套现情况** | 🟠 样本内部分套现 | GMGN top traders 卖出下界 $5.57M; 买入额 $8.59M |
| **盘口阶段** | 🟠 中市值 + 薄承接 | mcap $123.14M; LP $1.33M; 24h volume $45.01M |
| **监控重点** | 盯分发源 + 回流地址 | P0: `E99pfU...HUTe`, `GV6UUm...dC52`, `5URyNU...c19Y` |

**一句话**: 高控盘 + MM/机器人集群 + 分发源已浮现；当前更像做市主导的分发交易，而不是普通散户盘。

## 🎯 速读摘要 (中文)

> 本段供快速散户阅读 / AI 二次解读。详细链上侦测在下方各段，含英文术语。本段全部基于链上数据派生，不含买卖建议。

- **项目**: The Black Bull (ANSEM), Solana mint `9cRCn9rGT8V2imeM2BaKs13yhMEais3ruM3rPvTGpump`
- **当前行情**: 价格 `$0.12314538`，市值约 **$123.14M**，DEX 主池流动性约 **$1.33M**，holders **76,436**。
- **核心风险**: Top10 持仓 **63.24%**，Top1 `GV6UUm...dC52` 单独持仓 **58.66%**。
- **MM / 做市集群**: 识别到 **181** 个 MM/机器人候选地址；最大分发源 `E99pfU...HUTe` 连接 **72** 个下游，其中 **59** 个命中 MM/机器人特征。
- **已确认样本内卖出下界**: top traders 可见卖出约 **$5.57M**。注意这只是 GMGN 返回样本下界，不等于全链真实出货总额。
- **如何使用本报告**: 重点看下方 **重点监控钱包**，优先盯 P0 分发源、回流地址、以及已高额卖出的 MM 下游。

> ⚠️ **本报告读前必看 — Solana MVP 侦测限制 / 数据提醒**
>
> - 本报告不是 Binance Alpha EVM Surf-SQL 全量 forensic；它基于 GMGN holder/trader/tag 样本聚类。
> - “MM/操盘集群”是强行为判断：同源资金、同一分发来源、同一回流去向、bundler/dex_bot 标签、高成交低库存等信号叠加。
> - 未接入 Helius/Shyft/Vybe 前，无法展开完整 SPL transfer graph 和 Jupiter/Raydium/Meteora inner instructions；真实派发量可能高于本报告下界。
_工具版本 sol_meme forensic view · 主链 Solana · 数据拉取时间 2026-07-01 04:56:35 UTC · 报告生成时间 2026-07-01 04:56:36 UTC_

## 💹 代币行情 (实时)

| 项目 | 取值 |
|---|---|
| **项目名称** | **The Black Bull** (ANSEM) |
| Mint | `9cRCn9rGT8V2imeM2BaKs13yhMEais3ruM3rPvTGpump` |
| 主战场链 | Solana |
| **当前价** | **$0.12314538** |
| **24H 成交** | **$45.01M** (buy $22.19M / sell $22.82M, swaps 163,655) |
| 当前 LP (DEX 主池) | $1.33M |
| 市值 / 供应 | $123.14M / 999.96M |
| 数据来源 | GMGN CLI · 持币 76,436 个 · Smart/KOL 88/46 |

## 📋 决策摘要

| 项目 | 取值 |
|---|---|
| **🎯 风险评分** | **🟥🟥🟥🟥🟥🟥🟥🟥🟥🟥 (10/10)** |
| **链上状态标签** | **近期派发 / MM主导** — 样本内多分发源、多回流路径、MM/机器人标签密集 |
| 主战场链 | solana |
| **进场上限提示** | 主池 LP $1.33M，但 Top1/Top10 控盘过高，不能用 LP 单独判断承接 |
| 短期催化 | 未在 GMGN 基础数据中确认 |
| 必须自行交叉核对的盲区 | CEX/OTC、跨钱包后续兑换、完整 SPL inner instructions |

> ANSEM 判定：**不适合按普通散户盘理解**。当前链上状态更接近 MM/机器人集群主导的高控盘分发盘；若已有持仓，应重点盯 P0 分发源和回流地址继续转出/卖出。

## 🎯 链上状态: 近期派发 / MM主导 (风险评分 10/10)

**GMGN 样本内识别到 9 个综合关系集群、16 个分发来源集群、27 个同源资金集群、1 个收集/回流去向集群。**

| 决策锚点 | 数值 | 状态 |
|---|---:|---|
| DEX 主池 USD 流动性 | $1.33M | 🟠 |
| Top10 holder rate | 63.24% | 🔴 高控盘 |
| GMGN bundler wallets | 1000 | 🔴 机器人/打包痕迹重 |
| 样本内卖出下界 | $5.57M | 🟠 部分套现已发生 |

## 🧠 当前链上行为画像

| 严重度 | 标签 | 类别 | 触发指标 | 链上事实 |
|:-:|---|---|---|---|
| 🔴 **STRONG** | `S-C1` 同源分发集群 | C 出货行为 | `distribution_clusters=16` | 多个地址从同一上游收币后卖出或继续转出，最大分发源连接 72 个下游 |
| 🔴 **STRONG** | `S-R1` 综合资金关系集群 | D 协同结构 | `relationship_clusters=9` | 同资金来源、同分发源、同回流地址、相近 funding 时间/金额、同 bot 栈被合并成地址集群 |
| 🔴 **STRONG** | `S-B1` MM/机器人做市 | B 成交制造 | `mm_candidates=181, bundlers=1000` | 大量 bundler/dex_bot/axiom/photon/padre 地址，高成交低库存，符合做市/刷量/分发下游特征 |
| 🔴 **STRONG** | `S-A1` 高控盘 | A 筹码结构 | `top10=63.24%, top1=58.66%` | Top1/Top10 持仓过高，外部可验证散户抛压难以充分确认 |
| 🟠 **MEDIUM** | `S-C2` 样本内套现 | C 出货行为 | `sell_lower=$5.57M` | top traders 可见卖出为真实链上成交样本下界，不含 CEX/OTC/跨钱包后续兑换 |
| 🟠 **MEDIUM** | `S-D1` 回流/收集路径 | D 协同结构 | `collect_clusters=1` | 多个地址的最近 transfer-out 指向同一地址，疑似边分发边归集库存 |

## 🔴 真实派发 (样本内确认卖出下界)

### 🎯 拉盘对手盘验证

> **速读**: 总供应约 999.96M · **操盘/MM/机器人相关 12.36%** (前 5 分发集群当前持仓合计) · DEX 主池流动性 $1.33M · 样本内可见卖出下界 $5.57M。

| 筹码桶 | 估算 | 解读 |
|---|---:|---|
| 🟣 **操盘/MM/机器人相关** | **12.36%** | 前 5 个分发集群当前持仓合计；可见卖出 $6.18M |
| 🟦 **DEX 池 / 流动性侧** | **$1.33M** | 主池流动性，不等同于可承接真实卖压 |
| 🔥 **可验证非集群散户抛压** | **未充分确认** | SOL MVP 暂无完整 transfer graph，只能把非集群地址作为待排除对象 |

#### 🟣 前 5 个分发集群明细

> 上面的 **12.36%** 不是凭空估算，而是下表 5 个分发源当前持仓占比相加。卖出额是 GMGN 归一化后的 USD 估算；实际链上兑现资产是池子 quote 资产，这里按主池 SOL/USD ≈ $75.61 折算为 SOL。当前USD是未兑现库存估值，不计入“已兑现”。

| # | 分发源 | AI解读 | 下游地址数 | MM命中 | 当前持仓 | 已实现利润 | 未实现利润 | 未兑现库存USD | 卖出额USD | 已兑现SOL估算 | 代表下游 |
|---:|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---|
| 1 | `E99pfU...HUTe` | 已经盈利，主要利润仍在库存 | 72 | 59 | 8.54% | $2.59M | $5.77M | $10.53M | $4.48M | 59,315 SOL | 3CPHk5...FkWY, 9H9HU7...C4AZ, 8e9bkF...6qg6, 9aP2vS...SR5T, F5hkYs...xqs6 |
| 2 | `GV6UUm...dC52` | 已经盈利，主要利润仍在库存 | 10 | 7 | 1.44% | $817,539 | $1.51M | $1.78M | $1.17M | 15,435 SOL | 5URyNU...c19Y, 5FGoPP...rp8V, HDixbr...XN3o, 6btcCb...g5eT, DAEdBm...CvHC |
| 3 | `Dtw3GC...p2hs` | 已经盈利，主要利润仍在库存 | 4 | 3 | 1.25% | $124,329 | $683,013 | $1.54M | $365,557 | 4,835 SOL | HCgo8g...2uYC, 6Hcrxu...8UMg, GkdYWR...Atac, B2f9t2...k418 |
| 4 | `B4Z8JS...JdpF` | 已经盈利，主要利润仍在库存 | 2 | 2 | 1.14% | $156,727 | $1.27M | $1.40M | $140,367 | 1,856 SOL | CLM6E4...Kg1Q, ACTbvb...y831 |
| 5 | `5RMzPY...95AF` | 已实现盈利 | 2 | 2 | 0.00% | $1,018 | $0.63 | $2.99 | $19,905 | 263.25 SOL | 1337tf...qKKo, FZANgq...RH8n |

### 关键判断

**高控盘 + 分发源集中 + MM 地址密集** — 拉盘阻力可能低，但主动派发能力也强；真正要盯的是分发源是否继续向下游拨币，以及回流地址是否继续归集/再分发。

## 📊 风险信号聚合 (检测器 + 节奏)

### 检测器汇总

| emoji | 类别 | 数量 | 解读 |
|---|---|---:|---|
| 🔴 | 同一分发来源集群 | 16 | 多地址从同一上游收币后卖出/转出，疑似操盘下游 |
| 🔴 | MM/机器人候选 | 181 | bundler/dex_bot/axiom/photon/padre + 高成交低库存 |
| 🟠 | 样本内套现地址 | 139 | 已出现高卖出额、高已卖比例或大额转出 |
| 🟠 | 收集/回流路径 | 1 | 多个地址 transfer-out 指向同一去向 |

### 节奏识别

**三段节奏 — 初始筹码集中 → 分发源向下游拨币 → MM/机器人地址卖出并回流(进行中)**

- 第一段 初始集中: Top1 `GV6UUm...dC52` 当前仍持 58.66%，是最大单点筹码风险。
- 第二段 下游分发: `E99pfU...HUTe`、`GV6UUm...dC52` 等分发源连接多地址下游。
- 第三段 套现/回流: top traders 可见卖出 $5.57M，且出现同一回流去向，说明不是单向自然换手。

## 🧬 持有人资金关联与内幕筹码判断

> 本段已经把地址关系图消化成结论，不要求用户自己读一堆地址。完整地址明细保留在文末机器 JSON，正文只保留能影响判断的关键结论。

### 结论

- **主控集群已经成型**: `cluster_01` 覆盖 198 个样本钱包，MM/机器人命中 161 个，套现命中 118 个，当前持仓约 **73.66%**。
- **不是散户自然分布**: 该集群同时命中同 SOL 资金来源、同 token 分发源、同回流路径、相近 funding 时间/金额、bot 标签栈等特征，符合“同一操盘体系多钱包执行”的结构。
- **主库存仍在**: `GV6UUm...dC52` 当前持仓 **58.66%**，是最大单点库存风险；它的转出会比普通地址卖出更重要。
- **分发已经发生**: 样本内最大卖出成员 `3CPHk5...FkWY` 可见卖出 **$549,651**；主集群累计可见卖出 **$7.57M**。
- **回流/收集线索**: `8psNvW...VRtf` 是当前样本内最重要的收集/回流去向，连接 3 个上游。

### 这对交易决策意味着什么

| 观察点 | 解释 | 用户该怎么用 |
|---|---|---|
| 主集群持仓 73.66% | 控盘筹码仍然集中在同一关系图内 | 不要把 holder 数量当成分散度，优先看主集群是否继续转出 |
| 主集群已卖 $7.57M | 已出现边做市边兑现的行为 | 如果后续卖出继续增加，说明派发未结束 |
| Top1 库存 58.66% | 单点库存足以改变盘口 | 盯该地址是否继续向下游或池子方向移动 |
| 回流去向 `8psNvW...VRtf` | 有归集/回收库存迹象 | 盯回流后是否再分发给新下游 |

### 只保留关键集群摘要

| 集群 | AI 判断 | 钱包数 | 当前持仓 | 已卖下界 | 核心证据 |
|---|---|---:|---:|---:|---|
| `cluster_01` | 主控/MM集群 | 198 | 73.66% | $7.57M | same_sol_funder:3a8DRp...gLVj / same_token_distributor:yHCxHB...6PRe / same_token_collector:5URyNU...c19Y |
| `cluster_02` | 次级分发/回流集群 | 2 | 1.05% | $0 | same_sol_funder:GJvewf...T4YA / same_token_distributor:9KoXy9...CwhL / same_token_collector:9KoXy9...CwhL |
| `cluster_03` | 次级分发/回流集群 | 2 | 0.00% | $11,166 | same_sol_funder:D4YBDB...WMoj / same_token_distributor:6jmUvt...6xz1 / same_funder_30m:D4YBDB...9212 |

## 📌 重点监控钱包

这里只给最少但最有用的监控对象：主库存、分发源、回流地址、最高卖出执行地址。其余地址放在 JSON，避免正文变成地址清单。

| 优先级 | 地址 | 角色 | 为什么盯 | 触发信号 |
|---|---|---|---|---|
| P0 | `GV6UUmNxz2RpKxmNAPadYKb7uQpszwqQAu3qLJxVdC52` | 主库存/单点控筹 | 当前持仓 58.66% | 继续 transfer-out 或大额卖出 |
| P0 | `E99pfUw985q5qk5Aa6ERXqJwsBjoE1igPwNfHBabHUTe` | 最大分发源 | 连接 72 个下游，MM命中 59 个 | 继续向新地址拨币 |
| P0 | `8psNvWTrdNTiVRNzAgsou9kETXNJm2SXZyaKuJraVRtf` | 收集/回流地址 | 连接 3 个上游 | 收到筹码后再分发 |
| P1 | `3CPHk5b7SRvAsTsocehAu1bA5YKMXJYMr3qc2SuMFkWY` | 最高卖出执行地址 | 可见卖出 $549,651 | 继续卖出或转给新地址 |

## 机器可读 JSON 精简

```json
{
  "schema": "hertzflow_sol_meme_forensic_v1",
  "token": {
    "chain": "solana",
    "address": "9cRCn9rGT8V2imeM2BaKs13yhMEais3ruM3rPvTGpump",
    "symbol": "ANSEM",
    "name": "The Black Bull",
    "price_usd": 0.12314538,
    "market_cap_usd": 123140755.02896334,
    "liquidity_usd": 1331218.773056348,
    "holders": 76436
  },
  "verdict": {
    "risk_score": 10,
    "chain_state": "RECENT_DISTRIBUTION_MM_DOMINATED",
    "one_liner": "高控盘 + MM/机器人集群 + 分发源已浮现；当前更像做市主导的分发交易，而不是普通散户盘。",
    "limitations": [
      "GMGN holder/trader/tag sample, not full Solana transfer graph",
      "sell_lower_bound excludes CEX/OTC/cross-wallet later swaps",
      "MM labels are behavioral unless directly tagged by source"
    ]
  },
  "metrics": {
    "top10_holder_rate": 0.6324,
    "top1_holder_rate": 0.5866437697965792,
    "bundler_wallets": 1000,
    "mm_candidate_count": 181,
    "cashout_candidate_count": 139,
    "sell_lower_bound_usd": 5571881.882424356,
    "buy_sample_usd": 8587495.280565735,
    "distribution_cluster_count": 16,
    "funding_cluster_count": 27,
    "collection_cluster_count": 1,
    "relationship_cluster_count": 9
  },
  "top_clusters": {
    "relationship": [
      {
        "id": "cluster_01",
        "score": 100,
        "wallet_count": 198,
        "mm_count": 161,
        "cashout_count": 118,
        "hold_rate": 0.7366492960612381,
        "buy_usd": 9444333.394226398,
        "sell_usd": 7566443.641862883,
        "transfer_in_amount": 739481326.783052,
        "transfer_out_amount": 762324085.39932,
        "features": [
          "same_sol_funder:3a8DRp...gLVj",
          "same_token_distributor:yHCxHB...6PRe",
          "same_token_collector:5URyNU...c19Y",
          "same_funder_30m:3a8DRp...9802",
          "same_funder_amount:3a8DRp..._0.1",
          "same_created_1h:494901",
          "same_entry_15m:1979604",
          "same_sol_funder:2snHHr...kKuS"
        ],
        "representatives": [
          "GV6UUmNxz2RpKxmNAPadYKb7uQpszwqQAu3qLJxVdC52",
          "3CPHk5b7SRvAsTsocehAu1bA5YKMXJYMr3qc2SuMFkWY",
          "5URyNUmhcuWdZiiQrtNdFrSbQPfq72UV2gqQasr9c19Y",
          "D3dGSyWF53e9DZDZb5m2WapCuABN1JcCt2q8EhwaqEm8",
          "2S8E25nAcqvvMYEWZHBQk22GzevwvmsVNAs6Gw5tRX7d",
          "99ZbtoWfTeHtBUGkHixJaquL1g3BtPkBgCsZjP6sbtt1",
          "HCgo8gvk99Wk13XWbbAoyxyEx2DgzidzVDma4ny32uYC",
          "6btcCbEdYnCUyuzV3JEMDpw9YbbF1tPFzNSN2Sfwg5eT"
        ]
      },
      {
        "id": "cluster_02",
        "score": 31,
        "wallet_count": 2,
        "mm_count": 0,
        "cashout_count": 1,
        "hold_rate": 0.010500402494003467,
        "buy_usd": 2029.92782975274,
        "sell_usd": 0.0,
        "transfer_in_amount": 10541816.872978,
        "transfer_out_amount": 7088728.189447,
        "features": [
          "same_sol_funder:GJvewf...T4YA",
          "same_token_distributor:9KoXy9...CwhL",
          "same_token_collector:9KoXy9...CwhL",
          "same_funder_30m:GJvewf...9101",
          "same_funder_amount:GJvewf...A:10",
          "same_created_1h:494550",
          "same_entry_15m:1980009",
          "same_funder_30m:GJvewf...8040"
        ],
        "representatives": [
          "Ac9Y9QLBw5evBnV5X7647kHfqEcqmA2wgbuN6Sb1zSZM",
          "Ctk7mEh2NMCJKRs9KWu2c59eJc4xE9kAkGHTzizo6tD"
        ]
      },
      {
        "id": "cluster_03",
        "score": 30,
        "wallet_count": 2,
        "mm_count": 2,
        "cashout_count": 2,
        "hold_rate": 5.063634174908707e-09,
        "buy_usd": 10697.288886887161,
        "sell_usd": 11165.675582611411,
        "transfer_in_amount": 5.2130339999999995,
        "transfer_out_amount": 0.0,
        "features": [
          "same_sol_funder:D4YBDB...WMoj",
          "same_token_distributor:6jmUvt...6xz1",
          "same_funder_30m:D4YBDB...9212",
          "same_funder_amount:D4YBDB...oj:5",
          "same_created_1h:494606",
          "same_entry_15m:1980868",
          "same_sol_funder:4UGbSm...iWHR",
          "same_funder_30m:4UGbSm...6444"
        ],
        "representatives": [
          "CEq8qbEpk2sWr7Pi7T8kXScWUaM6NmCJCCdni1uortz5",
          "DrnuP46qcf7b7utTY9Esm46SwkTFhYu4TrtRGTyvkE67"
        ]
      },
      {
        "id": "cluster_04",
        "score": 30,
        "wallet_count": 2,
        "mm_count": 2,
        "cashout_count": 2,
        "hold_rate": 0.0,
        "buy_usd": 214.55497271114,
        "sell_usd": 228.5325076313,
        "transfer_in_amount": 0.794298,
        "transfer_out_amount": 0.0,
        "features": [
          "same_sol_funder:DhZJG8...L8C6",
          "same_token_distributor:J9KgS8...8Eyq",
          "same_funder_30m:DhZJG8...7409",
          "same_funder_amount:DhZJG8...:0.5",
          "same_created_1h:480670",
          "same_entry_15m:1980735",
          "same_bot_stack:bundler,gmgn",
          "same_sol_funder:74DRAx...apri"
        ],
        "representatives": [
          "3jezhDoBDKE5ehjgWYj6y5tuBQoum3r3nmbAM7qVFKrL",
          "25fbgxUaUZkjHnNHBSbGYmjyV5vMDNvyqFBLZKHDKQvg"
        ]
      },
      {
        "id": "cluster_05",
        "score": 24,
        "wallet_count": 2,
        "mm_count": 1,
        "cashout_count": 0,
        "hold_rate": 0.002888555201940719,
        "buy_usd": 298355.0488174176,
        "sell_usd": 18533.08267526318,
        "transfer_in_amount": 920000.0,
        "transfer_out_amount": 0.0,
        "features": [
          "same_sol_funder:CSEncq...2RCs",
          "same_funder_30m:CSEncq...7290",
          "same_funder_amount:CSEncq...s:20",
          "same_created_1h:493645",
          "same_entry_15m:1980874",
          "same_sol_funder:7qJ5MC...DNeT",
          "same_token_distributor:7qJ5MC...DNeT",
          "same_funder_30m:7qJ5MC...5613"
        ],
        "representatives": [
          "HLRAw55adZRYLR7YoiDxYLVu4NN92jQyzGt3zhdh3x3a",
          "5A7FdZMS2vm7RFQ5FRpXzp2EDccnisWP5GLwGDm2veCj"
        ]
      },
      {
        "id": "cluster_06",
        "score": 24,
        "wallet_count": 3,
        "mm_count": 0,
        "cashout_count": 0,
        "hold_rate": 0.002762104797800891,
        "buy_usd": 0.0,
        "sell_usd": 33988.41691284309,
        "transfer_in_amount": 2999997.061431,
        "transfer_out_amount": 0.0,
        "features": [
          "same_sol_funder:5QDsAv...6g1L",
          "same_token_distributor:9JCB8K...axJ4",
          "same_funder_30m:5QDsAv...5308",
          "same_funder_amount:5QDsAv..._0.1",
          "same_created_1h:482654",
          "same_entry_15m:1980520",
          "same_sol_funder:9JCB8K...axJ4",
          "same_funder_30m:9JCB8K...6465"
        ],
        "representatives": [
          "2kRgLqiRUJFiCs46GDJbaeH63T6kR3fS1T6d3j6NkBcS",
          "5N2Aeq556NdR8Gn93UZmGccJksXbfJ3J96M5TJ7PCFZi",
          "HpNtDG2qRPcvcXMszdUyBvdu3GEEZGh1kLNfXbdB933B"
        ]
      },
      {
        "id": "cluster_07",
        "score": 22,
        "wallet_count": 2,
        "mm_count": 0,
        "cashout_count": 0,
        "hold_rate": 0.00727021726548284,
        "buy_usd": 0.0,
        "sell_usd": 5093.92672271019,
        "transfer_in_amount": 7302780.93226,
        "transfer_out_amount": 0.0,
        "features": [
          "same_sol_funder:CxCTVj...rdtT",
          "same_token_distributor:CxCTVj...rdtT",
          "same_funder_30m:CxCTVj...2107",
          "same_funder_amount:CxCTVj..._0.1",
          "same_created_1h:486053",
          "same_entry_15m:1980920",
          "same_sol_funder:7cRyJD...R3q6",
          "same_funder_30m:7cRyJD...2248"
        ],
        "representatives": [
          "8wLPuPpZgbxnhTMiMG3suqsQgYQ1oy1s8nVYJjaT33m4",
          "BVvLf9EXkGBWG4ffzzwiQPafkVPnQ9yydSHU7r12cYxA"
        ]
      },
      {
        "id": "cluster_08",
        "score": 20,
        "wallet_count": 2,
        "mm_count": 2,
        "cashout_count": 2,
        "hold_rate": 0.0026427108248224477,
        "buy_usd": 642107.2034710523,
        "sell_usd": 239885.95821661383,
        "transfer_in_amount": 0.0,
        "transfer_out_amount": 0.0,
        "features": [
          "same_sol_funder:6tckHF...LoDQ",
          "same_funder_30m:6tckHF...0356",
          "same_funder_amount:6tckHF...DQ:2",
          "same_created_1h:495178",
          "same_entry_15m:1980918",
          "same_sol_funder:Gabz2r...9hob",
          "same_funder_30m:Gabz2r...8644",
          "same_funder_amount:Gabz2r...:0.1"
        ],
        "representatives": [
          "8s2MNRtz4d8ytu4wu8UnFi8ePWTKUWXB61inL59Trmez",
          "gEy39aH539VZoQhmM6mdWy7AMywdA3oAQ2YBXWhBKmh"
        ]
      }
    ],
    "distribution": [
      {
        "source": "E99pfUw985q5qk5Aa6ERXqJwsBjoE1igPwNfHBabHUTe",
        "wallet_count": 72,
        "mm_count": 59,
        "hold_rate": 0.08538520184941485,
        "buy_usd": 6164598.8714244785,
        "sell_usd": 4484844.355164994,
        "representatives": [
          "3CPHk5b7SRvAsTsocehAu1bA5YKMXJYMr3qc2SuMFkWY",
          "9H9HU7RsFnovQ9jPXo4Er9EPCdNQaHEtey8f6CpAC4AZ",
          "8e9bkF9q2cZqRpLqGNgimr19mhHarW7p1yvSreTC6qg6",
          "9aP2vSFp2rydWR7C7kVZSQLQa2sT62w23ZHVP8BVSR5T",
          "F5hkYsi8JxjyA2JHN5CA7MbnnhWubkXB2ZQB7Gkaxqs6"
        ]
      },
      {
        "source": "GV6UUmNxz2RpKxmNAPadYKb7uQpszwqQAu3qLJxVdC52",
        "wallet_count": 10,
        "mm_count": 7,
        "hold_rate": 0.014441193403437653,
        "buy_usd": 124752.3513850514,
        "sell_usd": 1167068.7806465207,
        "representatives": [
          "5URyNUmhcuWdZiiQrtNdFrSbQPfq72UV2gqQasr9c19Y",
          "5FGoPPj1nL8LCnfVnpTmreqQtqLuMXXAwuS1uahMrp8V",
          "HDixbrzwwLXczhDBk1JVrurPQsuLE8FUKnW2pucSXN3o",
          "6btcCbEdYnCUyuzV3JEMDpw9YbbF1tPFzNSN2Sfwg5eT",
          "DAEdBmTPEKM6xkwfzC3d411QUe6coKpkND6UURa4CvHC"
        ]
      },
      {
        "source": "Dtw3GCTNWpGrCNbTCNAh7ayda2NiWBF1RiGwtL8rp2hs",
        "wallet_count": 4,
        "mm_count": 3,
        "hold_rate": 0.012463347083982433,
        "buy_usd": 537349.0937090766,
        "sell_usd": 365557.3773503542,
        "representatives": [
          "HCgo8gvk99Wk13XWbbAoyxyEx2DgzidzVDma4ny32uYC",
          "6HcrxubcevZQs1fcPTVnywzw7N2XWqsyAPxqnmg78UMg",
          "GkdYWRjFzZW3oxbRaPJ43C5385E4GtfgW3vwfK2ZAtac",
          "B2f9t2AQKHE2jK24iCxC95zmgvcuZxkkK9HUjvd3k418"
        ]
      },
      {
        "source": "B4Z8JSSVCNWW5gkYgxrrTZKwVfnqMCxYZS9cPQLeJdpF",
        "wallet_count": 2,
        "mm_count": 2,
        "hold_rate": 0.011354233329063138,
        "buy_usd": 138222.99875218648,
        "sell_usd": 140367.03007088703,
        "representatives": [
          "CLM6E4zpTviEC77nWKogpVLQoXx9tgoQCYJ8NibxKg1Q",
          "ACTbvbNm5qTLuofNRPxFPMtHAAtdH1CtzhCZatYHy831"
        ]
      },
      {
        "source": "5RMzPYkhxk74m6xyp47HqxCG6hT2qWTgRFPaFS5S95AF",
        "wallet_count": 2,
        "mm_count": 2,
        "hold_rate": 2.41548081821309e-08,
        "buy_usd": 18806.55504751453,
        "sell_usd": 19904.70095729796,
        "representatives": [
          "1337tfZ2aYuCEY14XWz5d1bnYkSyREuwM5DaPBeaqKKo",
          "FZANgqGEj8uiGD7s39T4iUvYwSY5BsYQ8RvWkAz9RH8n"
        ]
      }
    ],
    "funding": [
      {
        "source": "AxiomRXZAq1Jgjj9pHmNqVP7Lhu67wLXZJZbaK87TTSk",
        "wallet_count": 19,
        "mm_count": 19,
        "hold_rate": 0.0054430974477018435,
        "buy_usd": 454028.43622648326,
        "sell_usd": 401406.48896657256,
        "representatives": [
          "4hSXPtxZgXFpo6Vxq9yqxNjcBoqWN3VoaPJWonUtupzD",
          "ACTbvbNm5qTLuofNRPxFPMtHAAtdH1CtzhCZatYHy831",
          "38CX6Y75mvRxC8rNFhCAUtZ6SLwdyR1NMoY4SNwTmUMJ",
          "9g7TscgkUbqu7fJNNq43BVUP6zp21AzET77YKLbS6as9",
          "GijFWw4oNyh9ko3FaZforNsi3jk6wDovARpkKahPD4o5"
        ]
      },
      {
        "source": "5tzFkiKscXHK5ZXCGbXZxdw7gTjjD1mBwuoFbhUvuAi9",
        "wallet_count": 11,
        "mm_count": 8,
        "hold_rate": 0.005442738133323074,
        "buy_usd": 185563.5219537822,
        "sell_usd": 247071.39854181994,
        "representatives": [
          "B2f9t2AQKHE2jK24iCxC95zmgvcuZxkkK9HUjvd3k418",
          "GmCqxJx2QPxKfhyiLyk5CdV3rQtwuXKnCoTq5RoFBCoD",
          "JBM3QhZgNgUZZzRdbHVrQULLtb7BphmJdR4JPu6mE7kG",
          "9JCB8Kr71PVnJ2XekxRUfozo7QVYb4G2dJZabbo5axJ4",
          "5Ukb6d8hjoZ3vMPK1TPMPUq2w89cwkNWYN2S7du5tHBJ"
        ]
      },
      {
        "source": "2snHHreXbpJ7UwZxPe37gnUNf7Wx7wv6UKDSR2JckKuS",
        "wallet_count": 6,
        "mm_count": 6,
        "hold_rate": 0.012745120256243463,
        "buy_usd": 212642.70400785073,
        "sell_usd": 191030.92078847226,
        "representatives": [
          "CLM6E4zpTviEC77nWKogpVLQoXx9tgoQCYJ8NibxKg1Q",
          "E9cnYgPfwbDmd5qXs4r3h3g9gWERRrz2cgJ9AbPoiucR",
          "5w5QUq1LWwd7KzzGyJEWuDHg8kymMX4j1VQ9CpGCg9E8",
          "6aHKA2wsyjL7kmANYkpAKykjr9d9Rgnnc2ztzvTqqegh",
          "65paNEG8m7mCVoASVF2KbRdU21aKXdASSB9G3NjCSQuE"
        ]
      },
      {
        "source": "CZ5H8Fiuf6HCLQXeNuZio9yU63d2un6Nu5PnrD1YwnR8",
        "wallet_count": 6,
        "mm_count": 5,
        "hold_rate": 0.008565212299831345,
        "buy_usd": 323251.3534309278,
        "sell_usd": 375232.3236543043,
        "representatives": [
          "GA1G2wmJcRzPipLMdjMgEcyRDgPRuBSaNNQWr77T9j4e",
          "6T8Var5aHQd2m1XBFC9ovHJvkex94wNHd5NQwpPGWW6N",
          "78thMY8yfYzXGRhSArPMr7j8Rsh5QEPZviHVPfEfoMDM",
          "4npDgDGmDCRFUm8ZzWEG6mzpVYSj1yTLdJDpoGnanhFG",
          "DytQyNJjG1xVtvTKkKbPcU9UQMMgf4WAbigu332SzE1P"
        ]
      },
      {
        "source": "iGdFcQoyR2MwbXMHQskhmNsqddZ6rinsipHc4TNSdwu",
        "wallet_count": 5,
        "mm_count": 5,
        "hold_rate": 0.004832276830030906,
        "buy_usd": 410517.6579708241,
        "sell_usd": 74998.90408701006,
        "representatives": [
          "H8MQegokeJxeWfNiD3MNk8Bykso99s7qWGdtTKu3hmZY",
          "7ybzureiACHnxt8pRcCHrU8pM6oD1c5s3qkkegfz1L7P",
          "GrhYtk4TycV1dwWXRCxxRgJMS1mkX1HBhipo7Z3556PP",
          "9Q6d9XZ4r2gsRY9wjz4mBjxsZcy154nZuc2E4uwaLhhd",
          "hnu69n6P5CgYXCtUKii9wgamqtDeTVHY3TVJ6HKt7wC"
        ]
      }
    ],
    "collection": [
      {
        "target": "8psNvWTrdNTiVRNzAgsou9kETXNJm2SXZyaKuJraVRtf",
        "wallet_count": 3,
        "mm_count": 2,
        "hold_rate": 0.004423462959656376,
        "buy_usd": 654495.120880655,
        "sell_usd": 701804.9269350199,
        "representatives": [
          "2S8E25nAcqvvMYEWZHBQk22GzevwvmsVNAs6Gw5tRX7d",
          "8e9bkF9q2cZqRpLqGNgimr19mhHarW7p1yvSreTC6qg6",
          "9L8gedW6GyFyJhmTcq2Er3dgr338HczuAaUYFUwCwXmw"
        ]
      }
    ]
  },
  "watchlist": [
    {
      "priority": "P0",
      "address": "GV6UUmNxz2RpKxmNAPadYKb7uQpszwqQAu3qLJxVdC52",
      "role": "主库存/单点控筹",
      "reason": "当前持仓 58.66%",
      "trigger": "继续 transfer-out 或大额卖出"
    },
    {
      "priority": "P0",
      "address": "E99pfUw985q5qk5Aa6ERXqJwsBjoE1igPwNfHBabHUTe",
      "role": "最大分发源",
      "reason": "连接 72 个下游，MM命中 59 个",
      "trigger": "继续向新地址拨币"
    },
    {
      "priority": "P0",
      "address": "8psNvWTrdNTiVRNzAgsou9kETXNJm2SXZyaKuJraVRtf",
      "role": "收集/回流地址",
      "reason": "连接 3 个上游",
      "trigger": "收到筹码后再分发"
    },
    {
      "priority": "P1",
      "address": "3CPHk5b7SRvAsTsocehAu1bA5YKMXJYMr3qc2SuMFkWY",
      "role": "最高卖出执行地址",
      "reason": "可见卖出 $549,651",
      "trigger": "继续卖出或转给新地址"
    }
  ]
}
```


## 方法边界

- 这份报告已经把 GMGN 的 holder/trader/tag 样本做了聚类，但还不是完整 Solana transfer graph。
- 当前“MM/操盘集群”属于强行为判断：同源资金、同一分发来源、同一收集去向、bot/bundler 标签、高成交低库存等信号叠加。
- 如果要做到 Binance Alpha EVM 那种完整取证，需要继续接 Helius/Shyft/Vybe，把 SPL transfer 和 Jupiter/Raydium/Meteora inner instructions 全量展开。
