# TAC (TAC) — 链上决策简报


## 🎯 一屏结论

> 本段 deterministic 由 link 上 detector 输出推导, 不构成买卖建议. 详细证据在下方各段.

| 维度 | 结论 | 关键证据 |
|---|---|---|
| **当前阶段** | 🔴 派发进行中 / 拉盘中出货 | 近 72h 100 笔大额异动; 已确认变现 $3,456,812 |
| **筹码结构** | 🟢 分散 | 庄家/项目方可控筹码 0.0% / 中转·流动性池(CEX+DEX) 0.0% / 可验证非庄家方抛压 100.0% |
| **内幕/庄家现货套现情况** | 🟡 少量套现 | 已确认内幕变现 4.1% 流通 + 交易所提币分发净 0.0% 流通 |
| **成交质量** | 🔴 24h 成交不可信 — 对敲机器人主导 | 497,257 笔链上撮合, 单机器人占 13.2% |
| **供应风险** | 🟠 存在供应源 — 量级有限 | 9 个铸币权限, 累计 3.7% 总供应 |
| **盘口阶段** | 🟠 中市值 + 薄承接 / 拉升中 | mcap $266M; 5% 深度 $8,112; LP/mcap 0.004; vol/LP 13.1×; 24h +165.5% |
| **监控重点** | 盯继续派发路径 | 近 72h 异动地址、铸币权限合约、高频清仓钱包 |

**一句话**: 派发进行中 / 拉盘中出货 + 分散 + 成交被 wash 放大.

## 🎯 速读摘要 (中文)

> 本段供快速 散户 阅读 / AI 二次解读. 详细 链上侦测 在下方各段, 含英文术语. 本段全部基于链上数据派生, 不含买卖建议.

