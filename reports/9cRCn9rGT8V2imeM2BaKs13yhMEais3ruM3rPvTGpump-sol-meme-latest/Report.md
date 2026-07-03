# ANSEM (The Black Bull) - Solana meme 链上速查报告

_生成时间 2026-07-01 04:56:35 UTC · 模式 sol_meme MVP · 数据源 GMGN CLI_

## 一屏结论

| 维度 | 结论 | 证据 |
|---|---|---|
| 当前阶段 | 疑似 MM/机器人主导 | 风险评分 7/10 |
| 市值/流动性 | $123.14M / $1.33M | holders 76436 |
| 筹码集中 | top10 63.24% | top holder 快照 100 个 |
| MM/做市地址 | 142 个候选 | confirmed/strong/weak 分层输出 |
| 派发/套现 | 196 个候选 | top traders 卖出额下界 $5.57M |
| 异动地址 | 225 个候选 | 输出监控 16 个 |

## 速读摘要

- **代币**: `9cRCn9rGT8V2imeM2BaKs13yhMEais3ruM3rPvTGpump`，价格 `0.12314538`，市值约 $123.14M，流动性约 $1.33M。
- **MM/做市**: 识别到 142 个候选地址；confirmed 代表 GMGN/bot 标签，strong 代表高成交低库存等行为特征。
- **派发/套现**: top traders 可见卖出额下界约 $5.57M，买入额约 $8.59M；这不是全链真实套现总额，只是 GMGN 返回样本下界。
- **异动监控**: 已导出 16 个地址，可优先盯大额卖出、疑似 MM、suspicious、bundler/rat/sniper 类地址。

## 安全与权限

| 项目 | 值 |
|---|---|
| Mint renounced | True |
| Freeze renounced | True |
| Rug ratio | - |
| Top10 holder rate | 0.6324 |
| Wash trading | - |
| Sniper count | - |
| Smart/KOL wallets | 88/46 |

## MM / 做市候选地址

| 地址 | 置信度 | 持仓% | 买入额 | 卖出额 | 交易数 | 理由 |
|---|---|---:|---:|---:|---:|---|
| `D3dGSy...qEm8` | confirmed | 0.05% | $487,777 | $462,522 | 135 | GMGN/bot 标签命中, 高频成交且低库存, 买卖量接近平衡，疑似做市/刷量 |
| `3CPHk5...FkWY` | confirmed | 0.07% | $367,442 | $549,651 | 135 | GMGN/bot 标签命中, 高频成交且低库存, 买卖量接近平衡，疑似做市/刷量 |
| `99Zbto...btt1` | confirmed | 0.04% | $222,121 | $287,025 | 220 | GMGN/bot 标签命中, 高频成交且低库存, 买卖量接近平衡，疑似做市/刷量 |
| `9UUyxT...dxjT` | confirmed | 0.05% | $184,641 | $180,078 | 81 | GMGN/bot 标签命中, 高频成交且低库存, 买卖量接近平衡，疑似做市/刷量 |
| `H3qrST...Bxj1` | confirmed | 0.31% | $871.62 | $329,810 | 271 | GMGN/bot 标签命中, 高频成交且低库存 |
| `3MZvE3...MgKN` | confirmed | 0.04% | $157,930 | $106,339 | 153 | GMGN/bot 标签命中, 高频成交且低库存, 买卖量接近平衡，疑似做市/刷量 |
| `9aP2vS...SR5T` | confirmed | 0.12% | $7,720 | $250,004 | 92 | GMGN/bot 标签命中, 高频成交且低库存 |
| `78thMY...oMDM` | confirmed | 0.08% | $49,503 | $187,840 | 61 | GMGN/bot 标签命中, 高频成交且低库存 |
| `3inTyf...rTg2` | confirmed | 0.30% | $181,296 | $32,715 | 58 | GMGN/bot 标签命中, 高频成交且低库存 |
| `GmCqxJ...BCoD` | confirmed | 0.08% | $74,284 | $119,524 | 320 | GMGN/bot 标签命中, 高频成交且低库存 |
| `C8HH76...D55Y` | confirmed | 0.23% | $150,052 | $38,392 | 50 | GMGN/bot 标签命中, 高频成交且低库存 |
| `2NCyVm...8HPy` | confirmed | 0.06% | $72,354 | $114,642 | 215 | GMGN/bot 标签命中, 高频成交且低库存 |
| `AHjQMx...pmxT` | confirmed | 0.08% | $95,682 | $83,836 | 166 | GMGN/bot 标签命中, 高频成交且低库存 |
| `4hSXPt...upzD` | confirmed | 0.14% | $59,109 | $99,437 | 186 | GMGN/bot 标签命中, 高频成交且低库存 |
| `As7HjL...SMB5` | confirmed | 0.00% | $58,105 | $93,523 | 115 | GMGN/bot 标签命中, 高频成交且低库存 |
| `ACTbvb...y831` | confirmed | 0.07% | $7,393 | $139,852 | 180 | GMGN/bot 标签命中, 高频成交且低库存 |
| `DedWto...sKDf` | confirmed | 0.04% | $28,690 | $106,922 | 69 | GMGN/bot 标签命中, 高频成交且低库存 |
| `9fnyoj...Usdj` | confirmed | 0.09% | $134,437 | $0 | 12 | GMGN/bot 标签命中 |
| `6Hcrxu...8UMg` | confirmed | 0.33% | $29,030 | $102,445 | 38 | GMGN/bot 标签命中 |
| `EMp115...utFB` | confirmed | 0.08% | $52,563 | $70,826 | 45 | GMGN/bot 标签命中 |

