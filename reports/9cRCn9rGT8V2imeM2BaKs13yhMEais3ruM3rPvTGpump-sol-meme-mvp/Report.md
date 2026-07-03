# SOL_MEME (SOL_MEME) - Solana meme 链上速查报告

_生成时间 2026-06-29 23:51:49 UTC · 模式 sol_meme MVP · 数据源 GMGN CLI_

## 一屏结论

| 维度 | 结论 | 证据 |
|---|---|---|
| 当前阶段 | 数据源不可达 | 风险评分 N/A |
| 市值/流动性 | $0 / $0 | holders - |
| 筹码集中 | top10 0.00% | top holder 快照 0 个 |
| MM/做市地址 | 0 个候选 | confirmed/strong/weak 分层输出 |
| 派发/套现 | 0 个候选 | top traders 卖出额下界 $0 |
| 异动地址 | 0 个候选 | 输出监控 0 个 |

## 速读摘要

- **数据缺口**: GMGN 部分接口当前不可达，以下结论只基于成功返回的数据，不能当完整取证。
- **代币**: `9cRCn9rGT8V2imeM2BaKs13yhMEais3ruM3rPvTGpump`，价格 `-`，市值约 $0，流动性约 $0。
- **MM/做市**: 识别到 0 个候选地址；confirmed 代表 GMGN/bot 标签，strong 代表高成交低库存等行为特征。
- **派发/套现**: top traders 可见卖出额下界约 $0，买入额约 $0；这不是全链真实套现总额，只是 GMGN 返回样本下界。
- **异动监控**: 已导出 0 个地址，可优先盯大额卖出、疑似 MM、suspicious、bundler/rat/sniper 类地址。

## 安全与权限

| 项目 | 值 |
|---|---|
| Mint renounced | - |
| Freeze renounced | - |
| Rug ratio | - |
| Top10 holder rate | 0 |
| Wash trading | - |
| Sniper count | - |
| Smart/KOL wallets | 0/0 |

## MM / 做市候选地址

未识别到足够强的 MM/做市候选；如果 GMGN traders 接口失败，这里会天然低估。

## 派发 / 套现候选

未识别到明确派发/套现候选；这不代表没有出货，只代表当前数据样本未命中。

## 异动地址

未识别到显著异动地址。

## Top holders 快照

holders 接口没有返回数据。

## 数据缺口

- info: [gmgn-cli] GET /v1/token/info fetch failed: ConnectTimeoutError: Connect Timeout Error (attempted address: openapi.gmgn.ai:443, timeout: 10000ms)
- security: [gmgn-cli] GET /v1/token/security fetch failed: ConnectTimeoutError: Connect Timeout Error (attempted address: openapi.gmgn.ai:443, timeout: 10000ms)
- pool: [gmgn-cli] GET /v1/token/pool_info fetch failed: ConnectTimeoutError: Connect Timeout Error (attempted address: openapi.gmgn.ai:443, timeout: 10000ms)
- holders: [gmgn-cli] GET /v1/market/token_top_holders fetch failed: ConnectTimeoutError: Connect Timeout Error (attempted address: openapi.gmgn.ai:443, timeout: 10000ms)
- traders: [gmgn-cli] GET /v1/market/token_top_traders fetch failed: ConnectTimeoutError: Connect Timeout Error (attempted address: openapi.gmgn.ai:443, timeout: 10000ms)

## 方法边界

- 本报告不等同于 Binance Alpha EVM forensic；Solana 的 MM/派发/套现判断以 GMGN 标签和行为特征为主。
- DEX 卖出额是样本下界，不包含链下 OTC、CEX 内部账本、跨钱包后续兑换。
- 下一阶段需要接 Helius/Shyft/Vybe 解析 SPL transfer、Jupiter/Raydium/Meteora inner instructions，才能接近完整派发链。
