# SOL_MEME (Solana meme 9cRCn9...pump) — 链上决策简报

> ⚠️ **主链可能不在覆盖范围 (镜像切片警告)**: 本 token 在 solana 也有部署 — 该链不在本工具的转账级链上 forensic 覆盖范围内, 这部分的真实持仓/派发/出货本报告看不到。若 solana 才是该 token 的主战场 (Alpha 上市链 Solana 仅为镜像端), 则本报告仅覆盖镜像切片、风险评估不完整 — 下方结论与 verdict 仅基于 Solana 侧数据, 不代表 token 全局。
> ⚠️ **实时行情未就绪**: surf `project-detail` 与 Binance Alpha API 两边都未返回此 token 的实时价格. 下方"代币行情"表跳过. 临时核对走链上浏览器 + 主池地址.

> ℹ️ **Solana 链 链上侦测 覆盖说明**: surf 的 `onchain-sql` 当前**不覆盖** Solana 链
> (`agent.solana_transfers` / `_dex_trades` 表不存在;
> surf 仅在 BSC / Ethereum / Arbitrum / Base / Polygon / Optimism 提供链上 SQL).
> 本报告**已自动跳过**以下 链上侦测 段, 它们依赖 surf SQL transfers 表:
> - 上线前内幕分发追溯 (Rule 11 合约部署地址 trace)
> - 真实派发卖出量化 (dump_tracker top sellers)
> - 近 72h 异常大单 (异常 转账 SQL)
> - 对敲配置检测 (wash_infra 检测器)
> - LP 24h 净流 + LP 创建时刻 (lp_24h_flow / TGE first-trade SQL)
>
> **保留**: Alpha API 实时行情 (价/vol/mcap/FDV/持币人 数), surf `token-持币人` (top-50 持仓 + Arkham 标签), section_alloc, monitoring_paste 导出.
>
> **手工核对**: 走 Solscan / Birdeye / DEX Screener 看深度 + 持币人 分布; 用 Helius / Shyft API 拉 SPL Token Program 的 mint / 转账 instruction.
_工具版本 1.2.6 · 主链 Solana · Alpha 上线 N/A_

_总供应 999,991,818 · 流通 999,991,818 (100.0%) · 类型 MEME_LIKELY_
_等级 S1 · S1 —_

## 📋 决策摘要

| 项目 | 取值 |
|---|---|
| **🎯 风险评分** | **⬜⬜⬜⬜⬜⬜⬜⬜⬜⬜ (0/10)** |
| **链上状态标签** | **无显著触发** — 无显著 链上侦测 触发信号 |
| 主战场链 | solana |
| **进场上限 (LP 5% 深度)** | **—** |
| 短期催化 | 无 |
| 必须自行 交叉核对 的盲区 | Solana meme fallback: surf onchain-sql is unavailable; holder snapshot uses surf token-holders REST.; 主战场 solana 的链上 SQL 不在 surf 覆盖, forensic SQL 段全部跳过, 仅保留 Alpha 实时 + token-holders 快照 |

> 🎯 **5 档链上状态标签含义** (渲染端 确定性 推导, 仅描述链上侦测 状态, 非交易建议):
> - **无显著触发** — 无显著链上侦测触发信号 (风险 0-2)
> - **观察中** — 部分异动但未触发主信号 (风险 2-5)
> - **派完离场** — 历史庄家已派完, 链上历史抛压已释放 (风险 4-7)
> - **潜伏内幕未派** — 潜伏内幕钱包未分发, 时点不可预测 (风险 6-9)
> - **近期派发** — 近 72h 大额链上活动 (风险 7-10)

> 当前建议按观察处理：这份 SOL meme 报告已经能识别链、供应量和覆盖范围，但价格、主池深度、持仓明细与历史转账证据不足，不适合据此直接放大仓位。



## 🎯 链上状态: 无显著触发 (风险评分 0/10)

**无显著 链上侦测 触发信号**


| 决策锚点 | 数值 | 状态 |
|---|---|---|
| Alpha 5% 撤单上限 | 未知 | 🔴 超薄 |
| DEX 主池 USD 流动性 | — | 🔴 |
| 池子代币 24h 净进出 (throughput, 非 LP 增减) | — | 🟢 |