## 派发 / 套现候选

| 地址 | 持仓% | 买入额 | 卖出额 | 已卖比例 | 转出量 | 理由 |
|---|---:|---:|---:|---:|---:|---|
| `3CPHk5...FkWY` | 0.07% | $367,442 | $549,651 | 89.96% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `5URyNU...c19Y` | 0.17% | $9,886 | $502,508 | 82.76% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `D3dGSy...qEm8` | 0.05% | $487,777 | $462,522 | 91.14% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `2S8E25...RX7d` | 0.22% | $638,646 | $459,608 | 70.89% | 0.162774 | 卖出比例高，存在派发/兑现动作, 存在转出，不一定是卖出但代表筹码继续扩散, 带 insider/bundler 类标签 |
| `H3qrST...Bxj1` | 0.31% | $871.62 | $329,810 | 48.94% | 2.85M | 卖出比例高，存在派发/兑现动作, 存在转出，不一定是卖出但代表筹码继续扩散 |
| `99Zbto...btt1` | 0.04% | $222,121 | $287,025 | 87.39% | 10,707 | 卖出比例高，存在派发/兑现动作, 存在转出，不一定是卖出但代表筹码继续扩散, 带 insider/bundler 类标签 |
| `HCgo8g...2uYC` | 0.33% | $202,038 | $263,112 | 39.44% | 25.00M | 卖出比例高，存在派发/兑现动作, 存在转出，不一定是卖出但代表筹码继续扩散 |
| `6btcCb...g5eT` | 0.12% | $0 | $261,754 | 84.06% | 0 | 卖出比例高，存在派发/兑现动作 |
| `9aP2vS...SR5T` | 0.12% | $7,720 | $250,004 | 91.03% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `8e9bkF...6qg6` | 0.14% | $14,186 | $241,950 | 70.63% | 0.094748 | 卖出比例高，存在派发/兑现动作, 存在转出，不一定是卖出但代表筹码继续扩散 |
| `8s2MNR...rmez` | 0.26% | $641,196 | $237,887 | 48.16% | 0 | 带 insider/bundler 类标签 |
| `LCTTbB...NiqX` | 0.09% | $274,513 | $231,878 | 71.25% | 715,632 | 卖出比例高，存在派发/兑现动作, 存在转出，不一定是卖出但代表筹码继续扩散, 带 insider/bundler 类标签 |
| `9H9HU7...C4AZ` | 0.23% | $368,148 | $212,614 | 76.98% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `3SdVtY...bgou` | 0.13% | $283,249 | $195,783 | 53.42% | 0 | 卖出比例高，存在派发/兑现动作 |
| `78thMY...oMDM` | 0.08% | $49,503 | $187,840 | 73.54% | 0 | 卖出比例高，存在派发/兑现动作 |
| `9UUyxT...dxjT` | 0.05% | $184,641 | $180,078 | 77.08% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `GfePXR...8Ew2` | 0.20% | $279,930 | $171,631 | 55.99% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `HQdFfm...fzeH` | 0.08% | $65,627 | $164,484 | 72.31% | 0 | 卖出比例高，存在派发/兑现动作 |
| `DAEdBm...CvHC` | 0.11% | $0 | $153,160 | 87.69% | 0 | 卖出比例高，存在派发/兑现动作 |
| `GA1G2w...9j4e` | 0.14% | $16,802 | $152,912 | 57.18% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `ACTbvb...y831` | 0.07% | $7,393 | $139,852 | 97.72% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `GmCqxJ...BCoD` | 0.08% | $74,284 | $119,524 | 91.04% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `APgKzZ...k8vD` | 0.14% | $63,168 | $115,624 | 91.19% | 2.77M | 卖出比例高，存在派发/兑现动作, 存在转出，不一定是卖出但代表筹码继续扩散, 带 insider/bundler 类标签 |
| `2NCyVm...8HPy` | 0.06% | $72,354 | $114,642 | 64.58% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `DedWto...sKDf` | 0.04% | $28,690 | $106,922 | 67.54% | 0 | 卖出比例高，存在派发/兑现动作 |

