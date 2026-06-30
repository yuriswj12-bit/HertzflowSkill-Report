# ANSEM (The Black Bull) - Solana meme 链上速查报告

_生成时间 2026-06-30 03:53:42 UTC · 模式 sol_meme MVP · 数据源 GMGN CLI_

## 一屏结论

| 维度 | 结论 | 证据 |
|---|---|---|
| 当前阶段 | 疑似 MM/机器人主导 | 风险评分 7/10 |
| 市值/流动性 | $126.54M / $1.29M | holders 39071 |
| 筹码集中 | top10 63.47% | top holder 快照 100 个 |
| MM/做市地址 | 133 个候选 | confirmed/strong/weak 分层输出 |
| 派发/套现 | 197 个候选 | top traders 卖出额下界 $5.73M |
| 异动地址 | 227 个候选 | 输出监控 18 个 |

## 速读摘要

- **代币**: `9cRCn9rGT8V2imeM2BaKs13yhMEais3ruM3rPvTGpump`，价格 `0.12654404`，市值约 $126.54M，流动性约 $1.29M。
- **MM/做市**: 识别到 133 个候选地址；confirmed 代表 GMGN/bot 标签，strong 代表高成交低库存等行为特征。
- **派发/套现**: top traders 可见卖出额下界约 $5.73M，买入额约 $7.25M；这不是全链真实套现总额，只是 GMGN 返回样本下界。
- **异动监控**: 已导出 18 个地址，可优先盯大额卖出、疑似 MM、suspicious、bundler/rat/sniper 类地址。

## 安全与权限

| 项目 | 值 |
|---|---|
| Mint renounced | True |
| Freeze renounced | True |
| Rug ratio | - |
| Top10 holder rate | 0.6347 |
| Wash trading | - |
| Sniper count | - |
| Smart/KOL wallets | 79/42 |

## MM / 做市候选地址

| 地址 | 置信度 | 持仓% | 买入额 | 卖出额 | 交易数 | 理由 |
|---|---|---:|---:|---:|---:|---|
| `3H9LVH...FSEC` | confirmed | 0.12% | $127,861 | $718,653 | 275 | GMGN/bot 标签命中, 高频成交且低库存 |
| `5V676H...9zFb` | confirmed | 0.08% | $239,445 | $154,544 | 170 | GMGN/bot 标签命中, 高频成交且低库存, 买卖量接近平衡，疑似做市/刷量 |
| `9aP2vS...SR5T` | confirmed | 0.12% | $7,720 | $250,004 | 92 | GMGN/bot 标签命中, 高频成交且低库存 |
| `78thMY...oMDM` | confirmed | 0.08% | $49,503 | $187,840 | 61 | GMGN/bot 标签命中, 高频成交且低库存 |
| `H3qrST...Bxj1` | confirmed | 0.21% | $0 | $229,179 | 203 | GMGN/bot 标签命中, 高频成交且低库存 |
| `34syhu...xEKT` | confirmed | 0.06% | $124,464 | $104,180 | 63 | GMGN/bot 标签命中, 高频成交且低库存 |
| `2uK7As...iANA` | confirmed | 0.06% | $107,858 | $115,247 | 105 | GMGN/bot 标签命中, 高频成交且低库存 |
| `3inTyf...rTg2` | confirmed | 0.30% | $181,296 | $25,427 | 56 | GMGN/bot 标签命中, 高频成交且低库存 |
| `9Jj6XH...BCW3` | confirmed | 0.07% | $98,282 | $92,089 | 56 | GMGN/bot 标签命中, 高频成交且低库存 |
| `C8HH76...D55Y` | confirmed | 0.24% | $150,052 | $29,386 | 48 | GMGN/bot 标签命中 |
| `DPUq1b...f5jc` | confirmed | 0.07% | $123,093 | $40,242 | 43 | GMGN/bot 标签命中 |
| `6h7gCv...A7Pd` | confirmed | 0.00% | $80,304 | $81,326 | 655 | GMGN/bot 标签命中, 高频成交且低库存 |
| `Dq34nm...wEdZ` | confirmed | 0.06% | $93,681 | $65,374 | 28 | GMGN/bot 标签命中 |
| `2NCyVm...8HPy` | confirmed | 0.08% | $68,627 | $89,246 | 194 | GMGN/bot 标签命中, 高频成交且低库存 |
| `As7HjL...SMB5` | confirmed | 0.00% | $58,105 | $93,523 | 115 | GMGN/bot 标签命中, 高频成交且低库存 |
| `GmCqxJ...BCoD` | confirmed | 0.09% | $58,759 | $90,616 | 259 | GMGN/bot 标签命中, 高频成交且低库存 |
| `ACTbvb...y831` | confirmed | 0.07% | $7,393 | $139,852 | 180 | GMGN/bot 标签命中, 高频成交且低库存 |
| `AHjQMx...pmxT` | confirmed | 0.08% | $76,927 | $65,795 | 133 | GMGN/bot 标签命中, 高频成交且低库存 |
| `6Hcrxu...8UMg` | confirmed | 0.33% | $29,030 | $102,445 | 38 | GMGN/bot 标签命中 |
| `EMp115...utFB` | confirmed | 0.08% | $52,563 | $70,826 | 45 | GMGN/bot 标签命中 |

