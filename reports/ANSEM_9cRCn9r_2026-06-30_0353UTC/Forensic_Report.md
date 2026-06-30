# ANSEM (The Black Bull) — 链上决策简报

## 🎯 一屏结论

> 本段由 GMGN holder/trader/tag 样本和 HertzFlow Solana forensic view 确定性推导，不构成买卖建议。详细证据在下方各段。

| 维度 | 结论 | 关键证据 |
|---|---|---|
| **当前阶段** | 🔴 MM/机器人主导的分发交易 | MM 候选 176 个; 可见卖出下界 $5.73M |
| **筹码结构** | 🟣 高控盘 | Top10 持仓 63.47%; Top1 持仓 58.66% |
| **资金/分发结构** | 🔴 多集群同源分发 | 最大分发源 `E99pfU...HUTe` 连接 78 个下游 |
| **做市/MM 地址集群** | 🔴 已显著浮现 | bundler 钱包 1000 个; 前 5 分发集群 MM 命中 79 个 |
| **派发/套现情况** | 🟠 样本内部分套现 | GMGN top traders 卖出下界 $5.73M; 买入额 $7.25M |
| **盘口阶段** | 🟠 中市值 + 薄承接 | mcap $126.54M; LP $1.29M; 24h volume $56.46M |
| **监控重点** | 盯分发源 + 回流地址 | P0: `E99pfU...HUTe`, `GV6UUm...dC52`, `5URyNU...c19Y` |

**一句话**: 高控盘 + MM/机器人集群 + 分发源已浮现；当前更像做市主导的分发交易，而不是普通散户盘。

## 🎯 速读摘要 (中文)

> 本段供快速散户阅读 / AI 二次解读。详细链上侦测在下方各段，含英文术语。本段全部基于链上数据派生，不含买卖建议。

- **项目**: The Black Bull (ANSEM), Solana mint `9cRCn9rGT8V2imeM2BaKs13yhMEais3ruM3rPvTGpump`
- **当前行情**: 价格 `$0.12654404`，市值约 **$126.54M**，DEX 主池流动性约 **$1.29M**，holders **39,071**。
- **核心风险**: Top10 持仓 **63.47%**，Top1 `GV6UUm...dC52` 单独持仓 **58.66%**。
- **MM / 做市集群**: 识别到 **176** 个 MM/机器人候选地址；最大分发源 `E99pfU...HUTe` 连接 **78** 个下游，其中 **63** 个命中 MM/机器人特征。
- **已确认样本内卖出下界**: top traders 可见卖出约 **$5.73M**。注意这只是 GMGN 返回样本下界，不等于全链真实出货总额。
- **如何使用本报告**: 重点看下方 **重点监控钱包**，优先盯 P0 分发源、回流地址、以及已高额卖出的 MM 下游。

> ⚠️ **本报告读前必看 — Solana MVP 侦测限制 / 数据提醒**
>
> - 本报告不是 Binance Alpha EVM Surf-SQL 全量 forensic；它基于 GMGN holder/trader/tag 样本聚类。
> - “MM/操盘集群”是强行为判断：同源资金、同一分发来源、同一回流去向、bundler/dex_bot 标签、高成交低库存等信号叠加。
> - 未接入 Helius/Shyft/Vybe 前，无法展开完整 SPL transfer graph 和 Jupiter/Raydium/Meteora inner instructions；真实派发量可能高于本报告下界。
_工具版本 sol_meme forensic view · 主链 Solana · 生成时间 2026-06-30 03:53:56 UTC_

## 💹 代币行情 (实时)

| 项目 | 取值 |
|---|---|
| **项目名称** | **The Black Bull** (ANSEM) |
| Mint | `9cRCn9rGT8V2imeM2BaKs13yhMEais3ruM3rPvTGpump` |
| 主战场链 | Solana |
| **当前价** | **$0.12654404** |
| **24H 成交** | **$56.46M** (buy $28.07M / sell $28.40M, swaps 195,147) |
| 当前 LP (DEX 主池) | $1.29M |
| 市值 / 供应 | $126.54M / 999.99M |
| 数据来源 | GMGN CLI · 持币 39,071 个 · Smart/KOL 79/42 |

## 📋 决策摘要