## 异动地址

| 地址 | 持仓% | 买入额 | 卖出额 | 利润 | 标签 | 理由 |
|---|---:|---:|---:|---:|---|---|
| `GV6UUm...dC52` | 58.66% | $48.47 | $0 | $76.35M | TOP1, bundler, top_holder, transfer_in | 高盈利地址, 关键标签地址 |
| `Ac9Y9Q...zSZM` | 0.95% | $2,030 | $0 | $2.08M | TOP3, top_holder, transfer_in | 高盈利地址 |
| `5URyNU...c19Y` | 0.17% | $9,886 | $502,508 | $1.02M | TOP35, bundler, transfer_in | 大额卖出, 高盈利地址, 关键标签地址 |
| `3CPHk5...FkWY` | 0.07% | $367,442 | $549,651 | $544,911 | TOP36, bundler, dex_bot, fomo | 大额卖出, 高盈利地址, 关键标签地址 |
| `CLM6E4...Kg1Q` | 1.06% | $130,830 | $515.28 | $1.23M | TOP2, bundler, top_holder, whale | 大额买入后仍持仓, 高盈利地址, 关键标签地址 |
| `2S8E25...RX7d` | 0.22% | $638,646 | $459,608 | $164,476 | TOP26, bundler, whale | 大额卖出, 高盈利地址, 关键标签地址 |
| `D3dGSy...qEm8` | 0.05% | $487,777 | $462,522 | $77,032 | TOP45, bundler, dex_bot, gmgn | 大额卖出, 高盈利地址, 关键标签地址 |
| `9aP2vS...SR5T` | 0.12% | $7,720 | $250,004 | $639,440 | TOP52, axiom, bundler | 大额卖出, 高盈利地址, 关键标签地址 |
| `8s2MNR...rmez` | 0.26% | $641,196 | $237,887 | $-47,678 | TOP17, bundler, fresh_wallet, whale | 大额卖出, 关键标签地址 |
| `9H9HU7...C4AZ` | 0.23% | $368,148 | $212,614 | $227,797 | TOP24, bundler, fresh_wallet, whale | 大额卖出, 高盈利地址, 关键标签地址 |
| `6btcCb...g5eT` | 0.12% | $0 | $261,754 | $521,596 | TOP58, transfer_in | 大额卖出, 高盈利地址 |
| `99Zbto...btt1` | 0.04% | $222,121 | $287,025 | $244,919 | TOP48, bundler, dex_bot, fomo | 大额卖出, 高盈利地址, 关键标签地址 |
| `6Hcrxu...8UMg` | 0.33% | $29,030 | $102,445 | $576,914 | TOP9, axiom, top_holder, transfer_in | 大额卖出, 高盈利地址 |
| `GA1G2w...9j4e` | 0.14% | $16,802 | $152,912 | $455,972 | TOP42, bundler, fomo, fresh_wallet | GMGN suspicious 标记, 大额卖出, 高盈利地址, 关键标签地址 |
| `LCTTbB...NiqX` | 0.09% | $274,513 | $231,878 | $119,133 | TOP83, bundler | 大额卖出, 高盈利地址, 关键标签地址 |
| `78thMY...oMDM` | 0.08% | $49,503 | $187,840 | $384,302 | TOP30, dex_bot, fomo, fresh_wallet | GMGN suspicious 标记, 大额卖出, 高盈利地址 |
| `APgKzZ...k8vD` | 0.14% | $63,168 | $115,624 | $442,513 | TOP46, bundler, transfer_in | 大额卖出, 高盈利地址, 关键标签地址 |
| `3SdVtY...bgou` | 0.13% | $283,249 | $195,783 | $119,914 | TOP48, whale | 大额卖出, 高盈利地址 |
| `HCgo8g...2uYC` | 0.33% | $202,038 | $263,112 | $93,057 | TOP8, fresh_wallet, top_holder, transfer_in | 大额卖出, 高盈利地址 |
| `HQdFfm...fzeH` | 0.08% | $65,627 | $164,484 | $323,065 | TOP91, fomo, whale | 大额卖出, 高盈利地址 |
| `5FGoPP...rp8V` | 0.30% | $1.05 | $100,181 | $430,900 | TOP12, fomo, transfer_in | 大额卖出, 高盈利地址 |
| `ACTbvb...y831` | 0.07% | $7,393 | $139,852 | $353,649 | TOP33, axiom, bundler, dex_bot | 大额卖出, 高盈利地址, 关键标签地址 |
| `9UUyxT...dxjT` | 0.05% | $184,641 | $180,078 | $122,254 | TOP42, bundler, dex_bot, gmgn | 大额卖出, 高盈利地址, 关键标签地址 |
| `GkdYWR...Atac` | 0.37% | $297,612 | $0 | $158,795 | TOP7, bundler, top_holder, transfer_in | 高盈利地址, 关键标签地址 |
| `4hSXPt...upzD` | 0.14% | $59,109 | $99,437 | $286,109 | TOP45, axiom, bundler, photon | 大额卖出, 高盈利地址, 关键标签地址 |