## 🧠 当前链上行为画像

> ℹ️ **未触发任何主要行为画像** — 10 个 链上侦测信号 检测器 都返回 OFF. 这通常出现在: (a) Solana / 非 EVM 链 中止 (surf 无 SQL 覆盖); (b) 新发未上线 token (data 不足); (c) 真正清白的 token. 配合上方 🎯 链上状态判断 + 顶部 链上侦测限制 提示条 综合看.


## 🔴 真实派发 (内幕 确认卖出下界)

### 🎯 拉盘对手盘验证

> **⚡ 速读**: 流通 1000.0M tokens · **非庄家方抛压 100.0%** (999,991,818 tokens = 前 100 大持币人内可验证 0.0% + 尾部 ~100.0%) · 庄家弹药 0.0% (⚠️ Alpha API 报流通 1000M, 链上可砸盘 1000M = 0.00x, Alpha 高估 (含 mint authority / vesting 锁仓)) · 中转·流动性池 (CEX 充值 + DEX 池, 庄家加池 vs 散户交易不可分) 0.0% (0 个交易所/DEX 池) · 内幕已确认变现 $0 (占流通 0.0%) ⚠️ **detector 未识别庄家卖出** — 链上 net 卖出 = 0 是 detector 阈值未达 (mining_fed / mint_authority / m6 insider DEX swap 都没 capture), 不代表真无卖出, 实际看 funding_attribution + 24h vol 段.

> ⚠️ **三桶 sanity check 触发** — 以下桶 ≈ 0%, 主动排查:
> - **庄家弹药 0%**: 罕见 — Alpha 类 token 通常有项目方控. 排查: (a) `_master_cluster_addrs` 是否空 (应 ≥ 50)? (b) m6 / mint_authority / cex_fanout / ht_dumpers detector 是否 run? (c) 检查 funding_attribution segments
> - **中转·流动性池 0%**: BSC 主流 Alpha token 通常都进 Binance/Gate/Bitget. 排查: (a) surf top_holders cex category 是否空? (b) cex_hot_wallet labels 是否完整 (Arkham)? (c) cex_fanout hubs 检测到的 CEX source addresses 应进 cex_pool
> 庄家想 pump 时, **可能砸盘的对手 = 现持有筹码里不属于庄家的部分**. 这部分越小, 庄家越敢拉 (拉了不怕被砸); 越大越有顾忌.

| 筹码桶 | 代币数 | 占当前流通 | 解读 |
|---|---:|---:|---|
| 🟣 **庄家 / 项目方可控筹码** | **0** | **0.0%** | **分散** — 项目方足迹不明显 |
| 🔥 **可验证非庄家方抛压** | **999,991,818** | **100.0%** | **外部抛压较重** (含散户大户 + 协议合约 + 跨链桥中转) |
| 🟦 **中转·流动性池 (CEX + DEX, 中性·不可分)** | **0** | **0.0%** | 0 个交易所热/冷/充值钱包. 链上**无法区分**散户充值聚合 vs 项目方托管储备. 拉盘时可能从两边都流出 |

### 关键判断

**项目方可控筹码 < 50%** — 控盘不强, 看外部对手盘 + CEX 池流向决定盘面.

<details>
<summary>🔍 展开: 庄家弹药 11 子桶明细 (含 raw 加总 + 重叠说明)</summary>