- **项目**: TAC (TAC), 主合约 [`0x1219c409…`](https://bscscan.com/address/0x1219c409fabe2c27bd0d1a565daeed9bd9f271de)
- **上线情况**: 币安 Alpha S1 (仅 Alpha) · 主战场 BSC 链

- **已确认内幕链上变现**: **188,856,099 tokens (占流通 4.05%)** ≈ **$3,456,812 USD** — 内幕钱包**自己**已通过 (a) 转入中心化交易所充值地址 + (b) 自己直接链上撮合 完成的真实变现下界; 实际真实出货大概率高于此数 (详见 📊 真实派发段)
- **TGE 时分发的 token 已被卖出**: **5,486,054 tokens** ≈ **$111,062 USD** (约占总供应 0.05%) — 通过 跨链桥 / 铸币权限合约自卖 (1 个合约) 通道回流市场

- **历史高频庄家已浮现**: 93 个钱包 365 天内累计**过账** (token 进出流量, 不等于卖出量, 含对敲双计) **6,888,040,830 tokens** 后余额清空 — 已离场走人

- **本报告完整度提示**: 仅含链上可验证 的 钱包 → DEX/CEX 资金流向. 链下行为 (CEX 提币后用别的方式分发 / OTC 转账 / 跨链桥未走 surf 索引等) 无法链上侦测, 实际真实出货量可能高于本报告数字. 详见下方 🟡 完整度提示.

- **如何使用本报告**: 跟下方 **重点监控钱包** 段配合看, 把核心钱包加进 Binance Wallet / OKX 监控 (monitoring_paste.json 可一键导入). 进/出场决策结合自己风险承受度判断.


> ⚠️ **本报告读前必看 — 链上侦测限制 / 数据提醒**
>
> - 🚨 **24 小时成交额 / 链上撮合量被对敲机器人主导**: 200 个对手地址 / 497,257 笔链上撮合, 单一对敲机器人最多 65,795 笔对敲 (单一对敲机器人占比 13.2%). **不要用 24 小时成交额判断真实承接量**, 看下方"承接上限 (5% 深度)". 详细 → 📊 真实派发段.
_工具版本 1.2.6 · 主链 BSC · Alpha 上线 2025-07-15_

_总供应 10,258,557,461 · 流通 4,657,385,389 (45.4%) · 类型 VC_LIKELY_
_等级 S1 · S1 2025-07-15_

## 💹 代币行情 (实时)

| 项目 | 取值 |
|---|---|
| **项目名称** | **TAC** (TAC) |
| Ticker | `TAC` |
| 主战场链 | BSC |
| 上线情况 | S1 (仅 Alpha) · Alpha 上线 2025-07-15 |
| **当前价** | **$0.05713** (🟢 +165.26% 24H) |
| **全网 24H 成交 (CEX+DEX)** | **$21,346,044** |
| 当前 LP (DEX 主池) | $1,191,506 |
| 市值 (mcap / FDV) | $266,053,223 / $572,968,428 |
| 数据来源 | surf+Alpha API (实时) · 持币 2,615 个 · 24H 65,225 笔 |

## 📋 决策摘要

| 项目 | 取值 |
|---|---|
| **🎯 风险评分** | **🟥🟥🟥🟥🟥🟥🟥🟥🟥⬜ (9/10)** |
| **链上状态标签** | **近期派发** — 近 72h 链上活动 — 100 笔大额转移 |
| 主战场链 | binance-smart-chain |
| **进场上限 (LP 5% 深度)** | **$8,111** |
| 短期催化 | 无 |
| 必须自行 交叉核对 的盲区 | 无 |

> 🎯 **5 档链上状态标签含义** (渲染端 确定性 推导, 仅描述链上侦测 状态, 非交易建议):
> - **无显著触发** — 无显著链上侦测触发信号 (风险 0-2)
> - **观察中** — 部分异动但未触发主信号 (风险 2-5)
> - **派完离场** — 历史庄家已派完, 链上历史抛压已释放 (风险 4-7)
> - **潜伏内幕未派** — 潜伏内幕钱包未分发, 时点不可预测 (风险 6-9)
> - **近期派发** — 近 72h 大额链上活动 (风险 7-10)

> TAC 当前不适合把上涨当成干净突破处理：链上状态已经指向拉盘中出货，近端大额异动很多，已确认内幕变现金额达到百万美元级，同时成交质量被对敲放大。持仓者优先降风险，观望者等派发路径和异常转账收敛后再评估。



## 🎯 链上状态: 近期派发 (风险评分 9/10)

**近 72h 链上活动 — 100 笔大额转移**


| 决策锚点 | 数值 | 状态 |
|---|---|---|
| Alpha 5% 撤单上限 | $8,111 | 🟡 中等 |
| DEX 主池 USD 流动性 | — | 🔴 |
| 池子代币 24h 净进出 (throughput, 非 LP 增减) | — | 🟢 |


## 🧠 当前链上行为画像

> 这一段把 10 个 检测器 输出翻译成"庄家可能在干嘛"的 4 类行为状态. 多标签 本设计如此 — 同一 token 可同时命中多类 (如 A1 蓄筹 + B1 对敲 做量 + C3 近期活动). 顺序: 严重度 (🔴 STRONG / 🟠 MEDIUM / 🟡 WEAK) → 类别 → 标签编号. 仅描述链上事实, 非交易建议.

| 严重度 | 标签 | 类别 | 触发指标 | 链上事实 |
|:-:|---|---|---|---|
| 🔴 **STRONG** | `B1` 对敲成交放大 (24h vol 不可信) | B 成交制造 | `wash_swap_count=497257, wash_top_bot_share=0.132, wash_n_dex_addrs=200` | 24 小时内 497,257 笔链上撮合, 200 个链上交易地址, 单一对敲机器人占 13.2% — 24 小时成交额含大量对敲, 不等同真实成交承接量 |
| 🔴 **STRONG** | `C1` 链上确认流出 (CEX 充值 + DEX swap) | C 出货行为 | `net_sellout_usd=3456812.0, sell_pct_circ=4.055` | 链上确认流出 $3,456,812 (占流通 4.05%) — 中心化交易所充值 + 链上撮合 路径已观察到内幕真实变现 |
| 🔴 **STRONG** | `C2` 历史高频庄家清仓 | C 出货行为 | `ht_operator_count=100, ht_throughput_pct_supply=72.04` | 100 个高频庄家钱包 (累计**过账** 占总供应 72%, 过账 = token 进出流量, 不等于卖出量), 历史已离场, 余额接近 0 |
| 🔴 **STRONG** | `C3` 近 72 小时异常链上活动 | C 出货行为 | `anomaly_72h_count=100, truncated=True` | 近 72 小时 100 笔大额异常转移 (笔数, 不是 token 量) (检测器满量程截断), 链上行为活跃 |
| 🟠 **MEDIUM** | `A3` Mint / 跨链桥 / 挖矿 供应源 | A 筹码准备 | `mint_authorities=9, mint_pct_supply_max=0.51, mint_pct_supply_sum=3.69` | 9 个铸币权限合约存在 (累计铸造占流通供应 3.7%), 持续供应源, 后续 铸造 → 出货 可能 |
| 🟠 **MEDIUM** | `B2` 假深度 (LP/mcap 失配 或 vol/LP 偏高) | B 成交制造 | `vol_lp_ratio=13.07, lp_mcap_ratio=0.0045, lp_usd=1191505.726515956` | 成交量/流动性 比 = 13.1× / 流动性/市值 比 = 0.0045 — 表面流动性偏低, 单笔成交对价格冲击大 |

> **行为画像不等于 判定**: 上方 🎯 链上状态 标签是综合 5 档 (无显著触发 / 观察中 / 派完离场 / 潜伏内幕未派 / 近期派发), 这里的行为画像是细分的 10 类 链上侦测信号. 一个 token 可以是 "近期派发" + 同时命中 A1+A2+A3+B1+C2+C3 等多标签.


## 🔴 真实派发 (内幕 确认卖出下界)

### 🎯 拉盘对手盘验证

> **⚡ 速读**: 流通 126.6M tokens · **非庄家方抛压 100.0%** (126,584,228 tokens = 前 100 大持币人内可验证 100.0%) · 庄家弹药 0.0% (⚠️ Alpha API 报流通 4657M, 链上可砸盘 127M = 0.03x, Alpha 高估 (含 mint authority / vesting 锁仓)) · 中转·流动性池 (CEX 充值 + DEX 池, 庄家加池 vs 散户交易不可分) 0.0% (0 个交易所/DEX 池) · 内幕已确认变现 $3,456,812 (占流通 4.1%).

> ⚠️ **三桶 sanity check 触发** — 以下桶 ≈ 0%, 主动排查:
> - **庄家弹药 0%**: 罕见 — Alpha 类 token 通常有项目方控. 排查: (a) `_master_cluster_addrs` 是否空 (应 ≥ 50)? (b) m6 / mint_authority / cex_fanout / ht_dumpers detector 是否 run? (c) 检查 funding_attribution segments
> - **中转·流动性池 0%**: BSC 主流 Alpha token 通常都进 Binance/Gate/Bitget. 排查: (a) surf top_holders cex category 是否空? (b) cex_hot_wallet labels 是否完整 (Arkham)? (c) cex_fanout hubs 检测到的 CEX source addresses 应进 cex_pool
> 庄家想 pump 时, **可能砸盘的对手 = 现持有筹码里不属于庄家的部分**. 这部分越小, 庄家越敢拉 (拉了不怕被砸); 越大越有顾忌.

| 筹码桶 | 代币数 | 占当前流通 | 解读 |
|---|---:|---:|---|
| 🟣 **庄家 / 项目方可控筹码** | **0** | **0.0%** | **分散** — 项目方足迹不明显 |
| 🔥 **可验证非庄家方抛压** | **126,584,228** | **100.0%** | **外部抛压较重** (含散户大户 + 协议合约 + 跨链桥中转) |
| 🟦 **中转·流动性池 (CEX + DEX, 中性·不可分)** | **0** | **0.0%** | 0 个交易所热/冷/充值钱包. 链上**无法区分**散户充值聚合 vs 项目方托管储备. 拉盘时可能从两边都流出 |

### 关键判断

**项目方可控筹码 < 50%** — 控盘不强, 看外部对手盘 + CEX 池流向决定盘面.
**raw 桶加总 310% (展开看明细)** — 桶间钱包级重叠, 是 debug caveat, 不影响速读 0.0% 庄家弹药结论.

<details>
<summary>🔍 展开: 庄家弹药 11 子桶明细 (含 raw 加总 + 重叠说明)</summary>

| 子桶 | 代币数 | 占流通 | 说明 |
|---|---:|---:|---|
| ①a 公开锁仓 / 国库 / 空投合约 m6 谱系外 | 0 | 0.0% | Sablier / Hedgey / 自定义锁仓. 有公开释放时间表, **拉盘时不会立刻砸**. 减未流通储备 5,601,172,072 后的下界 |
| ①b 多签可机动 m6 谱系外 | 0 | 0.0% | Gnosis Safe Proxy 等. 项目方一签今天就能转 |
| ② m6 谱系流通中部分 | 0 | 0.0% | m6 谱系总持仓 69,708,267 减锁仓 0. 含纯内幕 (36,727,957) |
| ⚠️ ③ 交易所提币分发 (净控筹不可算) | — | — | gross 流入, phase2 SQL 截断, 净 fanout 算不出.  |
| ④ DEX 池代币侧持仓 | 10,412,999 | 8.2% | DEX 池 99% 是项目方 / 做市商提供 |
| ⑤ 其他检测器命中 | 4,089,698 | 3.2% | 39 个钱包 — 资金流操盘者 / 跨币种鲸鱼 / 高频清仓庄家 |
| ⑥ 铸币合约未释放储备 | 326,627,927 | 258.0% | 矿币 / 跨链桥 铸币合约当前余额, 项目方控未释放供应 |
| ⑥' 已铸给庄家集群 (净持仓) | 51,432,073 | 40.6% | 累计铸币 - 合约储备 - 已变现 = 仍在伪矿币集群 |
| 📌 未流通项目方控制储备 | 5,601,172,072 | _占总供应 54.6%_ | **不算流通分母 — 但项目方控**. 锁仓 / 铸币节奏释放进流通后增加抛压 |
| ━━━━━ | ━━━━━ | ━━━━━ | ━━━━━ |
| 庄家弹药 raw 加总 | 392,562,697 | 310.1% | ⚠️ > 100% = 子桶钱包级重叠 (m6 内多签同时进 ①b + ②). 速读 0.0% 是钱包级反算严格去重 |

**说明**:
- 速读"庄家弹药"是**钱包级反算**: 遍历前 100, 命中庄家集合的去重 sum. 跟 raw 加总不同 — raw 按桶上界 (含重叠), 速读严格去重.
- 速读"非庄家方抛压"含**散户大户 + 协议合约 (Wormhole / veVELVET 等)**, 不全是真散户. 是上界.
- ①a vesting / ⑥ 铸币储备 → 拉盘时**不会立刻砸**, 中期才进流通.
- ①b 多签 / ⑥' cluster → **今天可转**, 跟"锁仓"性质不同.
- 算法版本: 庄家弹药 / 非庄家方抛压 反向算法 v0.8.4.8.

</details>

#### 🔍 可验证非庄家方抛压钱包明细 (反向算)

> 前 100 大持币人里**既不在庄家集合也不在中转·流动性池**的钱包. 庄家集合: m6 谱系 + 多签 / 公开锁仓 / 国库 / 空投合约 + 启发式抓的 + 检测器命中. **所有交易所钱包 + DEX 流动性池整段刨除** (归中性"中转·流动性池": 庄家加池/散户充值 vs 散户交易, 不可分). 可验证非庄家方抛压主要含真散户大户 + 跨链桥协议合约 + DeFi 协议合约.

| 序号 | 钱包 | 当前持仓 | % 流通 | 类型 | Arkham 标 |
|---:|---|---:|---:|---|---|
| 1 | [`0x6cd06aaf0650`](https://bscscan.com/address/0x6cd06aaf06506bc3ff382d83023354e2b80eed22) | 88,421,133 | 69.85% | 未分类 | — |
| 2 | [`0xc38de6135c9d`](https://bscscan.com/address/0xc38de6135c9d18ea378558a7e6c0c811dd4cb9c0) | 38,163,095 | 30.15% | 未分类 | — |
| ━━━━━━━━━━━━━━━━━ | ━━━━━━━━━━━━━━━━━ | ━━━━━━━━━ | ━━━━━━━ | ━━━━━━━━━ | ━━━━━━━━━ |
| **合计可验证非庄家方抛压 (前 100 大持币人内)** | 2 个钱包 | **126,584,228** | **100.0%** | — | — |

> ⚠️ **非庄家方抛压性质判断**: 主要含真散户大户 + Wormhole / veVELVET 等协议合约 (用户存的) + 跨链桥中转. 大额裸地址 (没 Arkham 标 + > 1% 流通) 是项目方化名 vs 真散户大户 嫌疑 — 到下方 monitoring_paste 手动核对钱包活动.

---

| 项目 | 取值 |
|---|---|
| 追踪钱包数 (m6 谱系全集) | **14** (18 标准内幕 + **1 挖矿机制取得** + **9 铸币权限合约**) |
| **纯内幕当前持有 (判定 参考的真潜伏抛压)** | **3.5420% 总供应** (363,355,886 tokens, **不含** vesting / 多签 / treasury / CEX 托管 / DEX 路由; 含 挖矿机制取得 操作员钱包当前 余额; 含 铸币权限合约 合约当前 余额) — ⛏️ 挖矿机制取得 仍 sit 2 tokens 待出货 · 🌉 铸币权限合约 仍 sit 326,627,927 tokens (可随时继续 mint→出货) |
| 内幕树当前持有 (含锁仓, 守恒锚) | 3.8635% 总供应 (396,336,196 tokens, 矿币模式下树 = 标准 内幕 + 挖矿机制取得 集合 + 铸币权限合约 合约 (无 vesting/lockup 分离)) |
| (a) 确认卖出 — CEX 充值 | 188,856,099 → Binance Wallet, Binance Deposit, Coinbase |
> _💡 注: 链下 CEX 提币 (从 CEX → 钱包) 不在 (a) 行 — (a) 只看链上 钱包 → CEX deposit. 项目方先从 CEX 提币再砸盘 (例如 Eleve 帖子描述的 H 案例), 提币本身是链下行为, 无法链上侦测; 提出后的链上转账如果走 DEX 路由 出货, 已在 (b) 行 captured._
| (b) 确认卖出 — DEX swap (本钱包) | 5,486,054 (18 笔; 🌉 铸币权限合约 自卖 5,486,054 tokens / 18 笔 ≈ **$111,062 USD** 全部 via DEX 路由) |
| **确认毛卖出, a+b** | **≥ 194,342,153 = 流通 4.1%**, USD ≈ $3,567,874 |
| **确认净卖出** | **$3,456,812** — 内幕**自卖 DEX TWAP** $0.0183 (拒 对敲 报价污染) |



> **📅 时间窗拆分** — 配合短期事件 (Twitter 突发出货报警 / 大额异动) 对账; 数字关系 **近 7 天 ≤ 近 30 天 ≤ 累计**.

| 时间窗 | 确认毛卖出 (tokens) | 占流通 % | 确认净卖出 (USD) | DEX 真实成交 (USD) | CEX 路由 (tokens) |
|---|---:|---:|---:|---:|---:|
| **近 7 天** | 2,564,061 | 0.06% | **$46,932** | — | 2,564,061 |
| 近 30 天 | 4,125,160 | 0.09% | $75,507 | — | 4,125,160 |
| 累计 (~364 天) | 188,856,099 | 4.05% | $3,456,812 | — | 188,856,099 |

> 解读: **近 7 天**显示当前热度 (跟 EmberCN-style 突发 alarm 直接对账); **近 30 天**显示当月节奏; **累计** = surf 查询窗口内全部. 单日突发可能没体现进 7d 平均, 但已在 累计里. CEX 路由 = 进了交易所充值/热钱包的 token 数 (sell off-chain 在 CEX 侧, 非 wash 价).


> 🕵️ **隐藏庄家弹药已观察到变现动作**: 跟踪的 **1 个隐藏弹药钱包** (启发式抓出 / 伪矿币铸币集群) 已通过 (a) 转入交易所充值地址 **489,391 tokens** (1 个交易所: OKX Deposit) + (b) 自己链上撮合 **0 tokens** (0 笔), 合计 **489,391 tokens** = 流通 0.01%, USD ≈ **$8,958** (粗估: 用 m6 内幕自卖 DEX TWAP, 跨群体口径不一定吻合). **这些钱包在算法 5 桶之外**, 可能补充在"确认毛卖出"之上看真实派发量; 但**需扣除跟 m6 内幕 / 挖矿机制取得集合可能存在的钱包重叠** (v0.8.4 backlog 加 disjoint dedupe). 时间窗: 从 2025-07-15 起.> ⚠️ **该币的链上出货被对敲机器人主导**: 200 个对手地址共 497,257 笔链上撮合, 单一对敲机器人最多 65,795 笔对敲. 大量内幕把币转给中继 / 机器人再出 (这部分**认不出归属**, 不计入上面的确认下界 — 所以真实出货大概率比下界高). 巨量对敲 = 出货同时拉高表面活跃度诱多.


<a id="section-recent-anomaly"></a>
## 📊 风险信号聚合 (检测器 + 节奏)

### 检测器汇总

| emoji | 类别 | 数量 | 解读 |
|---|---|---|---|
| 🔴 | 上线前内幕分发 | 8 | 上线前分发路径清楚，项目方部署钱包向多个接收方分配筹码，后续接收方行为需要持续盯住。 |
| 🔴 | 已分完内幕钱包 | 6 | 近端异常事件数量很高，说明当前仍有活跃的大额转移，不适合把价格上涨理解成筹码沉淀完成。 |
| 🟠 | 潜伏钱包 (未分发) | 1 | 真实派发检测已经确认有内幕变现，且 CEX 路径出现 Binance、Coinbase 等标签，说明部分筹码已经进入可兑现通道。 |
| 🔴 | 近 72h 异常大单 (truncated ≥100) | 100 | 成交质量检测提示 wash 放大，24h 成交量不能直接当成真实承接，买入容量应按更保守口径处理。 |

### 节奏识别

**上线前分发、下游扩散、近端异常同时存在**

- 第一波 上线前 OTC 预分发 (2025-07-11 ~ 2025-07-14 UTC): 第一波是项目方上线前把筹码交给接收方，奠定后续分发路径；这不是单纯转账噪音，而是后面出货链路的上游。
- 第二波 分发主体向下游分发 (2025-07-15 ~ 2026-04-30 UTC): 第二波是分发主体继续向下游扩散，多个地址把筹码拆分给更多接收方，说明筹码已经进入可流通和可变现阶段。
- 第三波 近 72h 异常活动 (2026-06-29 ~ 2026-06-29 UTC): 第三波发生在最新交易日附近，异常大额转账数量高，和价格急拉同时出现，交易上应按拉升中派发处理。


<details>
<summary>📂 <strong>📊 完整异动事件列表 (数据明细, 按分发轮次, UTC 时间)</strong> — 共 3 波分发, 合计 23 笔事件 (click 展开看完整时间表 + 钱包流向)</summary>

### 🟠 第一波 上线前 OTC 预分发 (2025-07-11 ~ 2025-07-14 UTC, **已完成**)

| 事件编号 | UTC | 距今 | 来源 → 目标 | 性质 | 金额 |
|---|---|---|---|---|---|
| `evt_003` | 2025-07-14 12:32 | 记录时间见本行 UTC 时间 | 项目方 `0x64f6902c…` → `0x93deb693…` | 项目方上线前分发动作，属于后续内幕接收方追踪的起点。 | 200,000,000 tokens |
| `evt_002` | 2025-07-11 13:23 | 记录时间见本行 UTC 时间 | 项目方 `0x64f6902c…` → `0xfe5b95b0…` | 项目方上线前分发动作，属于后续内幕接收方追踪的起点。 | 1 tokens |

### 🔴 第二波 分发主体向下游分发 (2025-07-15 ~ 2026-04-30 UTC, **该波事件显示筹码仍在向下游移动，和当前价格拉升叠加后，对持仓更偏风险信号。**)

| 事件编号 | UTC | 距今 | 来源 → 目标 | 性质 | 金额 |
|---|---|---|---|---|---|
| `evt_131` | 2025-07-15 09:57 | 记录时间见本行 UTC 时间 | `0xd2cd331e…` → 30 个接收地址 | 分发主体继续向下游拆分筹码，后续若进入 CEX 或 DEX 路由就是实际卖压。 | 合计 6,223,645,582 tokens |
| `evt_068` | 2025-07-15 09:58 | 记录时间见本行 UTC 时间 | `0xb300000b…` → 30 个接收地址 | 分发主体继续向下游拆分筹码，后续若进入 CEX 或 DEX 路由就是实际卖压。 | 合计 1,748,594,696 tokens |
| `evt_066` | 2025-07-15 10:00 | 记录时间见本行 UTC 时间 | `0x6aba0315…` → 2 个接收地址 | 分发主体继续向下游拆分筹码，后续若进入 CEX 或 DEX 路由就是实际卖压。 | 合计 1,559,116,612 tokens |
| `evt_032` | 2025-07-15 10:00 | 记录时间见本行 UTC 时间 | `0x73d8bd54…` → 30 个接收地址 | 分发主体继续向下游拆分筹码，后续若进入 CEX 或 DEX 路由就是实际卖压。 | 合计 944,945,361 tokens |
| `evt_106` | 2025-07-15 09:58 | 记录时间见本行 UTC 时间 | `0xca852767…` → 4 个接收地址 | 分发主体继续向下游拆分筹码，后续若进入 CEX 或 DEX 路由就是实际卖压。 | 合计 681,383,561 tokens |
| `evt_110` | 2025-07-15 09:58 | 记录时间见本行 UTC 时间 | `0xde9e4fe3…` → 19 个接收地址 | 分发主体继续向下游拆分筹码，后续若进入 CEX 或 DEX 路由就是实际卖压。 | 合计 434,633,164 tokens |
| `evt_005` | 2025-07-15 09:22 | 记录时间见本行 UTC 时间 | `0x93deb693…` → 27 个接收地址 | 分发主体继续向下游拆分筹码，后续若进入 CEX 或 DEX 路由就是实际卖压。 | 合计 210,000,000 tokens |
| `evt_129` | 2026-01-30 08:07 | 记录时间见本行 UTC 时间 | `0x0501f595…` → 2 个接收地址 | 分发主体继续向下游拆分筹码，后续若进入 CEX 或 DEX 路由就是实际卖压。 | 合计 165,212,987 tokens |
| `evt_098` | 2026-02-23 03:00 | 记录时间见本行 UTC 时间 | `0xbd97306a…` → 5 个接收地址 | 分发主体继续向下游拆分筹码，后续若进入 CEX 或 DEX 路由就是实际卖压。 | 合计 40,545,446 tokens |
| `evt_161` | 2026-02-23 13:16 | 记录时间见本行 UTC 时间 | `0x653dd767…` → 1 个接收地址 | 分发主体继续向下游拆分筹码，后续若进入 CEX 或 DEX 路由就是实际卖压。 | 合计 15,523,470 tokens |
| `evt_062` | 2026-04-30 09:50 | 记录时间见本行 UTC 时间 | `0xb5893a55…` → 3 个接收地址 | 分发主体继续向下游拆分筹码，后续若进入 CEX 或 DEX 路由就是实际卖压。 | 合计 13,658,710 tokens |
| `evt_103` | 2025-07-25 13:42 | 记录时间见本行 UTC 时间 | `0xe4b5b266…` → 3 个接收地址 | 分发主体继续向下游拆分筹码，后续若进入 CEX 或 DEX 路由就是实际卖压。 | 合计 10,092,335 tokens |
| `evt_065` | 2025-08-11 12:40 | 记录时间见本行 UTC 时间 | `0x05cb186a…` → 1 个接收地址 | 分发主体继续向下游拆分筹码，后续若进入 CEX 或 DEX 路由就是实际卖压。 | 合计 10,000,000 tokens |

### 🟡 第三波 近 72h 异常活动 (2026-06-29 ~ 2026-06-29 UTC, **该波事件显示筹码仍在向下游移动，和当前价格拉升叠加后，对持仓更偏风险信号。**)

| 事件编号 | UTC | 距今 | 来源 → 目标 | 性质 | 金额 |
|---|---|---|---|---|---|
| `evt_162` | 2026-06-29 09:36 | 记录时间见本行 UTC 时间 | `0x00000000…` → `0x1b5c6800…` | 近端大额异动，发生在价格拉升阶段，需要按潜在派发或换手风险处理。 | 41,757,498 tokens |
| `evt_163` | 2026-06-29 09:25 | 记录时间见本行 UTC 时间 | `0x00000000…` → `0x9c2bf15c…` | 近端大额异动，发生在价格拉升阶段，需要按潜在派发或换手风险处理。 | 40,259,611 tokens |
| `evt_164` | 2026-06-29 11:37 | 记录时间见本行 UTC 时间 | `0x86e5568c…` → `0x5528cf58…` | 近端大额异动，发生在价格拉升阶段，需要按潜在派发或换手风险处理。 | 356,253 tokens |
| `evt_165` | 2026-06-29 11:37 | 记录时间见本行 UTC 时间 | `0x5528cf58…` → `0x00000000…` | 近端大额异动，发生在价格拉升阶段，需要按潜在派发或换手风险处理。 | 356,253 tokens |
| `evt_166` | 2026-06-29 11:28 | 记录时间见本行 UTC 时间 | `0xa8e2b270…` → `0x86e5568c…` | 近端大额异动，发生在价格拉升阶段，需要按潜在派发或换手风险处理。 | 356,253 tokens |
| `evt_167` | 2026-06-29 12:48 | 记录时间见本行 UTC 时间 | `0x73d8bd54…` → `0x6aba0315…` | 近端大额异动，发生在价格拉升阶段，需要按潜在派发或换手风险处理。 | 308,181 tokens |
| `evt_168` | 2026-06-29 12:48 | 记录时间见本行 UTC 时间 | `0x6aba0315…` → `0xb300000b…` | 近端大额异动，发生在价格拉升阶段，需要按潜在派发或换手风险处理。 | 308,181 tokens |
| `evt_169` | 2026-06-29 08:58 | 记录时间见本行 UTC 时间 | `0x346d2533…` → `0x5528cf58…` | 近端大额异动，发生在价格拉升阶段，需要按潜在派发或换手风险处理。 | 304,310 tokens |


</details>


## 主战场链

| 项目 | 取值 |
|---|---|
| **主战场链** | **BSC** (BNB Chain) |
| 铸造链 | BSC, totalSupply 10,258,557,461 |
| 交易链 | BSC (Alpha + DEX 主池) |
| 跨链分布 | **单链, 无跨链桥发现** (v0.6 phase B.3 minimal — 仅 BSC 检测) |
| 报告覆盖范围 | **完整覆盖** |

✅ 无非 BSC 链数据需求.

**解读**: TAC 当前 Alpha 主战场是 BSC，CoinGecko 只给出 BSC 合约，本轮没有触发跨链供应覆盖警报，报告结论主要基于 BSC 链上证据。

## 入场价 锚点

| 时间锚点 | UTC | 价格 | 相对当前 |
|---|---|---|---|
| LP 创建首笔 (DEX 启动) | — | — | — |
| Alpha 上线首笔 | 2025-07-15 10:00 UTC | — | — |
| **当前价** | 2026-06-29 | **$0.0571** | 1.00× |

**解读**: Alpha 上线时间明确，但 LP 首笔价格缺失；当前价约 $0.057125，短线涨幅很大，不能用缺失的开盘锚去证明估值便宜。

<a id="section-alloc"></a>
## 项目方话语权

| 项目 | 取值 | 来源 |
|---|---|---|
| Alpha 配额比例 (官方披露) | **未披露** | Binance Alpha 官方接口当前未给出该字段 |
| 项目方钱包 `0x64f6902c…` 当前余额 | 几乎空仓 (全部分发完) | 项目方分发追溯 |
| 上线前内幕接收方 14 个累计余额 | 69,708,267 tokens (= 0.68% 总供应) | 内幕钱包累计 |
| 潜伏钱包 1 个持仓 (核心未来风险) | **2 tokens (= 0.00% 总供应 / $0)** | 未分发内幕钱包 |
| 已分完内幕钱包 10 个 (分发完成) | 已 100% 分完, 剩余 0 | 已转出 ≥95% 的内幕钱包 |

**解读**: 官方 Alpha 配额未披露，链上可见的上线前接收方规模有限，但已分完和分发中地址同时存在，说明风险集中在后续变现路径。

## 短期上 CEX 催化剂

| 交易所 | 状态 | 时间 | 距今 |
|---|---|---|---|
| Binance | 未上线 | — | — |
| Aster | 未核实 | — | — |
| Bitget | 未核实 | — | — |

无 14 天内新催化剂. 当前 S1 (Alpha only).

**解读**: TAC 当前仍是 S1，未看到 Binance 合约永续上线；短线催化不足，链上出货压力比 CEX 上新预期更重要。

<a id="section-liq"></a>
## 进场上限

| 锚点 | 取值 | 备注 |
|---|---|---|
| **不超 5% 滑点的最大单笔买入 (估算)** | $8,111 | 由 Alpha 24h vol 推导 (vol_24h / 96 × 0.05 启发式估算) |
| DEX 主池流动性 | — | 无主池 |
| DEX 主池 24h 交易量 | $21,346,044 | surf project-detail (跨链 CEX+DEX 实时聚合) |
| 池子代币 24h 净进出 (throughput, 非 LP 增减) | — | surf agent.bsc_transfers |
| DEX 主池地址 | — | FDV $572,968,428 |

**解读**: 不超 5% 滑点的估算买入上限约 $8,111，拆分后的单笔上限约 $2,703；在 24h 暴涨和派发并存时，盘口并不支持大仓位追入。

<a id="section-holdings"></a>
## 各角色持仓分布

**持仓分布表**:

| 角色 | 钱包数 | 当前持仓 | 占总供应 % | Top 钱包 |
|---|---|---|---|---|
| DEX 主池 | 0 | 0 | —% | — |
| 项目方钱包 | 1 | 4,000,099 | 0.0390% | [`0x64f6902c…`](https://bscscan.com/address/0x64f6902c232b2eadc731b316c0d7d0fa88d4ff7e) |
| 项目方/基建/分发池 (vesting / 多签 / treasury / DEX 基建 / CEX 托管 / 第三方分发平台 / 散户 claim 池, Arkham 已确认) | 6 | 125,580,227 | 1.2242% | [`0x6cd06aaf…`](https://bscscan.com/address/0x6cd06aaf06506bc3ff382d83023354e2b80eed22) |
| 潜伏钱包 (内幕未分发) | 0 | 0 | —% | — |
| 分发中钱包 (内幕) | 1 | 36,298,165 | 0.3538% | [`0xb5893a55…`](https://bscscan.com/address/0xb5893a55965a4a01c239f852d93ac47942415231) |
| 已分完钱包 (内幕) | 1 | 326,400 | 0.0032% | [`0x93deb693…`](https://bscscan.com/address/0x93deb693b170d56bdde1b0a5222b14c0f885d976) |
| 散户接收 (分发下游) | 3 | 1,242,548 | 0.0121% | [`0x6984e749…`](https://bscscan.com/address/0x6984e749baf0faf6a2f6bffd940806abb495cb1c) |
| 其他 (散户+未分类) | 38 | 598,014,825 | 5.8294% | [`0xbd2f3b1a…`](https://bscscan.com/address/0xbd2f3b1aabdb4910829a445afcda7175c457753e) |

**关键解读**:
- 内幕树 **14** 钱包累计持 **0.7%** 总供应, 含 6 已分完 (各持 ≈ 0) · 1 分发中 · 1 持仓接近 0 · 6 公开锁仓 custody / dust 未分类.
- insider 已链上确认流出 **3.5M USD** = **4.05%** 流通, 用内幕自卖 TWAP 计价 (非 wash 报价).

<details>
<summary>📂 <strong>上溯发现 (项目方钱包 → 内幕谱系)</strong> — 8 个内幕钱包: 6 已分完 / 1 分发中 / 1 潜伏 (click 展开看完整谱系 + 钱包余额 + 派发率) (+6 CEX/DEX 中性 infra)</summary>

**内幕钱包列表 (项目方分发追溯)**:

| 编号 | 地址 | 收自项目方 | 当前持仓 | 已分 % |
|---|---|---|---|---|
| `m6_001` | [`0x93deb693`](https://bscscan.com/address/0x93deb693b170d56bdde1b0a5222b14c0f885d976) | 200,000,000 | 326,400 | 99.8% |
| `m6_002` | [`0xfe5b95b0`](https://bscscan.com/address/0xfe5b95b0f1d5e43d639d4986c4dd019be3be556e) | 1 | 2 | 0.0% |
| `m6_003` | [`0x73d8bd54`](https://bscscan.com/address/0x73d8bd54f7cf5fab43fe4ef40a62d390644946db) 🏦Binance Wallet | 150,000,000 | 21,633,725 | 85.6% |
| `m6_004` | [`0xb5893a55`](https://bscscan.com/address/0xb5893a55965a4a01c239f852d93ac47942415231) | 49,956,875 | 36,298,165 | 27.3% |
| `m6_005` | [`0x05cb186a`](https://bscscan.com/address/0x05cb186ab8ec85378a2cbf8a858568a8fb216b07) 🏦Binance Deposit | 10,000,000 | 0 | 100.0% |
| `m6_006` | [`0x6aba0315`](https://bscscan.com/address/0x6aba0315493b7e6989041c91181337b662fb1b90) 🏦Binance Wallet | 847,840,580 | -2,138 | 100.0% |
| `m6_007` | [`0xb300000b`](https://bscscan.com/address/0xb300000b72deaeb607a12d5f54773d1c19c7028d) 💧DEX Router | 76,117,334 | 2,676 | 100.0% |
| `m6_008` | [`0xbd97306a`](https://bscscan.com/address/0xbd97306a087ed0c46b783cfbfdcdc6c12c7a2866) | 20,677,521 | 103,390 | 99.5% |
| `m6_009` | [`0xe4b5b266`](https://bscscan.com/address/0xe4b5b2667e049ac8c79ae6c5a7e3300815aa32be) 🏦Binance | 10,000,000 | 0 | 100.0% |
| `m6_010` | [`0xca852767`](https://bscscan.com/address/0xca852767b43a395ac1dd54737193eba5e20c78bd) | 680,154,892 | 0 | 100.0% |
| `m6_011` | [`0xde9e4fe3`](https://bscscan.com/address/0xde9e4fe32b049f821c7f3e9802381aa470ffca73) | 225,794,011 | -0 | 100.0% |
| `m6_012` | [`0x0501f595`](https://bscscan.com/address/0x0501f595d17dd90ff11a9873692ee3f8d478f4e5) | 162,598,787 | 0 | 100.0% |
| `m6_013` | [`0xd2cd331e`](https://bscscan.com/address/0xd2cd331e493a325dd5634cfeb93852389c0aaece) 💧V3 Pool | 24,745,912 | 11,346,048 | 54.1% |
| `m6_014` | [`0x653dd767`](https://bscscan.com/address/0x653dd7677aea3030eab68c97ed3594bacf560158) | 15,523,470 | 0 | 100.0% |
_统计 (m6 谱系全集 **8** 个): 1 持仓接近 0 / 公开锁仓 custody · 1 分发中 · 6 已分完_

**m4_notes (LP 前预分配解读)**:
- 项目方分发追溯: 项目方钱包 0x64f6902c... 于 2025-07-10 23:22 铸造 308,997,145 tokens, 上线前向 8 个内幕地址分发 308,997,145. 潜伏钱包 (未分发) 1 个, 合计持仓 2 tokens.
- 项目方部署钱包已完成多轮上线前分发，后续风险不在部署钱包余额本身，而在接收方和下游地址是否继续进入交易所或路由。
- M4/M6 接收方里已经出现已分完和分发中地址，说明筹码并非静态锁仓；监控重点应放在分发中钱包、铸币权限相关地址和高频清仓钱包。



**⚠️ Step4 预算上限截断 (Data Gap — 结论是下界)**: 分发树宽度超过 step4 递归预算 (默认 12), 已展开最大的若干个 sub-dumper, **另有 7 个 sub-dumper (累计约 28,080,354 tokens) 未递归展开**. 当前 verdict 基于已展开部分, 是**下界** — 真实操盘网络可能更深。
_Action: 这是预算截断不是 surf 失败. 需要完整深度跑 `BINANCE_ALPHA_STEP4_MAX_DUMPERS=40` 重跑._

</details>

## 💰 高价值地址资金来源 (mint / DEX / P2P)

下面是 对敲配置 / 流水大户 / m6 内幕 / Top-30 持币人 段里已经标记过的高价值地址, 按 365 天内**收到的 token 来源**分类: mint (从 0x0 直接铸造, 矿币 / 跨链桥 / 空投 mint 合约都算) / DEX 买入 (从已知 DEX 主池买入) / P2P (其他 EOA 转账, 包含未识别的 CEX 提现). 用来判断: ⛏️ Mint 占比高 = 矿币 / 跨链桥 token 操作员或挖空投的 马甲钱包; 🟢 DEX 占比高 = 真买盘 散户 持仓; 🔵 P2P 占比高 = 操作员归集 / OTC 接收.

> 已查 200 个高价值地址, 其中 41 个 365 天内有真实收币记录 — ⛏️ Mint 主导 1 个 / 🟢 DEX 主导 0 个 / 🔵 P2P 主导 40 个.


| 地址 | 首要来源 | 总收币 | mint % | DEX 买入 % | P2P % |
|---|---|---:|---:|---:|---:|
| [`0xd2cd331e…`](https://bscscan.com/address/0xd2cd331e493a325dd5634cfeb93852389c0aaece) | 🔵 P2P 转账主导 | 8,055,179,818 | 0.0% | 0.0% | 100.0% |
| [`0xb300000b…`](https://bscscan.com/address/0xb300000b72deaeb607a12d5f54773d1c19c7028d) | 🔵 P2P 转账主导 | 1,812,373,452 | 0.0% | 0.0% | 100.0% |
| [`0x6aba0315…`](https://bscscan.com/address/0x6aba0315493b7e6989041c91181337b662fb1b90) | 🔵 P2P 转账主导 | 1,559,371,654 | 0.0% | 0.0% | 100.0% |
| [`0x73d8bd54…`](https://bscscan.com/address/0x73d8bd54f7cf5fab43fe4ef40a62d390644946db) | 🔵 P2P 转账主导 | 966,673,063 | 0.0% | 0.0% | 100.0% |
| [`0xca852767…`](https://bscscan.com/address/0xca852767b43a395ac1dd54737193eba5e20c78bd) | 🔵 P2P 转账主导 | 681,383,561 | 0.0% | 0.0% | 100.0% |
| [`0xde9e4fe3…`](https://bscscan.com/address/0xde9e4fe32b049f821c7f3e9802381aa470ffca73) | 🔵 P2P 转账主导 | 434,633,164 | 0.0% | 0.0% | 100.0% |
| [`0x2aa6845f…`](https://bscscan.com/address/0x2aa6845f7e84b2cc1619c823bf4f6b04ec733f2c) | 🔵 P2P 转账主导 | 363,118,272 | 0.0% | 0.0% | 100.0% |
| [`0x93deb693…`](https://bscscan.com/address/0x93deb693b170d56bdde1b0a5222b14c0f885d976) | 🔵 P2P 转账主导 | 210,326,400 | 0.0% | 0.0% | 100.0% |
| [`0x088ca577…`](https://bscscan.com/address/0x088ca577f148a47da34ad3664f5c3cd5d0cc3986) | 🔵 P2P 转账主导 | 167,117,450 | 0.0% | 0.0% | 100.0% |
| [`0x0501f595…`](https://bscscan.com/address/0x0501f595d17dd90ff11a9873692ee3f8d478f4e5) | 🔵 P2P 转账主导 | 165,212,987 | 0.0% | 0.0% | 100.0% |
| [`0xa73072ad…`](https://bscscan.com/address/0xa73072adc6c34859426fcc29bc6ca2cac07c93c3) | 🔵 P2P 转账主导 | 111,352,108 | 0.0% | 0.0% | 100.0% |
| [`0x7736a721…`](https://bscscan.com/address/0x7736a721ce90abdb8183f9cbe9e6f6b61c32cef2) | 🔵 P2P 转账主导 | 85,936,262 | 0.0% | 0.0% | 100.0% |
| [`0x9a13a9fa…`](https://bscscan.com/address/0x9a13a9fac1644f02890a326d0fbef08302cb89e1) | 🔵 P2P 转账主导 | 80,292,467 | 0.0% | 0.0% | 100.0% |
| [`0xf51a9efb…`](https://bscscan.com/address/0xf51a9efb3f8ed40e0f8bbd5de44b0bcdd4f2a98e) | 🔵 P2P 转账主导 | 71,875,018 | 0.0% | 0.0% | 100.0% |
| [`0x2c61ee89…`](https://bscscan.com/address/0x2c61ee89e44ae920f3310fe080865d220a1b777c) | 🔵 P2P 转账主导 | 70,032,356 | 0.0% | 0.0% | 100.0% |
| [`0x1b7e4ca1…`](https://bscscan.com/address/0x1b7e4ca15a2fe5310a91d4754a67ea52a0a7dc03) | 🔵 P2P 转账主导 | 65,184,149 | 0.0% | 0.0% | 100.0% |
| [`0xfea18be5…`](https://bscscan.com/address/0xfea18be59b326917572fbb999410749b22f335bf) | 🔵 P2P 转账主导 | 63,230,882 | 0.0% | 0.0% | 100.0% |
| [`0x24d3857d…`](https://bscscan.com/address/0x24d3857d80e915f98421248ab06530c7a39362f7) | 🔵 P2P 转账主导 | 56,973,553 | 0.0% | 0.0% | 100.0% |
| [`0x80d9e531…`](https://bscscan.com/address/0x80d9e531b5e091580df76ae505a3b8695c36ec0e) | 🔵 P2P 转账主导 | 54,380,440 | 0.0% | 0.0% | 100.0% |
| [`0x561a3a8f…`](https://bscscan.com/address/0x561a3a8f7c97b66248c8a343a2649301740ce7c5) | 🔵 P2P 转账主导 | 53,396,450 | 0.0% | 0.0% | 100.0% |
| [`0xb5893a55…`](https://bscscan.com/address/0xb5893a55965a4a01c239f852d93ac47942415231) | 🔵 P2P 转账主导 | 49,956,875 | 0.0% | 0.0% | 100.0% |
| [`0xe31fb549…`](https://bscscan.com/address/0xe31fb549b68e5df2cc521795fb9b59c9da5dd197) | 🔵 P2P 转账主导 | 43,402,907 | 0.0% | 0.0% | 100.0% |
| [`0x6cd1b8cf…`](https://bscscan.com/address/0x6cd1b8cfcd2ca2bcdb46a2d96bd22b92e16ba427) | 🔵 P2P 转账主导 | 43,230,039 | 0.0% | 0.0% | 100.0% |
| [`0xd4ade84d…`](https://bscscan.com/address/0xd4ade84d1e4b1015a5dda8eb6c43858a3ac905f5) | 🔵 P2P 转账主导 | 40,980,964 | 0.9% | 0.0% | 99.1% |
| [`0xbd97306a…`](https://bscscan.com/address/0xbd97306a087ed0c46b783cfbfdcdc6c12c7a2866) | 🔵 P2P 转账主导 | 40,676,772 | 0.0% | 0.0% | 100.0% |
| [`0x3159fc5e…`](https://bscscan.com/address/0x3159fc5ed978688b451c854895dc24d67e02bab8) | 🔵 P2P 转账主导 | 36,290,000 | 0.0% | 0.0% | 100.0% |
| [`0x0e91e407…`](https://bscscan.com/address/0x0e91e407a3c8887b0713d9abf7695cb6efdc385c) | 🔵 P2P 转账主导 | 25,972,782 | 0.0% | 0.0% | 100.0% |
| [`0xf86aabe6…`](https://bscscan.com/address/0xf86aabe61b1df0f33dd09f3b7bf8232f3d01a904) | 🔵 P2P 转账主导 | 23,394,177 | 0.0% | 0.0% | 100.0% |
| [`0xfc1221d1…`](https://bscscan.com/address/0xfc1221d10f967ed0ecf34a7f763d328d19d470a1) | 🔵 P2P 转账主导 | 21,319,676 | 0.0% | 0.0% | 100.0% |
| [`0x154cd934…`](https://bscscan.com/address/0x154cd934c93f21a4ba4e8ee8ec4b3cba4687259f) | 🔵 P2P 转账主导 | 20,689,692 | 0.0% | 0.0% | 100.0% |

> _扫描封顶: 工作流 收集到 241 个高价值候选, max_addrs cap = 200, 实际入查 200 个 (按 检测器 优先级排序: 对敲 → flow → m6 → 出货-sellers → Top-30 持币人). 截断 41 个 — 多见于 PLAY 类大量 flow_operators (60+) token._

> _CEX 提现这一栏暂未独立标识 (v0.7.24 候选), 当前归入 P2P. 真 CEX hot 钱包 转出 vs 普通 EOA 转账无法区分时, 都算 P2P._


### ⛏️ Mining-fed 钱包出货明细 (v0.7.23.2)

> Mining-fed 钱包 (1 个) 365 天内通过 DEX 卖出: **0 tokens ≈ $0 USD**, 总链上 outflow 600,000 tokens. **这是矿币 / 跨链桥 token 模式下 dump_tracker 拿不到的真实出货数据** — 庄家 通过 挖矿 合约领币然后变现的路径.

**[`0xfe5b95b0f1d5…`](https://bscscan.com/address/0xfe5b95b0f1d5e43d639d4986c4dd019be3be556e)** —
 无 DEX 卖出记录.
 Top outflow:
> - [`0x6535380044be…`](https://bscscan.com/address/0x6535380044be29b93f1c73461b5e3a115e28bfd4) ← 600,000 tokens (1 笔)


<a id="section-bridge-mint"></a>
### 🌉 跨链桥 / 铸币权限合约 自卖明细 (v0.7.24a)

> 检测到 **9 个 铸币权限合约 合约** (从 0x0 接收 mint, 排除 合约部署地址 + 已在 挖矿机制取得 段覆盖的钱包). 它们是 跨链桥 / staking / airdrop 合约, **自己**也可能 DEX swap. 这是 v0.7.23.x 系列完全漏掉的 出货 路径.

| Authority 地址 | Arkham 标签 | 365d Mint 量 | % 总供应 | 自己 DEX 卖出 | USD ≈ |
|---|---|---:|---:|---|---:|
| [`0xb213531aa811…`](https://bscscan.com/address/0xb213531aa8113f455c626a305feaef82da605e08) | _无标签 (新发合约 Arkham 未收录) | 51,921,464 | 0.51% | 5,486,054 tokens (18 笔) | **$111,062** |
| [`0xbd2f3b1aabdb…`](https://bscscan.com/address/0xbd2f3b1aabdb4910829a445afcda7175c457753e) | _无标签 (新发合约 Arkham 未收录) | 45,173,485 | 0.44% | — (未直接 DEX 自卖) | — |
| [`0x6ee6462f65b9…`](https://bscscan.com/address/0x6ee6462f65b922d5863bec36a3e6c2008be05291) | _无标签 (新发合约 Arkham 未收录) | 44,426,717 | 0.43% | — (未直接 DEX 自卖) | — |
| [`0x1b5c6800daac…`](https://bscscan.com/address/0x1b5c6800daacb36a43c94378fcdc5d18e8f5e6e1) | _无标签 (新发合约 Arkham 未收录) | 41,757,498 | 0.41% | — (未直接 DEX 自卖) | — |
| [`0x9c2bf15cc697…`](https://bscscan.com/address/0x9c2bf15cc69740effef5717072a3d00f04afdf66) | _无标签 (新发合约 Arkham 未收录) | 40,259,611 | 0.39% | — (未直接 DEX 自卖) | — |
| [`0x3b9345aa7765…`](https://bscscan.com/address/0x3b9345aa7765d0886384d91c422b7fb8eb276565) | _无标签 (新发合约 Arkham 未收录) | 39,484,719 | 0.38% | — (未直接 DEX 自卖) | — |
| [`0x13d8e224c375…`](https://bscscan.com/address/0x13d8e224c3759a6e2c1f5f6c848dda2af3c489c4) | _无标签 (新发合约 Arkham 未收录) | 38,898,262 | 0.38% | — (未直接 DEX 自卖) | — |
| [`0x143bb85e9314…`](https://bscscan.com/address/0x143bb85e9314e97b55e61195bf0ed032e7291caa) | _无标签 (新发合约 Arkham 未收录) | 38,412,685 | 0.37% | — (未直接 DEX 自卖) | — |
| [`0x708db14970c9…`](https://bscscan.com/address/0x708db14970c9079f64d552e8b3cf33525f0123d5) | _无标签 (新发合约 Arkham 未收录) | 38,214,950 | 0.37% | — (未直接 DEX 自卖) | — |


> 🌉 铸币权限合约 **自己** 365d 通过 DEX 卖出: **5,486,054 tokens ≈ $111,062 USD**. 这是 跨链桥 contract 直接 swap 出去的部分 — 跟 挖矿机制取得 操作员的 出货 是独立两条路径, **真实总 出货 应该是两者相加**.


**[`0xb213531aa811…`](https://bscscan.com/address/0xb213531aa8113f455c626a305feaef82da605e08)** 自 DEX 卖出 $111,062 USD, top outflow:
> - [`0x6e4141d33021…`](https://bscscan.com/address/0x6e4141d33021b52c91c28608403db4a0ffb50ec6) ← 4,122,071 tokens (6 笔) · 🏷️ **Kyber Network** (Aggregator Executor)> - [`0xde9e4fe32b04…`](https://bscscan.com/address/0xde9e4fe32b049f821c7f3e9802381aa470ffca73) ← 1,363,983 tokens (3 笔) · 🏷️ **1inch**

<a id="section-high-throughput"></a>
### 🌊 高频出货钱包 (v0.7.24b)

> 检测到 **93 个 庄家 钱包**有 高频 清仓 pattern (大额 token 流过 + 余额 ≈ 0 + 高频 tx). 阈值: 吞吐 1M ~ 5% 总供应, 余额 < 吞吐 5%, n_tx ≥ 1000. 已 filter 掉 DEX 路由 / CEX deposit / 聚合器 等 infra 标签 (它们不是 庄家). 这是 60d 之前 出货完毕走人的 庄家 — flow_operators (60d 窗) + 挖矿机制取得 (余额 > threshold) 都漏掉.

| 庄家 地址 | 主要角色 | Arkham 标签 | 365d 流入 (= 收 mint/p2p) | 流出 (= 卖 / 转走) | 残留 余额 | tx 笔数 |
|---|---|---|---:|---:|---:|---:|
| [`0xde9e4fe32b04…`](https://bscscan.com/address/0xde9e4fe32b049f821c7f3e9802381aa470ffca73) | 🌊 HT 庄家 (primary) | 1inch | 434,633,164 | 434,633,164 | -0 | 65,332 |
| [`0x2aa6845f7e84…`](https://bscscan.com/address/0x2aa6845f7e84b2cc1619c823bf4f6b04ec733f2c) | 🌊 HT 庄家 (primary) | _无标签 (EOA / 未收录) | 363,118,272 | 363,121,989 | -3,717 | 32,337 |
| [`0x4923d960f84d…`](https://bscscan.com/address/0x4923d960f84d89e72c78daf82015b519aaafe994) | 🌊 HT 庄家 (primary) | _无标签 (EOA / 未收录) | 334,071,329 | 334,074,889 | -3,560 | 104,468 |
| [`0x42407fb33b34…`](https://bscscan.com/address/0x42407fb33b3487fd7b644d84f35818a63e22b03c) | 🌊 HT 庄家 (primary) | _无标签 (EOA / 未收录) | 311,609,409 | 311,609,409 | -0 | 16,197 |
| [`0x971435fc38ee…`](https://bscscan.com/address/0x971435fc38eed5e0aaff0dd717d0d16a02a4110e) | 🌊 HT 庄家 (primary) | _无标签 (EOA / 未收录) | 292,050,772 | 292,047,930 | 2,841 | 90,243 |
| [`0x628683c3c54e…`](https://bscscan.com/address/0x628683c3c54ec4a22217d0022d0d442b391e9a4f) | 🌊 HT 庄家 (primary) | _无标签 (EOA / 未收录) | 285,076,382 | 285,152,855 | -76,473 | 19,163 |
| [`0x73b4c8188922…`](https://bscscan.com/address/0x73b4c818892283e5fc37fee7b91ff7245b236d3c) | 🌊 HT 庄家 (primary) | _无标签 (EOA / 未收录) | 229,262,020 | 229,237,949 | 24,071 | 80,829 |
| [`0x278d858f05b9…`](https://bscscan.com/address/0x278d858f05b94576c1e6f73285886876ff6ef8d2) | 🌊 HT 庄家 (primary) | _无标签 (EOA / 未收录) | 199,436,435 | 199,380,736 | 55,699 | 81,203 |
| [`0x111111125421…`](https://bscscan.com/address/0x111111125421ca6dc452d289314280a0f8842a65) | 🌊 HT 庄家 (primary) | 1inch (AggregationRouterV6) | 191,822,990 | 191,822,990 | -0 | 15,281 |
| [`0xb891cc3b4271…`](https://bscscan.com/address/0xb891cc3b4271e85644c4e871e16c650ecc71d5b0) | 🌊 HT 庄家 (primary) | _无标签 (EOA / 未收录) | 172,198,256 | 172,184,978 | 13,278 | 22,940 |
| [`0x2f0cabba08a9…`](https://bscscan.com/address/0x2f0cabba08a90d30382ee731f361198e7155dbb6) | 🌊 HT 庄家 (primary) | _无标签 (EOA / 未收录) | 167,954,453 | 168,159,324 | -204,871 | 32,638 |
| [`0x088ca577f148…`](https://bscscan.com/address/0x088ca577f148a47da34ad3664f5c3cd5d0cc3986) | 🌊 HT 庄家 (primary) | _无标签 (EOA / 未收录) | 167,117,450 | 167,117,450 | -0 | 5,534 |
| [`0x0501f595d17d…`](https://bscscan.com/address/0x0501f595d17dd90ff11a9873692ee3f8d478f4e5) | 🌊 HT 庄家 (primary) | _无标签 (EOA / 未收录) | 165,212,987 | 165,212,987 | -0 | 29,430 |
| [`0x62ccef0b4545…`](https://bscscan.com/address/0x62ccef0b4545166f721caa9fee13c1d3767e27dc) | 🌊 HT 庄家 (primary) | DexRouter | 134,938,213 | 134,943,550 | -5,337 | 51,230 |
| [`0x7817dbf38e9d…`](https://bscscan.com/address/0x7817dbf38e9d1c95671625f0052c147864692fe0) | 🌊 HT 庄家 (primary) | _无标签 (EOA / 未收录) | 132,777,221 | 132,571,699 | 205,523 | 72,182 |
| [`0x75f838dbf3be…`](https://bscscan.com/address/0x75f838dbf3be0a79d6e5904ab5c364d5418a5f66) | 🌊 HT 庄家 (primary) | _无标签 (EOA / 未收录) | 119,062,231 | 118,571,531 | 490,700 | 3,760 |
| [`0x5528cf58feb8…`](https://bscscan.com/address/0x5528cf58feb8fbfce94f43b33240fffb1312bde3) | 🌊 HT 庄家 (primary) | LZMultiCall | 117,807,878 | 117,807,878 | 0 | 1,282 |
| [`0x3d2bb7e9df6b…`](https://bscscan.com/address/0x3d2bb7e9df6b49b82ec75214aea8feddab78fc5f) | 🌊 HT 庄家 (primary) | _无标签 (EOA / 未收录) | 116,962,058 | 116,944,841 | 17,216 | 10,474 |
| [`0xa73072adc6c3…`](https://bscscan.com/address/0xa73072adc6c34859426fcc29bc6ca2cac07c93c3) | 🌊 HT 庄家 (primary) | _无标签 (EOA / 未收录) | 111,352,108 | 111,258,410 | 93,699 | 2,759 |
| [`0x2087d8fe9279…`](https://bscscan.com/address/0x2087d8fe927966fee758ba5563fb8f2347180b7c) | 🌊 HT 庄家 (primary) | _无标签 (EOA / 未收录) | 107,375,295 | 107,381,760 | -6,465 | 42,658 |

> _仅展示前 20 个, 共检测到 93 个高频庄家钱包 (按过账量排序; 过账 = token 进出流量, 不等于卖出量). 完整列表见 skeleton.json `funding_attribution.high_throughput_dumpers.dumpers`._

> 🌊 这些钱包 365d 内合计流过 **6,888,040,830 tokens** 然后清仓走人 — 已经 出货完毕的 庄家. 它们已经卖完了, 但**未来如果项目方再 mint 一批分发给类似 pattern 钱包**, 它们就是下一波 出货 风险源.





<a id="section-monitoring"></a>
## 监控钱包 + 实时告警


> 📊 **监控优先级 (v0.7.27 确定性 ranker)**: 🚨 5 CRITICAL · 🔥 10 HIGH · 👀 0 NORMAL · 💤 6 NOT_TRACKED (不导出 paste.json)>
> paste.json 里钱包已按等级排序, 🚨 在最前. 优先盯 CRITICAL+HIGH (15 个), 这些钱包动 = 改变链上侦测 判断. NORMAL (0 个) 做批量 交叉核对, 不需要 push notification. 💤 NOT_TRACKED 是 DEX 路由 / 公共 CEX 热钱包, 流量噪音淹没真信号, 已从 paste 剔除.

_(report 仅展示 top 10, 完整 21 个钱包请用 `monitoring/monitoring_paste.json` 一键粘贴进 Binance Wallet / OKX 监控)_

| # | 等级 | 钱包 | 角色 | primary 角色段 | 触发条件 | 状态 |
|---|:-:|---|---|---|---|---|
| 1 | 🔥 HIGH | [`0x64f6902c`](https://bscscan.com/address/0x64f6902c232b2eadc731b316c0d7d0fa88d4ff7e) | 项目方部署钱包 | [项目方话语权](#section-alloc) | 链上行为参考: 大额 (≥ $10k) 转入 DEX 路由 / CEX 充值地址 | 🟡 |
| 2 | 🔥 HIGH | [`0x93deb693`](https://bscscan.com/address/0x93deb693b170d56bdde1b0a5222b14c0f885d976) | 已分完钱包 (已分 100%) | — | 链上行为参考: 大额 (≥ $10k) 转入 DEX 路由 / CEX 充值地址 | 🟢 |
| 3 | 🔥 HIGH | [`0xfe5b95b0`](https://bscscan.com/address/0xfe5b95b0f1d5e43d639d4986c4dd019be3be556e) | 潜伏钱包 (持 2 tokens, 未分发) | — | 链上行为参考: 大额 (≥ $10k) 转入 DEX 路由 / CEX 充值地址 | 🔴 |
| 4 | 💤 NOT_TRACKED | [`0x73d8bd54`](https://bscscan.com/address/0x73d8bd54f7cf5fab43fe4ef40a62d390644946db) | 🏦 CEX 平台中转 (Binance Wallet) | [📌 监控钱包](#section-monitoring) | 不导出到 paste.json (基础设施 / 公共钱包流量过高) | ⚪ |
| 5 | 🔥 HIGH | [`0xb5893a55`](https://bscscan.com/address/0xb5893a55965a4a01c239f852d93ac47942415231) | 分发中钱包 (已分 27%) | — | 链上行为参考: 大额 (≥ $10k) 转入 DEX 路由 / CEX 充值地址 | 🟠 |
| 6 | 💤 NOT_TRACKED | [`0x05cb186a`](https://bscscan.com/address/0x05cb186ab8ec85378a2cbf8a858568a8fb216b07) | 🏦 CEX 平台中转 (Binance Deposit) | [📌 监控钱包](#section-monitoring) | 不导出到 paste.json (基础设施 / 公共钱包流量过高) | ⚪ |
| 7 | 💤 NOT_TRACKED | [`0x6aba0315`](https://bscscan.com/address/0x6aba0315493b7e6989041c91181337b662fb1b90) | 🏦 CEX 平台中转 (Binance Wallet) | [📌 监控钱包](#section-monitoring) | 不导出到 paste.json (基础设施 / 公共钱包流量过高) | ⚪ |
| 8 | 💤 NOT_TRACKED | [`0xb300000b`](https://bscscan.com/address/0xb300000b72deaeb607a12d5f54773d1c19c7028d) | 💧 DEX 流动性池 (DEX Router) | [🔵 LP 深度段](#section-liq) | 不导出到 paste.json (基础设施 / 公共钱包流量过高) | ⚪ |
| 9 | 🔥 HIGH | [`0xbd97306a`](https://bscscan.com/address/0xbd97306a087ed0c46b783cfbfdcdc6c12c7a2866) | 已分完钱包 (已分 100%) | [🌊 高频出货钱包](#section-high-throughput) | 链上行为参考: 大额 (≥ $10k) 转入 DEX 路由 / CEX 充值地址 | 🟢 |
| 10 | 💤 NOT_TRACKED | [`0xe4b5b266`](https://bscscan.com/address/0xe4b5b2667e049ac8c79ae6c5a7e3300815aa32be) | 🏦 CEX 平台中转 (Binance) | [📌 监控钱包](#section-monitoring) | 不导出到 paste.json (基础设施 / 公共钱包流量过高) | ⚪ |

监控列表优先盯 HIGH 和 CRITICAL 地址，尤其是分发中钱包、铸币权限相关钱包和高频清仓钱包；公共 CEX 热钱包噪音过高，不适合单独跟踪。

## 机器可读 JSON (精简)

```json
{
  "schema_version": "1.2.6",
  "symbol": "TAC",
  "verdict": "EXIT_IF_HOLDING",
  "verdict_zh": "建议卖出",
  "verdict_downgrade_applied": 1,
  "chain_state": "RECENT_DISTRIBUTION",
  "chain_state_label": "近 72h 链上活动 — 100 笔大额转移",
  "chain_state_risk_score": 9,
  "alpha_listing_tier": "S1",
  "any_anomaly_firing": true,
  "render_provenance": {
    "rendered_by": "render_report.py (v0.6, jinja2)",
    "data_source": "report_data.json (LLM-filled, Python-validated)",
    "deterministic": true
  },
  "structural_counts": {
    "anomaly_waves": 3,
    "evidence_graph_entries": 299,
    "holdings_role_rows": 8,
    "holdings_progress_bars": 8,
    "monitoring_wallets": 21,
    "lineage_flowchart_nodes": 24,
    "lineage_flowchart_edges": 47,
    "m6_rows": 14,
    "decision_anchors": 3,
    "decision_re_entry_conditions": 2
  },
  "address_role_index": {
    "0x6134e2c57837d5abfc52e0bee486004badfa8b27": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xb213531aa8113f455c626a305feaef82da605e08": {
      "primary_role": "mint_authority",
      "all_roles": \[
        "mint_authority"
      \],
      "primary_section_anchor": "section-bridge-mint"
    },
    "0xa73072adc6c34859426fcc29bc6ca2cac07c93c3": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x278d858f05b94576c1e6f73285886876ff6ef8d2": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x1b5c6800daacb36a43c94378fcdc5d18e8f5e6e1": {
      "primary_role": "mint_authority",
      "all_roles": \[
        "mint_authority"
      \],
      "primary_section_anchor": "section-bridge-mint"
    },
    "0xb300000b72deaeb607a12d5f54773d1c19c7028d": {
      "primary_role": "dex_pool",
      "all_roles": \[
        "dex_pool"
      \],
      "primary_section_anchor": "section-liq"
    },
    "0x708db14970c9079f64d552e8b3cf33525f0123d5": {
      "primary_role": "mint_authority",
      "all_roles": \[
        "mint_authority"
      \],
      "primary_section_anchor": "section-bridge-mint"
    },
    "0x5528cf58feb8fbfce94f43b33240fffb1312bde3": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xc198c465d875f8d762f1b166341c5c0fdefe09b3": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xfad20e2b1828168fc8147417bb89519dc1d6e664": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xb891cc3b4271e85644c4e871e16c650ecc71d5b0": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x17abbbcdccb8cb4a0d41203be83220f35548499b": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x1fb7b61bfcc506153220753847fd05e80718e3e1": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x62ccef0b4545166f721caa9fee13c1d3767e27dc": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xa017609fa051e4f0e76802a926fd780f587db0fa": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x982385d229082d390d4fb942d28eb728e8f42c33": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x031942f26a094be40414f442a2f1295e3a5c1680": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x3159fc5ed978688b451c854895dc24d67e02bab8": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x653dd7677aea3030eab68c97ed3594bacf560158": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x73b4c818892283e5fc37fee7b91ff7245b236d3c": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x2c61ee89e44ae920f3310fe080865d220a1b777c": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x9a13a9fac1644f02890a326d0fbef08302cb89e1": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x208633b825abf7b0c2a1ccea7dbdfc37d0d5a325": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x5c6cd93855695f04bb72102d9fc4904166c5c15a": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x9c2bf15cc69740effef5717072a3d00f04afdf66": {
      "primary_role": "mint_authority",
      "all_roles": \[
        "mint_authority"
      \],
      "primary_section_anchor": "section-bridge-mint"
    },
    "0xa48fc1f847bd50a99ab473ad5f09c9515312800b": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x3e0a64501a8981842dc1d722ad6cbcf816aabd1a": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xd4ade84d1e4b1015a5dda8eb6c43858a3ac905f5": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x47bdf280e1b247583e11a06f7d7b17b49af5d560": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x60b97709d633dd4e0f0f44f6102fd50341c0afa6": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x15807ebb7c8f88fe784e965e5f0f2d637beaec8f": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x6984e749baf0faf6a2f6bffd940806abb495cb1c": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xe263d8702220ef358b3b6cd3af3960e296b8a25b": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x2f0cabba08a90d30382ee731f361198e7155dbb6": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x3b9345aa7765d0886384d91c422b7fb8eb276565": {
      "primary_role": "mint_authority",
      "all_roles": \[
        "mint_authority"
      \],
      "primary_section_anchor": "section-bridge-mint"
    },
    "0x80d9e531b5e091580df76ae505a3b8695c36ec0e": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x561a3a8f7c97b66248c8a343a2649301740ce7c5": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x4b1b2ea60cc20a171cb7eed8fe0de988f79651d2": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x6ee6462f65b922d5863bec36a3e6c2008be05291": {
      "primary_role": "mint_authority",
      "all_roles": \[
        "mint_authority"
      \],
      "primary_section_anchor": "section-bridge-mint"
    },
    "0xde9e4fe32b049f821c7f3e9802381aa470ffca73": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xf51a9efb3f8ed40e0f8bbd5de44b0bcdd4f2a98e": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xbe9ef2f063b15cff7f143b90bd4a80170e2258bd": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x13d8e224c3759a6e2c1f5f6c848dda2af3c489c4": {
      "primary_role": "mint_authority",
      "all_roles": \[
        "mint_authority"
      \],
      "primary_section_anchor": "section-bridge-mint"
    },
    "0x8c8b5293795d643d982dcbafc905d0645e9f8efb": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xe2569f956e37c071ea7de60eddd1e90d0f26929a": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x57fd714755dbe55798501e1b4b2bcc355c06bf6a": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x75f838dbf3be0a79d6e5904ab5c364d5418a5f66": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x54ec93dce3ef6e48dfa5895135dcfee2fa039260": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xbd2f3b1aabdb4910829a445afcda7175c457753e": {
      "primary_role": "mint_authority",
      "all_roles": \[
        "mint_authority"
      \],
      "primary_section_anchor": "section-bridge-mint"
    },
    "0x7817dbf38e9d1c95671625f0052c147864692fe0": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x2087d8fe927966fee758ba5563fb8f2347180b7c": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xe179dff7dc07729905c526f9d39c170a09dade09": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x1ea99b62efc93982b58e48d5bcd6ff931180fb5a": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x154cd934c93f21a4ba4e8ee8ec4b3cba4687259f": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x39682fff3f81cdbed0cdf9356c633f24ca47269a": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xb41ae9642f28f4657807004cac7b4b3a85291bca": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x143bb85e9314e97b55e61195bf0ed032e7291caa": {
      "primary_role": "mint_authority",
      "all_roles": \[
        "mint_authority"
      \],
      "primary_section_anchor": "section-bridge-mint"
    },
    "0x84eece394a096cd80f6e3386012ed5708440f844": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x088ca577f148a47da34ad3664f5c3cd5d0cc3986": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xb1f23a3fcc47905cce7e7ef0deae271855e914fa": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x628683c3c54ec4a22217d0022d0d442b391e9a4f": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x64f6902c232b2eadc731b316c0d7d0fa88d4ff7e": {
      "primary_role": "deployer",
      "all_roles": \[
        "deployer"
      \],
      "primary_section_anchor": "section-alloc"
    },
    "0x971435fc38eed5e0aaff0dd717d0d16a02a4110e": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x4bab2cb2ed6ee2d564ba5398cab4161d95e58f1b": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x0e91e407a3c8887b0713d9abf7695cb6efdc385c": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xc0d30004338aeb91e2c7fd49b9b16bd1ca4b9a62": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x0f694d8fa3c9c90f6c7ec43d3bb0e888d4c71840": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x7736a721ce90abdb8183f9cbe9e6f6b61c32cef2": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xbcab8296b6b596787132d8db0d3bbaa2cda365c7": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x4923d960f84d89e72c78daf82015b519aaafe994": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x6bf1d4368219d1126c9e971e07654ef415dc8229": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x1b7e4ca15a2fe5310a91d4754a67ea52a0a7dc03": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x73d8bd54f7cf5fab43fe4ef40a62d390644946db": {
      "primary_role": "public_cex_hot_wallet",
      "all_roles": \[
        "public_cex_hot_wallet"
      \],
      "primary_section_anchor": "section-monitoring"
    },
    "0x477ff94b9db530642b5818a69bd530325702da9a": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x000be4f551e7440b93ce9d2cc11979879147e19f": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xfc1221d10f967ed0ecf34a7f763d328d19d470a1": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x4c05e926ae3e427549aad4800865357f9b236c98": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xe4b5b2667e049ac8c79ae6c5a7e3300815aa32be": {
      "primary_role": "public_cex_hot_wallet",
      "all_roles": \[
        "public_cex_hot_wallet"
      \],
      "primary_section_anchor": "section-monitoring"
    },
    "0x11eacd2bedd700a5e21ff70dea4086305100e5e0": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xb733109fab29787268d504ce65e31892fab20262": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x346d25338f3cbd5a102011ca33a47d26b9400b90": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xe94753d6e067d25e0dbe90ed782b7ea21475fc48": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xf86aabe61b1df0f33dd09f3b7bf8232f3d01a904": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xd2cd331e493a325dd5634cfeb93852389c0aaece": {
      "primary_role": "dex_pool",
      "all_roles": \[
        "dex_pool"
      \],
      "primary_section_anchor": "section-liq"
    },
    "0xfea18be59b326917572fbb999410749b22f335bf": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x24d3857d80e915f98421248ab06530c7a39362f7": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xbd97306a087ed0c46b783cfbfdcdc6c12c7a2866": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x4812bb70890de10615b2dab53f1564ac5a07922c": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x1231deb6f5749ef6ce6943a275a1d3e7486f4eae": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x6aba0315493b7e6989041c91181337b662fb1b90": {
      "primary_role": "public_cex_hot_wallet",
      "all_roles": \[
        "public_cex_hot_wallet"
      \],
      "primary_section_anchor": "section-monitoring"
    },
    "0xcc3fc06d4057ad0c28c9ffb32563387d97f0fa61": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x08ae6a310785979f167f6f1a12e665ba5aab2486": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x05cb186ab8ec85378a2cbf8a858568a8fb216b07": {
      "primary_role": "public_cex_hot_wallet",
      "all_roles": \[
        "public_cex_hot_wallet"
      \],
      "primary_section_anchor": "section-monitoring"
    },
    "0xd8b1bf348f5848c35b9ed8175dfa843f06a98c53": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x2eeb0fcfe9eac2a8d2c9578b5b31af2eb000f486": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x111111125421ca6dc452d289314280a0f8842a65": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x084aeb64cfe9e89d9cfe6f3f82378d63eaa5f430": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xe0881cc50de6a472cd340111e80d70b79d807ac1": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xf91e8bf46b9e90909e53c82353c833bb4a5e3a45": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x6e4141d33021b52c91c28608403db4a0ffb50ec6": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x6b3affc894b0d2d566e5ff03ad79188f1b65bfff": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x2c730d9b00135627f1d34f3546f15ecaa9a7f52e": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x6cd1b8cfcd2ca2bcdb46a2d96bd22b92e16ba427": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xb05eb667d42eb31e0c814384f1ac2c8428166420": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x63242a4ea82847b20e506b63b0e2e2eff0cc6cb0": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x9999b0cdd35d7f3b281ba02efc0d228486940515": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xec70c076ed9d5d4ffb8bc09094b9a251f239d0c2": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0xb89da1c54923c888146bbf00a89e462e8e4562df": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x0501f595d17dd90ff11a9873692ee3f8d478f4e5": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x3156020dff8d99af1ddc523ebdfb1ad2018554a0": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x144d395b5562c742259932d2ee6e1d8d092a21b8": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x2aa6845f7e84b2cc1619c823bf4f6b04ec733f2c": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x42407fb33b3487fd7b644d84f35818a63e22b03c": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x6b080b294bfb2d908595e12068c8d054f58f9a76": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x3d2bb7e9df6b49b82ec75214aea8feddab78fc5f": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    },
    "0x2ad99fcfe69248561bf5f0eb788af5217afaaa29": {
      "primary_role": "high_throughput_operator",
      "all_roles": \[
        "high_throughput_operator"
      \],
      "primary_section_anchor": "section-high-throughput"
    }
  }
}
```

---

****仅数据研究, 非投资建议. evidence_graph 包含 299 个稳定 ID 用于 provenance 追溯.****