## Top holders 快照

| # | 地址 | 持仓% | 余额 | USD | transfer-in | 标签 |
|---:|---|---:|---:|---:|---|---|
| 1 | `GV6UUm...dC52` | 58.66% | 586.62M | $72.22M | True | TOP1, bundler, top_holder, transfer_in |
| 2 | `CLM6E4...Kg1Q` | 1.06% | 10.63M | $1.31M | False | TOP2, bundler, top_holder, whale |
| 3 | `Ac9Y9Q...zSZM` | 0.95% | 9.50M | $1.17M | True | TOP3, top_holder, transfer_in |
| 4 | `FnzKY6...L3CC` | 0.54% | 5.38M | $662,158 | False | TOP4, top_holder |
| 5 | `8wLPuP...33m4` | 0.52% | 5.20M | $640,354 | True | TOP5, top_holder, transfer_in |
| 6 | `HDixbr...XN3o` | 0.38% | 3.80M | $467,838 | True | TOP6, fomo, top_holder, transfer_in |
| 7 | `GkdYWR...Atac` | 0.37% | 3.71M | $456,523 | True | TOP7, bundler, top_holder, transfer_in |
| 8 | `HCgo8g...2uYC` | 0.33% | 3.30M | $406,884 | True | TOP8, fresh_wallet, top_holder, transfer_in |
| 9 | `6Hcrxu...8UMg` | 0.33% | 3.30M | $406,381 | True | TOP9, axiom, top_holder, transfer_in |
| 10 | `F5hkYs...xqs6` | 0.32% | 3.23M | $397,441 | True | TOP10, bundler, fomo, top_holder |
| 11 | `H3qrST...Bxj1` | 0.31% | 3.11M | $383,031 | True | TOP11, axiom, top_holder, transfer_in |
| 12 | `5FGoPP...rp8V` | 0.30% | 3.03M | $373,416 | True | TOP12, fomo, transfer_in |
| 13 | `ASTyfS...iaJZ` | 0.30% | 3.02M | $372,394 | False | TOP13 |
| 14 | `6e7V9e...rvpN` | 0.30% | 3.00M | $368,750 | False | TOP14, fresh_wallet |
| 15 | `G6sYuV...iSFX` | 0.30% | 2.97M | $366,194 | True | TOP15, bundler, transfer_in, whale |
| 16 | `3inTyf...rTg2` | 0.30% | 2.96M | $364,768 | False | TOP16, bundler, padre |
| 17 | `8s2MNR...rmez` | 0.26% | 2.64M | $325,339 | False | TOP17, bundler, fresh_wallet, whale |
| 18 | `3J9Sq1...Fdxb` | 0.26% | 2.62M | $322,902 | False | TOP18, bundler |
| 19 | `8MHU3N...JP7b` | 0.26% | 2.61M | $321,358 | False | TOP19, bundler, whale |
| 20 | `6T8Var...WW6N` | 0.24% | 2.41M | $296,171 | True | TOP20, bundler, fomo, fresh_wallet |

## 数据缺口

- GMGN 基础接口均返回成功。深度 swap/transfer provenance 仍需要 Helius/Shyft/Vybe 接入。

## 方法边界

- 本报告不等同于 Binance Alpha EVM forensic；Solana 的 MM/派发/套现判断以 GMGN 标签和行为特征为主。
- DEX 卖出额是样本下界，不包含链下 OTC、CEX 内部账本、跨钱包后续兑换。
- 下一阶段需要接 Helius/Shyft/Vybe 解析 SPL transfer、Jupiter/Raydium/Meteora inner instructions，才能接近完整派发链。