| 子桶 | 代币数 | 占流通 | 说明 |
|---|---:|---:|---|
| ①a 公开锁仓 / 国库 / 空投合约 m6 谱系外 | 0 | 0.0% | Sablier / Hedgey / 自定义锁仓. 有公开释放时间表, **拉盘时不会立刻砸**. 减未流通储备 0 后的下界 |
| ①b 多签可机动 m6 谱系外 | 0 | 0.0% | Gnosis Safe Proxy 等. 项目方一签今天就能转 |
| ② m6 谱系流通中部分 | 0 | 0.0% | m6 谱系总持仓 0 减锁仓 0. 含纯内幕 (0) |
| ⚠️ ③ 交易所提币分发 (净控筹不可算) | — | — | gross 流入, phase2 SQL 截断, 净 fanout 算不出.  |
| ━━━━━ | ━━━━━ | ━━━━━ | ━━━━━ |
| 庄家弹药 raw 加总 | 0 | 0.0% | 各桶加总假设不重叠. 上界估算 |

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
| ━━━━━━━━━━━━━━━━━ | ━━━━━━━━━━━━━━━━━ | ━━━━━━━━━ | ━━━━━━━ | ━━━━━━━━━ | ━━━━━━━━━ |
| **合计可验证非庄家方抛压 (前 100 大持币人内)** | 0 个钱包 | **0** | **0.0%** | — | — |

> ⚠️ **非庄家方抛压性质判断**: 主要含真散户大户 + Wormhole / veVELVET 等协议合约 (用户存的) + 跨链桥中转. 大额裸地址 (没 Arkham 标 + > 1% 流通) 是项目方化名 vs 真散户大户 嫌疑 — 到下方 monitoring_paste 手动核对钱包活动.

---

| 项目 | 取值 |
|---|---|
| 追踪钱包数 | **0** (0 标准内幕; 矿币 / 跨链桥 token, 无 pre-launch m6 谱系) |
| 内幕树当前持有 (含锁仓, 守恒锚) | 0.0000% 总供应 (0 tokens, 含未解锁锁仓 + CEX/DEX 中转余额, **不等于 内幕 掌控数字**) |
| (a) 确认卖出 — CEX 充值 | 0 |
| (b) 确认卖出 — DEX swap (本钱包) | 0 (0 笔) |
| **确认毛卖出, a+b** | **≥ 0 (流通占比未知)** |
| **确认净卖出** | **无法 reliably 估算** — 矿币 / 跨链桥 token m6 谱系空, dump_tracker 不跑 net 算法. 参考: ht_dumpers 100 钱包总 **过账** 0 tokens (= 0.0x 流通) 含**大量对敲 wash 不全是 sell**. 真实卖出 < throughput, 可能在 0.1-0.5x 流通量级, 但 dependent 项目方 wash 程度 |



> ⚠️ **确认卖出不完整**: CEX/DEX 确认查询在 surf 多次重试后仍失败或当前链不在覆盖范围, 上面可能更低估. 建议重跑或到链上浏览器手工核对.


<a id="section-recent-anomaly"></a>
## 📊 风险信号聚合 (检测器 + 节奏)

### 检测器汇总

| emoji | 类别 | 数量 | 解读 |
|---|---|---|---|
| ⚪ | 上线前内幕分发 | 0 | Rule 11 上线前分发追溯未在 Solana 模式运行，因此没有 deployer 到内幕接收方的完整路径证据。 |
| ⚪ | 已分完内幕钱包 | 0 | 近期异常转账检测缺少 Solana transfers SQL 表，不能确认最近是否存在连续大额转出。 |
| ⚪ | 潜伏钱包 (未分发) | 0 | CEX 入金与真实派发链路没有可用 SQL 证据，Binance 行情侧也未给出可执行的新增催化剂。 |
| ⚪ | 近 72h 异常大单 | 0 | 对敲、跨币大户和清仓过账类检测均因 Solana SQL 覆盖缺失跳过，报告只保留快照级判断。 |

### 节奏识别

**Solana 快照覆盖不足，未形成可验证异常节奏**



<details>
<summary>📂 <strong>📊 完整异动事件列表 (数据明细, 按分发轮次, UTC 时间)</strong> — 共 0 波分发, 合计 0 笔事件 (click 展开看完整时间表 + 钱包流向)</summary>


</details>


## 主战场链