| 项目 | 取值 |
|---|---|
| **🎯 风险评分** | **🟥🟥🟥🟥🟥🟥🟥🟥🟥🟥 (10/10)** |
| **链上状态标签** | **近期派发 / MM主导** — 样本内多分发源、多回流路径、MM/机器人标签密集 |
| 主战场链 | solana |
| **进场上限提示** | 主池 LP $1.29M，但 Top1/Top10 控盘过高，不能用 LP 单独判断承接 |
| 短期催化 | 未在 GMGN 基础数据中确认 |
| 必须自行交叉核对的盲区 | CEX/OTC、跨钱包后续兑换、完整 SPL inner instructions |

> ANSEM 判定：**不适合按普通散户盘理解**。当前链上状态更接近 MM/机器人集群主导的高控盘分发盘；若已有持仓，应重点盯 P0 分发源和回流地址继续转出/卖出。

## 🎯 链上状态: 近期派发 / MM主导 (风险评分 10/10)

**GMGN 样本内识别到 4 个综合关系集群、14 个分发来源集群、25 个同源资金集群、2 个收集/回流去向集群。**

| 决策锚点 | 数值 | 状态 |
|---|---:|---|
| DEX 主池 USD 流动性 | $1.29M | 🟠 |
| Top10 holder rate | 63.47% | 🔴 高控盘 |
| GMGN bundler wallets | 1000 | 🔴 机器人/打包痕迹重 |
| 样本内卖出下界 | $5.73M | 🟠 部分套现已发生 |

## 🧠 当前链上行为画像

| 严重度 | 标签 | 类别 | 触发指标 | 链上事实 |
|:-:|---|---|---|---|
| 🔴 **STRONG** | `S-C1` 同源分发集群 | C 出货行为 | `distribution_clusters=14` | 多个地址从同一上游收币后卖出或继续转出，最大分发源连接 78 个下游 |
| 🔴 **STRONG** | `S-R1` 综合资金关系集群 | D 协同结构 | `relationship_clusters=4` | 同资金来源、同分发源、同回流地址、相近 funding 时间/金额、同 bot 栈被合并成地址集群 |
| 🔴 **STRONG** | `S-B1` MM/机器人做市 | B 成交制造 | `mm_candidates=176, bundlers=1000` | 大量 bundler/dex_bot/axiom/photon/padre 地址，高成交低库存，符合做市/刷量/分发下游特征 |
| 🔴 **STRONG** | `S-A1` 高控盘 | A 筹码结构 | `top10=63.47%, top1=58.66%` | Top1/Top10 持仓过高，外部可验证散户抛压难以充分确认 |
| 🟠 **MEDIUM** | `S-C2` 样本内套现 | C 出货行为 | `sell_lower=$5.73M` | top traders 可见卖出为真实链上成交样本下界，不含 CEX/OTC/跨钱包后续兑换 |
| 🟠 **MEDIUM** | `S-D1` 回流/收集路径 | D 协同结构 | `collect_clusters=2` | 多个地址的最近 transfer-out 指向同一地址，疑似边分发边归集库存 |

## 🔴 真实派发 (样本内确认卖出下界)

### 🎯 拉盘对手盘验证

> **速读**: 总供应约 999.99M · **操盘/MM/机器人相关 14.57%** (前 5 分发集群当前持仓合计) · DEX 主池流动性 $1.29M · 样本内可见卖出下界 $5.73M。

| 筹码桶 | 估算 | 解读 |
|---|---:|---|
| 🟣 **操盘/MM/机器人相关** | **14.57%** | 前 5 个分发集群当前持仓合计；可见卖出 $5.87M |
| 🟦 **DEX 池 / 流动性侧** | **$1.29M** | 主池流动性，不等同于可承接真实卖压 |
| 🔥 **可验证非集群散户抛压** | **未充分确认** | SOL MVP 暂无完整 transfer graph，只能把非集群地址作为待排除对象 |

#### 🟣 前 5 个分发集群明细

> 上面的 **14.57%** 不是凭空估算，而是下表 5 个分发源当前持仓占比相加。卖出额是 GMGN 归一化后的 USD 估算；实际链上兑现资产是池子 quote 资产，这里按主池 SOL/USD ≈ $74.22 折算为 SOL。当前USD是未兑现库存估值，不计入“已兑现”。