## 派发 / 套现候选

| 地址 | 持仓% | 买入额 | 卖出额 | 已卖比例 | 转出量 | 理由 |
|---|---:|---:|---:|---:|---:|---|
| `3H9LVH...FSEC` | 0.12% | $127,861 | $718,653 | 91.85% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `5URyNU...c19Y` | 0.17% | $7,100 | $502,508 | 82.92% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `2S8E25...RX7d` | 0.14% | $493,601 | $413,084 | 77.94% | 0.162774 | 卖出比例高，存在派发/兑现动作, 存在转出，不一定是卖出但代表筹码继续扩散, 带 insider/bundler 类标签 |
| `3CPHk5...FkWY` | 0.19% | $269,232 | $327,186 | 66.79% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `4aArED...xTu3` | 0.09% | $182,158 | $299,939 | 98.32% | 63.07M | 卖出比例高，存在派发/兑现动作, 存在转出，不一定是卖出但代表筹码继续扩散, 带 insider/bundler 类标签 |
| `6btcCb...g5eT` | 0.12% | $0 | $261,754 | 84.06% | 0 | 卖出比例高，存在派发/兑现动作 |
| `9aP2vS...SR5T` | 0.12% | $7,720 | $250,004 | 91.03% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `CxCTVj...rdtT` | 0.59% | $2,327 | $245,409 | 51.62% | 4.14M | 当前筹码来自 transfer-in，可能是分发下游, 卖出比例高，存在派发/兑现动作, 存在转出，不一定是卖出但代表筹码继续扩散 |
| `vsTw91...CWDr` | 0.13% | $76,419 | $230,541 | 63.59% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `H3qrST...Bxj1` | 0.21% | $0 | $229,179 | 50.88% | 2.85M | 卖出比例高，存在派发/兑现动作, 存在转出，不一定是卖出但代表筹码继续扩散 |
| `9H9HU7...C4AZ` | 0.23% | $368,148 | $212,614 | 76.98% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `LCTTbB...NiqX` | 0.11% | $274,513 | $206,699 | 66.12% | 715,632 | 卖出比例高，存在派发/兑现动作, 存在转出，不一定是卖出但代表筹码继续扩散, 带 insider/bundler 类标签 |
| `78thMY...oMDM` | 0.08% | $49,503 | $187,840 | 73.55% | 0 | 卖出比例高，存在派发/兑现动作 |
| `8e9bkF...6qg6` | 0.18% | $14,186 | $185,008 | 62.13% | 0.094748 | 卖出比例高，存在派发/兑现动作, 存在转出，不一定是卖出但代表筹码继续扩散 |
| `GfePXR...8Ew2` | 0.20% | $279,930 | $171,631 | 55.99% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `5V676H...9zFb` | 0.08% | $239,445 | $154,544 | 75.89% | 9,294 | 卖出比例高，存在派发/兑现动作, 存在转出，不一定是卖出但代表筹码继续扩散, 带 insider/bundler 类标签 |
| `DAEdBm...CvHC` | 0.11% | $0 | $153,160 | 87.69% | 0 | 卖出比例高，存在派发/兑现动作 |
| `GA1G2w...9j4e` | 0.14% | $16,802 | $152,912 | 57.18% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `HQdFfm...fzeH` | 0.09% | $60,641 | $151,483 | 70.38% | 0 | 卖出比例高，存在派发/兑现动作 |
| `ACTbvb...y831` | 0.07% | $7,393 | $139,852 | 97.72% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `2uK7As...iANA` | 0.06% | $107,858 | $115,247 | 69.27% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `34syhu...xEKT` | 0.06% | $124,464 | $104,180 | 63.34% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `3Ci8as...guBU` | 0.00% | $97,533 | $104,132 | 100.00% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `6Hcrxu...8UMg` | 0.33% | $29,030 | $102,445 | 18.21% | 0 | 卖出比例高，存在派发/兑现动作 |
| `As7HjL...SMB5` | 0.00% | $58,105 | $93,523 | 100.00% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |

## 异动地址

| 地址 | 持仓% | 买入额 | 卖出额 | 利润 | 标签 | 理由 |
|---|---:|---:|---:|---:|---|---|
| `GV6UUm...dC52` | 58.66% | $48.47 | $0 | $78.36M | TOP1, bundler, top_holder, transfer_in | 高盈利地址, 关键标签地址 |
| `3H9LVH...FSEC` | 0.12% | $127,861 | $718,653 | $1.41M | TOP59, bundler, photon | 大额卖出, 高盈利地址, 关键标签地址 |
| `Ac9Y9Q...zSZM` | 0.95% | $2,030 | $0 | $2.11M | TOP3, top_holder, transfer_in | 高盈利地址 |
| `CxCTVj...rdtT` | 0.59% | $2,327 | $245,409 | $1.61M | TOP4, top_holder | 大额卖出, 高盈利地址 |
| `5URyNU...c19Y` | 0.17% | $7,100 | $502,508 | $1.03M | TOP36, bundler, transfer_in | 大额卖出, 高盈利地址, 关键标签地址 |
| `CLM6E4...Kg1Q` | 1.06% | $130,830 | $515.28 | $1.26M | TOP2, bundler, top_holder, whale | 大额买入后仍持仓, 高盈利地址, 关键标签地址 |
| `3CPHk5...FkWY` | 0.19% | $269,232 | $327,186 | $560,523 | TOP31, bundler, fomo, whale | 大额卖出, 高盈利地址, 关键标签地址 |
| `2S8E25...RX7d` | 0.14% | $493,601 | $413,084 | $157,942 | TOP46, bundler, whale | 大额卖出, 高盈利地址, 关键标签地址 |
| `9aP2vS...SR5T` | 0.12% | $7,720 | $250,004 | $643,699 | TOP56, axiom, bundler | 大额卖出, 高盈利地址, 关键标签地址 |
| `9H9HU7...C4AZ` | 0.23% | $368,148 | $212,614 | $235,508 | TOP24, bundler, fresh_wallet, whale | 大额卖出, 高盈利地址, 关键标签地址 |
| `vsTw91...CWDr` | 0.13% | $76,419 | $230,541 | $489,215 | TOP55, bundler, gmgn | 大额卖出, 高盈利地址, 关键标签地址 |
| `6btcCb...g5eT` | 0.12% | $0 | $261,754 | $525,590 | TOP63, transfer_in | 大额卖出, 高盈利地址 |
| `4aArED...xTu3` | 0.09% | $182,158 | $299,939 | $251,619 | TOP87, bundler, whale | 大额卖出, 高盈利地址, 关键标签地址 |
| `6Hcrxu...8UMg` | 0.33% | $29,030 | $102,445 | $588,202 | TOP9, axiom, top_holder, transfer_in | 大额卖出, 高盈利地址 |
| `GA1G2w...9j4e` | 0.14% | $16,802 | $152,912 | $460,875 | TOP42, bundler, fomo, fresh_wallet | GMGN suspicious 标记, 大额卖出, 高盈利地址, 关键标签地址 |
| `78thMY...oMDM` | 0.08% | $49,503 | $187,840 | $386,637 | TOP35, dex_bot, fomo, fresh_wallet | GMGN suspicious 标记, 大额卖出, 高盈利地址 |
| `LCTTbB...NiqX` | 0.11% | $274,513 | $206,699 | $110,538 | TOP72, bundler | 大额卖出, 高盈利地址, 关键标签地址 |
| `HQdFfm...fzeH` | 0.09% | $60,641 | $151,483 | $313,046 | TOP92, fomo, whale | 大额卖出, 高盈利地址 |
| `5FGoPP...rp8V` | 0.31% | $1.05 | $90,231 | $431,281 | TOP11, fomo, top_holder, transfer_in | 大额卖出, 高盈利地址 |
| `ACTbvb...y831` | 0.07% | $7,393 | $139,852 | $355,843 | TOP37, axiom, bundler, dex_bot | 大额卖出, 高盈利地址, 关键标签地址 |
| `GkdYWR...Atac` | 0.37% | $297,612 | $0 | $171,476 | TOP8, bundler, top_holder, transfer_in | 高盈利地址, 关键标签地址 |
| `HDixbr...XN3o` | 0.38% | $0 | $0 | $450,879 | TOP7, fomo, top_holder, transfer_in | 高盈利地址 |
| `GfePXR...8Ew2` | 0.20% | $279,930 | $171,631 | $-2,928 | TOP29, bundler, transfer_in, whale | 大额卖出, 关键标签地址 |
| `3inTyf...rTg2` | 0.30% | $181,296 | $25,427 | $236,966 | TOP12, bundler, padre | 高盈利地址, 关键标签地址 |
| `5V676H...9zFb` | 0.08% | $239,445 | $154,544 | $42,043 | TOP29, axiom, bundler, dex_bot | 大额卖出, 关键标签地址 |