| 项目 | 取值 |
|---|---|
| **主战场链** | **solana** (单链, 无 BSC 镜像; Binance Alpha 以 SPL token 直接挂) |
| 铸造链 | solana, totalSupply 999,991,818 |
| 交易链 | solana (Alpha + DEX 主池) |
| 跨链分布 | **单链 solana** — Alpha 直接挂 SPL token, 没有 BSC / EVM 镜像桥; 本报告仅 持币人 snapshot + Alpha 实时, **不**包含 链上侦测 SQL 段 |
| 报告覆盖范围 | **HOLDER_SNAPSHOT (主链 solana)** — surf 不覆盖 solana 的 `onchain-sql` (无 `agent.solana_transfers` 表), 全部 链上侦测 SQL 段已跳过; 保留 Alpha 实时行情 + surf token-持币人 REST + monitoring 导出 |

⚠️ 主链 solana 走 HOLDER_SNAPSHOT 模式 — surf onchain-sql 不覆盖该链, 链上侦测 SQL 段全部跳过. 实时行情 / 持币人 / mcap / FDV 等 REST 数据正常拉取. 内幕谱系 / 对敲 / 流水大户 / 跨币 4 类 SQL 检测**无数据**, 顶部 提示条 已说明; 用 Solscan / Helius / Shyft / Vybe 手工核对

**解读**: 该 CA 被识别为 Solana 单链 SPL token，报告走 HOLDER_SNAPSHOT；EVM 版内幕谱系、真实派发、对敲和跨币 SQL 检测都不适用。

## 入场价 锚点

| 时间锚点 | UTC | 价格 | 相对当前 |
|---|---|---|---|
| LP 创建首笔 (DEX 启动) | — | — | — |
| Alpha 上线首笔 | — | — | — |
| **当前价** | 2026-06-29 | — | 1.00× |

**解读**: LP 创建价、Alpha 首笔价和当前价都缺失，因此不能计算当前相对开盘的倍数；价格判断需要外部实时盘口补齐。

<a id="section-alloc"></a>
## 项目方话语权

| 项目 | 取值 | 来源 |
|---|---|---|
| Alpha 配额比例 (官方披露) | **未披露** | Binance Alpha 官方接口当前未给出该字段 |
| 项目方钱包 `—` 当前余额 | 未知 | 项目方分发追溯 |
| 上线前内幕接收方 0 个累计余额 | 0 tokens (= 0.00% 总供应) | 内幕钱包累计 |
| 潜伏钱包 0 个持仓 (核心未来风险) | **0 tokens (= 0.00% 总供应 / $—)** | 未分发内幕钱包 |
| 已分完内幕钱包 0 个 (分发完成) | 已 100% 分完, 剩余 0 | 已转出 ≥95% 的内幕钱包 |

**解读**: Alpha 配额未披露，上线前内幕接收方也没有 SQL 追溯结果；这里不能证明项目方筹码少，只能说明本模式没有捕获到可核验分发。

## 短期上 CEX 催化剂

| 交易所 | 状态 | 时间 | 距今 |
|---|---|---|---|
| Binance | 未上线 | — | — |
| Aster | 未核实 | — | — |
| Bitget | 未核实 | — | — |

无 14 天内新催化剂. 当前 S1 (Alpha only).

**解读**: Binance 行显示未上线，Aster 与 Bitget 未核实，近期没有形成可执行的 CEX 催化剂证据。

<a id="section-liq"></a>
## 进场上限

| 锚点 | 取值 | 备注 |
|---|---|---|
| **不超 5% 滑点的最大单笔买入 (估算)** | — | 由 Alpha 24h vol 推导 (vol_24h / 96 × 0.05 启发式估算) |
| DEX 主池流动性 | — | 无主池 |
| DEX 主池 24h 交易量 | — | surf project-detail (跨链 CEX+DEX 实时聚合) |
| 池子代币 24h 净进出 (throughput, 非 LP 增减) | — | surf 不覆盖 (chain SQL 表不存在), 见顶部 Solana banner |
| DEX 主池地址 | — |  |

**解读**: 没有 Alpha 24h 成交量和 DEX 主池流动性时，不能给出不超过 5% 滑点的买入上限；任何买入都要先用外部盘口重新估算容量。

<a id="section-holdings"></a>
## 各角色持仓分布

**持仓分布表**:

| 角色 | 钱包数 | 当前持仓 | 占总供应 % | Top 钱包 |
|---|---|---|---|---|
| DEX 主池 | 0 | 0 | —% | — |
| 项目方钱包 | 0 | 0 | —% | — |
| 潜伏钱包 (内幕未分发) | 0 | 0 | —% | — |

**关键解读**:
- 内幕追踪 **0** 钱包累计持 **0.0%** 总供应  (矿币 / 跨链桥 token, 无 pre-launch m6 谱系).
- insider 已链上确认流出 **0.0M USD** = **0.00%** 流通, 用内幕自卖 TWAP 计价 (非 wash 报价).

<details>
<summary>📂 <strong>上溯发现 (项目方钱包 → 内幕谱系)</strong> — 0 个内幕钱包: 0 已分完 / 0 分发中 / 0 潜伏 (click 展开看完整谱系 + 钱包余额 + 派发率)</summary>

**内幕钱包列表 (项目方分发追溯)**:

| 编号 | 地址 | 收自项目方 | 当前持仓 | 已分 % |
|---|---|---|---|---|
_统计 (m6 谱系全集 **0** 个): 0 持仓接近 0 / 公开锁仓 custody · 0 分发中 · 0 已分完_

**m4_notes (LP 前预分配解读)**:
- 当前没有可验证的上线前分发链路，Solana 模式下不生成 deployer 到接收方的 M4 钱包列表。
- Solana HOLDER_SNAPSHOT 模式没有跑上线前 deployer 到接收方的 SQL 追溯，所以这里不把 0 个内幕钱包解释成项目方完全干净。
- 当前能确认的是 SPL 总供应约 999,991,818 枚；上线前分发、二级接盘和转出路径需要 Solscan 或专业 Solana 索引补查。



</details>

## 💰 高价值地址资金来源 (mint / DEX / P2P)

下面是 对敲配置 / 流水大户 / m6 内幕 / Top-30 持币人 段里已经标记过的高价值地址, 按 365 天内**收到的 token 来源**分类: mint (从 0x0 直接铸造, 矿币 / 跨链桥 / 空投 mint 合约都算) / DEX 买入 (从已知 DEX 主池买入) / P2P (其他 EOA 转账, 包含未识别的 CEX 提现). 用来判断: ⛏️ Mint 占比高 = 矿币 / 跨链桥 token 操作员或挖空投的 马甲钱包; 🟢 DEX 占比高 = 真买盘 散户 持仓; 🔵 P2P 占比高 = 操作员归集 / OTC 接收.

> ⏭️ **资金来源段已跳过** — surf_no_sql_solana.


<a id="section-monitoring"></a>
## 监控钱包 + 实时告警


> 📊 **监控优先级 (v0.7.27 确定性 ranker)**: 🚨 0 CRITICAL · 🔥 0 HIGH · 👀 0 NORMAL>
> paste.json 里钱包已按等级排序, 🚨 在最前. 优先盯 CRITICAL+HIGH (0 个), 这些钱包动 = 改变链上侦测 判断. NORMAL (0 个) 做批量 交叉核对, 不需要 push notification. 💤 NOT_TRACKED 是 DEX 路由 / 公共 CEX 热钱包, 流量噪音淹没真信号, 已从 paste 剔除.


| # | 等级 | 钱包 | 角色 | primary 角色段 | 触发条件 | 状态 |
|---|:-:|---|---|---|---|---|

本轮未导出可直接粘贴监控的钱包。实际交易前应先补 Solscan / GMGN / OKX 钱包的 top holder 和 LP 池监控，再做仓位决定。

## 机器可读 JSON (精简)

```json
{
  "schema_version": "1.2.6",
  "symbol": "SOL_MEME",
  "verdict": "ADVISORY",
  "verdict_zh": "观察",
  "verdict_downgrade_applied": 0,
  "chain_state": "CLEAN",
  "chain_state_label": "无显著 链上侦测 触发信号",
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
    "holdings_role_rows": 3,
    "holdings_progress_bars": 3,
    "monitoring_wallets": 0,
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

****仅数据研究, 非投资建议. evidence_graph 包含 0 个稳定 ID 用于 provenance 追溯.****