| # | 分发源 | AI解读 | 下游地址数 | MM命中 | 当前持仓 | 已实现利润 | 未实现利润 | 未兑现库存USD | 卖出额USD | 已兑现SOL估算 | 代表下游 |
|---:|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---|
| 1 | `E99pfU...HUTe` | 已经盈利，主要利润仍在库存 | 78 | 63 | 9.84% | $2.27M | $7.54M | $12.45M | $3.53M | 47,528 SOL | 3CPHk5...FkWY, 9H9HU7...C4AZ, 8e9bkF...6qg6, F5hkYs...xqs6, 3inTyf...rTg2 |
| 2 | `GV6UUm...dC52` | 已经盈利，主要利润仍在库存 | 10 | 7 | 1.48% | $778,043 | $1.60M | $1.87M | $1.12M | 15,057 SOL | 5URyNU...c19Y, 5FGoPP...rp8V, HDixbr...XN3o, 6btcCb...g5eT, DAEdBm...CvHC |
| 3 | `Dtw3GC...p2hs` | 已经盈利，主要利润仍在库存 | 5 | 3 | 1.53% | $738,826 | $867,088 | $1.93M | $821,098 | 11,063 SOL | 3H9LVH...FSEC, HCgo8g...2uYC, 6Hcrxu...8UMg, GkdYWR...Atac, B2f9t2...k418 |
| 4 | `B4Z8JS...JdpF` | 已经盈利，主要利润仍在库存 | 3 | 3 | 1.72% | $590,618 | $2.05M | $2.18M | $385,776 | 5,198 SOL | CLM6E4...Kg1Q, CxCTVj...rdtT, ACTbvb...y831 |
| 5 | `6jmUvt...6xz1` | 已经盈利，主要利润仍在库存 | 3 | 3 | 0.01% | $1,305 | $1,460 | $8,970 | $14,275 | 192.34 SOL | 6msXZd...VmGW, CEq8qb...rtz5, DrnuP4...kE67 |

### 关键判断

**高控盘 + 分发源集中 + MM 地址密集** — 拉盘阻力可能低，但主动派发能力也强；真正要盯的是分发源是否继续向下游拨币，以及回流地址是否继续归集/再分发。

## 📊 风险信号聚合 (检测器 + 节奏)

### 检测器汇总

| emoji | 类别 | 数量 | 解读 |
|---|---|---:|---|
| 🔴 | 同一分发来源集群 | 14 | 多地址从同一上游收币后卖出/转出，疑似操盘下游 |
| 🔴 | MM/机器人候选 | 176 | bundler/dex_bot/axiom/photon/padre + 高成交低库存 |
| 🟠 | 样本内套现地址 | 141 | 已出现高卖出额、高已卖比例或大额转出 |
| 🟠 | 收集/回流路径 | 2 | 多个地址 transfer-out 指向同一去向 |

### 节奏识别

**三段节奏 — 初始筹码集中 → 分发源向下游拨币 → MM/机器人地址卖出并回流(进行中)**

- 第一段 初始集中: Top1 `GV6UUm...dC52` 当前仍持 58.66%，是最大单点筹码风险。
- 第二段 下游分发: `E99pfU...HUTe`、`GV6UUm...dC52` 等分发源连接多地址下游。
- 第三段 套现/回流: top traders 可见卖出 $5.73M，且出现同一回流去向，说明不是单向自然换手。

## 🧬 持有人资金关联与内幕筹码判断

> 本段已经把地址关系图消化成结论，不要求用户自己读一堆地址。完整地址明细保留在文末机器 JSON，正文只保留能影响判断的关键结论。

### 结论

- **主控集群已经成型**: `cluster_01` 覆盖 203 个样本钱包，MM/机器人命中 163 个，套现命中 122 个，当前持仓约 **75.46%**。
- **不是散户自然分布**: 该集群同时命中同 SOL 资金来源、同 token 分发源、同回流路径、相近 funding 时间/金额、bot 标签栈等特征，符合“同一操盘体系多钱包执行”的结构。
- **主库存仍在**: `GV6UUm...dC52` 当前持仓 **58.66%**，是最大单点库存风险；它的转出会比普通地址卖出更重要。
- **分发已经发生**: 样本内最大卖出成员 `3H9LVH...FSEC` 可见卖出 **$718,653**；主集群累计可见卖出 **$7.01M**。
- **回流/收集线索**: `GV6UUm...dC52` 是当前样本内最重要的收集/回流去向，连接 2 个上游。