## Top holders 快照

| # | 地址 | 持仓% | 余额 | USD | transfer-in | 标签 |
|---:|---|---:|---:|---:|---|---|
| 1 | `GV6UUm...dC52` | 58.66% | 586.63M | $74.23M | True | TOP1, bundler, top_holder, transfer_in |
| 2 | `CLM6E4...Kg1Q` | 1.06% | 10.63M | $1.35M | False | TOP2, bundler, top_holder, whale |
| 3 | `Ac9Y9Q...zSZM` | 0.95% | 9.50M | $1.20M | True | TOP3, top_holder, transfer_in |
| 4 | `CxCTVj...rdtT` | 0.59% | 5.86M | $740,983 | False | TOP4, top_holder |
| 5 | `FnzKY6...L3CC` | 0.51% | 5.11M | $647,034 | False | TOP5, fresh_wallet, top_holder |
| 6 | `HCgo8g...2uYC` | 0.49% | 4.91M | $621,212 | True | TOP6, fresh_wallet, top_holder, transfer_in |
| 7 | `HDixbr...XN3o` | 0.38% | 3.80M | $480,833 | True | TOP7, fomo, top_holder, transfer_in |
| 8 | `GkdYWR...Atac` | 0.37% | 3.71M | $469,204 | True | TOP8, bundler, top_holder, transfer_in |
| 9 | `6Hcrxu...8UMg` | 0.33% | 3.30M | $417,670 | True | TOP9, axiom, top_holder, transfer_in |
| 10 | `F5hkYs...xqs6` | 0.32% | 3.23M | $408,471 | False | TOP10, bundler, fomo, top_holder |
| 11 | `5FGoPP...rp8V` | 0.31% | 3.11M | $392,902 | True | TOP11, fomo, top_holder, transfer_in |
| 12 | `3inTyf...rTg2` | 0.30% | 3.02M | $382,551 | False | TOP12, bundler, padre |
| 13 | `ASTyfS...iaJZ` | 0.29% | 2.93M | $370,933 | False | TOP13 |
| 14 | `3SdVtY...bgou` | 0.28% | 2.82M | $356,956 | False | TOP14, whale |
| 15 | `Cqku64...sUpw` | 0.26% | 2.63M | $332,755 | False | TOP15, bundler, fresh_wallet |
| 16 | `3J9Sq1...Fdxb` | 0.26% | 2.62M | $331,871 | False | TOP16, bundler |
| 17 | `8MHU3N...JP7b` | 0.26% | 2.61M | $330,284 | False | TOP17, bundler, whale |
| 18 | `DopmpJ...PcSU` | 0.25% | 2.50M | $316,444 | False | TOP18, bundler |
| 19 | `6T8Var...WW6N` | 0.24% | 2.40M | $303,577 | False | TOP19, bundler, fomo, fresh_wallet |
| 20 | `37Byuj...NEYN` | 0.24% | 2.39M | $302,646 | False | TOP20 |

## 数据缺口

- GMGN 基础接口均返回成功。深度 swap/transfer provenance 仍需要 Helius/Shyft/Vybe 接入。

## 方法边界

- 本报告不等同于 Binance Alpha EVM forensic；Solana 的 MM/派发/套现判断以 GMGN 标签和行为特征为主。
- DEX 卖出额是样本下界，不包含链下 OTC、CEX 内部账本、跨钱包后续兑换。
- 下一阶段需要接 Helius/Shyft/Vybe 解析 SPL transfer、Jupiter/Raydium/Meteora inner instructions，才能接近完整派发链。