### 这对交易决策意味着什么

| 观察点 | 解释 | 用户该怎么用 |
|---|---|---|
| 主集群持仓 75.46% | 控盘筹码仍然集中在同一关系图内 | 不要把 holder 数量当成分散度，优先看主集群是否继续转出 |
| 主集群已卖 $7.01M | 已出现边做市边兑现的行为 | 如果后续卖出继续增加，说明派发未结束 |
| Top1 库存 58.66% | 单点库存足以改变盘口 | 盯该地址是否继续向下游或池子方向移动 |
| 回流去向 `GV6UUm...dC52` | 有归集/回收库存迹象 | 盯回流后是否再分发给新下游 |

### 只保留关键集群摘要

| 集群 | AI 判断 | 钱包数 | 当前持仓 | 已卖下界 | 核心证据 |
|---|---|---:|---:|---:|---|
| `cluster_01` | 主控/MM集群 | 203 | 75.46% | $7.01M | same_sol_funder:3a8DRp...gLVj / same_token_distributor:yHCxHB...6PRe / same_token_collector:5URyNU...c19Y |
| `cluster_02` | 次级分发/回流集群 | 2 | 1.05% | $0 | same_sol_funder:GJvewf...T4YA / same_token_distributor:9KoXy9...CwhL / same_token_collector:9KoXy9...CwhL |
| `cluster_03` | 关联筹码集群 | 3 | 0.30% | $0 | same_sol_funder:9JCB8K...axJ4 / same_token_distributor:9JCB8K...axJ4 / same_funder_30m:9JCB8K...6705 |

## 📌 重点监控钱包

这里只给最少但最有用的监控对象：主库存、分发源、回流地址、最高卖出执行地址。其余地址放在 JSON，避免正文变成地址清单。

| 优先级 | 地址 | 角色 | 为什么盯 | 触发信号 |
|---|---|---|---|---|
| P0 | `GV6UUmNxz2RpKxmNAPadYKb7uQpszwqQAu3qLJxVdC52` | 主库存/单点控筹 | 当前持仓 58.66% | 继续 transfer-out 或大额卖出 |
| P0 | `E99pfUw985q5qk5Aa6ERXqJwsBjoE1igPwNfHBabHUTe` | 最大分发源 | 连接 78 个下游，MM命中 63 个 | 继续向新地址拨币 |
| P1 | `3H9LVHarjBoZ2YPEsgFbVD1zuERCGwfp4AeyHoHsFSEC` | 最高卖出执行地址 | 可见卖出 $718,653 | 继续卖出或转给新地址 |

## 机器可读 JSON 精简

```json
{
  "schema": "hertzflow_sol_meme_forensic_v1",
  "token": {
    "chain": "solana",
    "address": "9cRCn9rGT8V2imeM2BaKs13yhMEais3ruM3rPvTGpump",
    "symbol": "ANSEM",
    "name": "The Black Bull",
    "price_usd": 0.12654404,
    "market_cap_usd": 126542432.51105988,
    "liquidity_usd": 1292481.1609706206,
    "holders": 39071
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
    "top10_holder_rate": 0.6347,
    "top1_holder_rate": 0.5866357622779812,
    "bundler_wallets": 1000,
    "mm_candidate_count": 176,
    "cashout_candidate_count": 141,
    "sell_lower_bound_usd": 5726397.323576898,
    "buy_sample_usd": 7250108.235066552,
    "distribution_cluster_count": 14,
    "funding_cluster_count": 25,
    "collection_cluster_count": 2,
    "relationship_cluster_count": 4
  },
  "top_clusters": {
    "relationship": [
      {
        "id": "cluster_01",
        "score": 100,
        "wallet_count": 203,
        "mm_count": 163,
        "cashout_count": 122,
        "hold_rate": 0.7545884371135106,
        "buy_usd": 8109707.326117558,
        "sell_usd": 7010237.588519357,
        "transfer_in_amount": 764510125.557723,
        "transfer_out_amount": 832822925.550987,
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
          "3H9LVHarjBoZ2YPEsgFbVD1zuERCGwfp4AeyHoHsFSEC",
          "GV6UUmNxz2RpKxmNAPadYKb7uQpszwqQAu3qLJxVdC52",
          "5URyNUmhcuWdZiiQrtNdFrSbQPfq72UV2gqQasr9c19Y",
          "2S8E25nAcqvvMYEWZHBQk22GzevwvmsVNAs6Gw5tRX7d",
          "3CPHk5b7SRvAsTsocehAu1bA5YKMXJYMr3qc2SuMFkWY",
          "4aArEDkqkPBwFiSCShd6GJ8dTFHzZboGf3GD7qwxxTu3",
          "6btcCbEdYnCUyuzV3JEMDpw9YbbF1tPFzNSN2Sfwg5eT",
          "CxCTVjvgK3bWcgavMKo8PushR8ycw1atrWiSTruZrdtT"
        ]
      },
      {
        "id": "cluster_02",
        "score": 31,
        "wallet_count": 2,
        "mm_count": 0,
        "cashout_count": 1,
        "hold_rate": 0.010500139513659242,
        "buy_usd": 2029.92782975274,
        "sell_usd": 0.0,
        "transfer_in_amount": 10541814.872978,
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
        "score": 24,
        "wallet_count": 3,
        "mm_count": 0,
        "cashout_count": 0,
        "hold_rate": 0.003000035170877776,
        "buy_usd": 0.0,
        "sell_usd": 0.0,
        "transfer_in_amount": 2999997.061431,
        "transfer_out_amount": 0.0,
        "features": [
          "same_sol_funder:9JCB8K...axJ4",
          "same_token_distributor:9JCB8K...axJ4",
          "same_funder_30m:9JCB8K...6705",
          "same_funder_amount:9JCB8K...:0.1",
          "same_created_1h:483352",
          "same_entry_15m:1980520",
          "same_funder_30m:9JCB8K...6465",
          "same_funder_amount:9JCB8K..._0.1"
        ],
        "representatives": [
          "2kRgLqiRUJFiCs46GDJbaeH63T6kR3fS1T6d3j6NkBcS",
          "5N2Aeq556NdR8Gn93UZmGccJksXbfJ3J96M5TJ7PCFZi",
          "HpNtDG2qRPcvcXMszdUyBvdu3GEEZGh1kLNfXbdB933B"
        ]
      },
      {
        "id": "cluster_04",
        "score": 24,
        "wallet_count": 2,
        "mm_count": 1,
        "cashout_count": 2,
        "hold_rate": 0.0007947658490195801,
        "buy_usd": 247473.61162693985,
        "sell_usd": 163137.935734911,
        "transfer_in_amount": 0.0,
        "transfer_out_amount": 4647.090392,
        "features": [
          "same_sol_funder:GHrTm6...RdK5",
          "same_funder_30m:GHrTm6...7296",
          "same_funder_amount:GHrTm6..._0.1",
          "same_created_1h:483648",
          "same_entry_15m:1980773",
          "same_sol_funder:BeyjG7...gxto",
          "same_token_collector:3FenmB...8gFa",
          "same_funder_30m:BeyjG7...7296"
        ],
        "representatives": [
          "5V676H2Th83MycbJQ1JuL3f8GCCf6WDDVY2qY8Tj9zFb",
          "5mnuSGWc8vzH7Xyj54ebNGhouJetvigzh2wE9UCE6btz"
        ]
      }
    ],
    "distribution": [
      {
        "source": "E99pfUw985q5qk5Aa6ERXqJwsBjoE1igPwNfHBabHUTe",
        "wallet_count": 78,
        "mm_count": 63,
        "hold_rate": 0.09840472971289455,
        "buy_usd": 5686423.6649934165,
        "sell_usd": 3527504.53062857,
        "representatives": [
          "3CPHk5b7SRvAsTsocehAu1bA5YKMXJYMr3qc2SuMFkWY",
          "9H9HU7RsFnovQ9jPXo4Er9EPCdNQaHEtey8f6CpAC4AZ",
          "8e9bkF9q2cZqRpLqGNgimr19mhHarW7p1yvSreTC6qg6",
          "F5hkYsi8JxjyA2JHN5CA7MbnnhWubkXB2ZQB7Gkaxqs6",
          "3inTyfqCpLwa4U812GmB3FPcGz6iFWxHbaNpw5dPrTg2"
        ]
      },
      {
        "source": "GV6UUmNxz2RpKxmNAPadYKb7uQpszwqQAu3qLJxVdC52",
        "wallet_count": 10,
        "mm_count": 7,
        "hold_rate": 0.014754943143059746,
        "buy_usd": 118276.4964440419,
        "sell_usd": 1117514.9130208986,
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
        "wallet_count": 5,
        "mm_count": 3,
        "hold_rate": 0.015268226301841712,
        "buy_usd": 587945.1405060393,
        "sell_usd": 821098.1840189284,
        "representatives": [
          "3H9LVHarjBoZ2YPEsgFbVD1zuERCGwfp4AeyHoHsFSEC",
          "HCgo8gvk99Wk13XWbbAoyxyEx2DgzidzVDma4ny32uYC",
          "6HcrxubcevZQs1fcPTVnywzw7N2XWqsyAPxqnmg78UMg",
          "GkdYWRjFzZW3oxbRaPJ43C5385E4GtfgW3vwfK2ZAtac",
          "B2f9t2AQKHE2jK24iCxC95zmgvcuZxkkK9HUjvd3k418"
        ]
      },
      {
        "source": "B4Z8JSSVCNWW5gkYgxrrTZKwVfnqMCxYZS9cPQLeJdpF",
        "wallet_count": 3,
        "mm_count": 3,
        "hold_rate": 0.017210083475304387,
        "buy_usd": 140550.39895216134,
        "sell_usd": 385775.93926993734,
        "representatives": [
          "CLM6E4zpTviEC77nWKogpVLQoXx9tgoQCYJ8NibxKg1Q",
          "CxCTVjvgK3bWcgavMKo8PushR8ycw1atrWiSTruZrdtT",
          "ACTbvbNm5qTLuofNRPxFPMtHAAtdH1CtzhCZatYHy831"
        ]
      },
      {
        "source": "6jmUvtpjs94bvy4XZ75Yrmj6HMpbBPtk3qtBHDzM6xz1",
        "wallet_count": 3,
        "mm_count": 3,
        "hold_rate": 7.086192828507501e-05,
        "buy_usd": 20386.403898319,
        "sell_usd": 14275.358383226801,
        "representatives": [
          "6msXZdBsgkyMi5CsLxb2wuRMHPzW3egEpg7W2TeDVmGW",
          "CEq8qbEpk2sWr7Pi7T8kXScWUaM6NmCJCCdni1uortz5",
          "DrnuP46qcf7b7utTY9Esm46SwkTFhYu4TrtRGTyvkE67"
        ]
      }
    ],
    "funding": [
      {
        "source": "AxiomRXZAq1Jgjj9pHmNqVP7Lhu67wLXZJZbaK87TTSk",
        "wallet_count": 20,
        "mm_count": 20,
        "hold_rate": 0.006150250406033907,
        "buy_usd": 429083.94345956604,
        "sell_usd": 272063.29379079776,
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
        "wallet_count": 14,
        "mm_count": 10,
        "hold_rate": 0.008970716234984332,
        "buy_usd": 272125.34262694087,
        "sell_usd": 253811.3844493318,
        "representatives": [
          "Cqku64qzS5h8i2BroQh2yTyhdUTLYPvMFzo12apLsUpw",
          "B2f9t2AQKHE2jK24iCxC95zmgvcuZxkkK9HUjvd3k418",
          "GmCqxJx2QPxKfhyiLyk5CdV3rQtwuXKnCoTq5RoFBCoD",
          "JBM3QhZgNgUZZzRdbHVrQULLtb7BphmJdR4JPu6mE7kG",
          "9JCB8Kr71PVnJ2XekxRUfozo7QVYb4G2dJZabbo5axJ4"
        ]
      },
      {
        "source": "CZ5H8Fiuf6HCLQXeNuZio9yU63d2un6Nu5PnrD1YwnR8",
        "wallet_count": 7,
        "mm_count": 6,
        "hold_rate": 0.009868605754994906,
        "buy_usd": 332256.3119943626,
        "sell_usd": 394152.44014238776,
        "representatives": [
          "GA1G2wmJcRzPipLMdjMgEcyRDgPRuBSaNNQWr77T9j4e",
          "6T8Var5aHQd2m1XBFC9ovHJvkex94wNHd5NQwpPGWW6N",
          "78thMY8yfYzXGRhSArPMr7j8Rsh5QEPZviHVPfEfoMDM",
          "4npDgDGmDCRFUm8ZzWEG6mzpVYSj1yTLdJDpoGnanhFG",
          "DytQyNJjG1xVtvTKkKbPcU9UQMMgf4WAbigu332SzE1P"
        ]
      },
      {
        "source": "2snHHreXbpJ7UwZxPe37gnUNf7Wx7wv6UKDSR2JckKuS",
        "wallet_count": 5,
        "mm_count": 5,
        "hold_rate": 0.012677134804587422,
        "buy_usd": 209564.6672131873,
        "sell_usd": 129934.12751694194,
        "representatives": [
          "CLM6E4zpTviEC77nWKogpVLQoXx9tgoQCYJ8NibxKg1Q",
          "E9cnYgPfwbDmd5qXs4r3h3g9gWERRrz2cgJ9AbPoiucR",
          "5w5QUq1LWwd7KzzGyJEWuDHg8kymMX4j1VQ9CpGCg9E8",
          "65paNEG8m7mCVoASVF2KbRdU21aKXdASSB9G3NjCSQuE",
          "Cas6a9t6wTmV9a1b6FRYCEBX6ChQvtY1Wmfj9FvgED3K"
        ]
      },
      {
        "source": "iGdFcQoyR2MwbXMHQskhmNsqddZ6rinsipHc4TNSdwu",
        "wallet_count": 5,
        "mm_count": 5,
        "hold_rate": 0.00487987300794582,
        "buy_usd": 410479.5992388908,
        "sell_usd": 69006.82487655662,
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
        "target": "GV6UUmNxz2RpKxmNAPadYKb7uQpszwqQAu3qLJxVdC52",
        "wallet_count": 2,
        "mm_count": 2,
        "hold_rate": 0.0008960776864538511,
        "buy_usd": 188435.80911618558,
        "sell_usd": 311861.61360913387,
        "representatives": [
          "4aArEDkqkPBwFiSCShd6GJ8dTFHzZboGf3GD7qwxxTu3",
          "yHCxHBEaJW5tbndqC8JciSThr7U1cqLpdcsvHcx6PRe"
        ]
      },
      {
        "target": "8psNvWTrdNTiVRNzAgsou9kETXNJm2SXZyaKuJraVRtf",
        "wallet_count": 2,
        "mm_count": 1,
        "hold_rate": 0.0032639708373435466,
        "buy_usd": 507787.57943636534,
        "sell_usd": 598092.0627312406,
        "representatives": [
          "2S8E25nAcqvvMYEWZHBQk22GzevwvmsVNAs6Gw5tRX7d",
          "8e9bkF9q2cZqRpLqGNgimr19mhHarW7p1yvSreTC6qg6"
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
      "reason": "连接 78 个下游，MM命中 63 个",
      "trigger": "继续向新地址拨币"
    },
    {
      "priority": "P1",
      "address": "3H9LVHarjBoZ2YPEsgFbVD1zuERCGwfp4AeyHoHsFSEC",
      "role": "最高卖出执行地址",
      "reason": "可见卖出 $718,653",
      "trigger": "继续卖出或转给新地址"
    }
  ]
}
```


## 方法边界

- 这份报告已经把 GMGN 的 holder/trader/tag 样本做了聚类，但还不是完整 Solana transfer graph。
- 当前“MM/操盘集群”属于强行为判断：同源资金、同一分发来源、同一收集去向、bot/bundler 标签、高成交低库存等信号叠加。
- 如果要做到 Binance Alpha EVM 那种完整取证，需要继续接 Helius/Shyft/Vybe，把 SPL transfer 和 Jupiter/Raydium/Meteora inner instructions 全量展开。
