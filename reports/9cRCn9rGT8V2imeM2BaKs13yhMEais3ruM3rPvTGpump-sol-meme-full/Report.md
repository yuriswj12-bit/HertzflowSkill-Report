# ANSEM (The Black Bull) - Solana meme 链上速查报告

_生成时间 2026-06-30 01:03:19 UTC · 模式 sol_meme MVP · 数据源 GMGN CLI_

## 一屏结论

| 维度 | 结论 | 证据 |
|---|---|---|
| 当前阶段 | 疑似 MM/机器人主导 | 风险评分 7/10 |
| 市值/流动性 | $135.68M / $1.42M | holders 34649 |
| 筹码集中 | top10 63.44% | top holder 快照 100 个 |
| MM/做市地址 | 129 个候选 | confirmed/strong/weak 分层输出 |
| 派发/套现 | 194 个候选 | top traders 卖出额下界 $5.45M |
| 异动地址 | 226 个候选 | 输出监控 18 个 |

## 速读摘要

- **代币**: `9cRCn9rGT8V2imeM2BaKs13yhMEais3ruM3rPvTGpump`，价格 `0.13568241`，市值约 $135.68M，流动性约 $1.42M。
- **MM/做市**: 识别到 129 个候选地址；confirmed 代表 GMGN/bot 标签，strong 代表高成交低库存等行为特征。
- **派发/套现**: top traders 可见卖出额下界约 $5.45M，买入额约 $7.26M；这不是全链真实套现总额，只是 GMGN 返回样本下界。
- **异动监控**: 已导出 18 个地址，可优先盯大额卖出、疑似 MM、suspicious、bundler/rat/sniper 类地址。

## 安全与权限

| 项目 | 值 |
|---|---|
| Mint renounced | True |
| Freeze renounced | True |
| Rug ratio | - |
| Top10 holder rate | 0.6344 |
| Wash trading | - |
| Sniper count | - |
| Smart/KOL wallets | 78/41 |

## MM / 做市候选地址

| 地址 | 置信度 | 持仓% | 买入额 | 卖出额 | 交易数 | 理由 |
|---|---|---:|---:|---:|---:|---|
| `3H9LVH...FSEC` | confirmed | 0.07% | $64,815 | $718,653 | 254 | GMGN/bot 标签命中, 高频成交且低库存 |
| `9aP2vS...SR5T` | confirmed | 0.12% | $7,720 | $250,004 | 92 | GMGN/bot 标签命中, 高频成交且低库存 |
| `78thMY...oMDM` | confirmed | 0.08% | $49,503 | $187,840 | 61 | GMGN/bot 标签命中, 高频成交且低库存 |
| `H3qrST...Bxj1` | confirmed | 0.21% | $0 | $229,179 | 203 | GMGN/bot 标签命中, 高频成交且低库存 |
| `34syhu...xEKT` | confirmed | 0.06% | $124,464 | $104,180 | 63 | GMGN/bot 标签命中, 高频成交且低库存 |
| `2uK7As...iANA` | confirmed | 0.06% | $107,858 | $115,247 | 105 | GMGN/bot 标签命中, 高频成交且低库存 |
| `3inTyf...rTg2` | confirmed | 0.30% | $181,296 | $25,427 | 56 | GMGN/bot 标签命中, 高频成交且低库存 |
| `C8HH76...D55Y` | confirmed | 0.24% | $150,052 | $29,386 | 48 | GMGN/bot 标签命中 |
| `9Jj6XH...BCW3` | confirmed | 0.08% | $98,282 | $75,767 | 50 | GMGN/bot 标签命中, 高频成交且低库存 |
| `Dq34nm...wEdZ` | confirmed | 0.06% | $93,681 | $65,374 | 28 | GMGN/bot 标签命中 |
| `As7HjL...SMB5` | confirmed | 0.00% | $58,105 | $93,523 | 115 | GMGN/bot 标签命中, 高频成交且低库存 |
| `ACTbvb...y831` | confirmed | 0.07% | $7,393 | $139,852 | 180 | GMGN/bot 标签命中, 高频成交且低库存 |
| `6h7gCv...A7Pd` | confirmed | 0.00% | $67,221 | $68,534 | 641 | GMGN/bot 标签命中, 高频成交且低库存 |
| `GmCqxJ...BCoD` | confirmed | 0.08% | $44,229 | $90,616 | 233 | GMGN/bot 标签命中, 高频成交且低库存 |
| `6Hcrxu...8UMg` | confirmed | 0.33% | $29,030 | $102,445 | 38 | GMGN/bot 标签命中 |
| `DPUq1b...f5jc` | confirmed | 0.10% | $123,093 | $995.70 | 32 | GMGN/bot 标签命中 |
| `EMp115...utFB` | confirmed | 0.08% | $52,563 | $70,826 | 45 | GMGN/bot 标签命中 |
| `38CX6Y...mUMJ` | confirmed | 0.12% | $116,058 | $7,108 | 30 | GMGN/bot 标签命中 |
| `6T8Var...WW6N` | confirmed | 0.24% | $121,330 | $1,008 | 46 | GMGN/bot 标签命中 |
| `CDL22E...RVUf` | confirmed | 0.07% | $69,247 | $41,947 | 20 | GMGN/bot 标签命中 |

## 派发 / 套现候选

| 地址 | 持仓% | 买入额 | 卖出额 | 已卖比例 | 转出量 | 理由 |
|---|---:|---:|---:|---:|---:|---|
| `3H9LVH...FSEC` | 0.07% | $64,815 | $718,653 | 94.76% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `HTpoBR...cS9y` | 0.21% | $696,950 | $522,178 | 72.61% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `5URyNU...c19Y` | 0.17% | $7,100 | $502,508 | 82.92% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `2S8E25...RX7d` | 0.15% | $493,601 | $401,045 | 76.60% | 0.162774 | 卖出比例高，存在派发/兑现动作, 存在转出，不一定是卖出但代表筹码继续扩散, 带 insider/bundler 类标签 |
| `3CPHk5...FkWY` | 0.19% | $269,232 | $327,186 | 66.79% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `4aArED...xTu3` | 0.08% | $172,265 | $299,939 | 98.46% | 63.07M | 卖出比例高，存在派发/兑现动作, 存在转出，不一定是卖出但代表筹码继续扩散, 带 insider/bundler 类标签 |
| `6btcCb...g5eT` | 0.12% | $0 | $261,754 | 84.06% | 0 | 卖出比例高，存在派发/兑现动作 |
| `9aP2vS...SR5T` | 0.12% | $7,720 | $250,004 | 91.03% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `CxCTVj...rdtT` | 0.59% | $2,327 | $241,927 | 51.41% | 4.14M | 当前筹码来自 transfer-in，可能是分发下游, 卖出比例高，存在派发/兑现动作, 存在转出，不一定是卖出但代表筹码继续扩散 |
| `vsTw91...CWDr` | 0.13% | $76,419 | $230,541 | 63.59% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `H3qrST...Bxj1` | 0.21% | $0 | $229,179 | 50.88% | 2.85M | 卖出比例高，存在派发/兑现动作, 存在转出，不一定是卖出但代表筹码继续扩散 |
| `9H9HU7...C4AZ` | 0.23% | $368,148 | $212,614 | 76.98% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `78thMY...oMDM` | 0.08% | $49,503 | $187,840 | 73.55% | 0 | 卖出比例高，存在派发/兑现动作 |
| `8e9bkF...6qg6` | 0.18% | $14,186 | $185,008 | 62.13% | 0.094748 | 卖出比例高，存在派发/兑现动作, 存在转出，不一定是卖出但代表筹码继续扩散 |
| `GfePXR...8Ew2` | 0.20% | $279,930 | $171,631 | 55.99% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `DAEdBm...CvHC` | 0.11% | $0 | $153,160 | 87.69% | 0 | 卖出比例高，存在派发/兑现动作 |
| `GA1G2w...9j4e` | 0.14% | $16,802 | $152,912 | 57.18% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `HQdFfm...fzeH` | 0.09% | $60,641 | $151,483 | 70.38% | 0 | 卖出比例高，存在派发/兑现动作 |
| `LCTTbB...NiqX` | 0.10% | $206,473 | $143,926 | 60.50% | 715,632 | 卖出比例高，存在派发/兑现动作, 存在转出，不一定是卖出但代表筹码继续扩散, 带 insider/bundler 类标签 |
| `ACTbvb...y831` | 0.07% | $7,393 | $139,852 | 97.72% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `2uK7As...iANA` | 0.06% | $107,858 | $115,247 | 69.27% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `34syhu...xEKT` | 0.06% | $124,464 | $104,180 | 63.34% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `6Hcrxu...8UMg` | 0.33% | $29,030 | $102,445 | 18.21% | 0 | 卖出比例高，存在派发/兑现动作 |
| `3Ci8as...guBU` | 0.00% | $97,533 | $101,491 | 98.31% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |
| `As7HjL...SMB5` | 0.00% | $58,105 | $93,523 | 100.00% | 0 | 卖出比例高，存在派发/兑现动作, 带 insider/bundler 类标签 |

## 异动地址

| 地址 | 持仓% | 买入额 | 卖出额 | 利润 | 标签 | 理由 |
|---|---:|---:|---:|---:|---|---|
| `GV6UUm...dC52` | 58.66% | $48.47 | $0 | $83.16M | TOP1, bundler, top_holder, transfer_in | 高盈利地址, 关键标签地址 |
| `3H9LVH...FSEC` | 0.07% | $64,815 | $718,653 | $1.42M | TOP36, bundler, dex_bot, photon | 大额卖出, 高盈利地址, 关键标签地址 |
| `Ac9Y9Q...zSZM` | 0.95% | $2,030 | $0 | $2.19M | TOP3, top_holder, transfer_in | 高盈利地址 |
| `CxCTVj...rdtT` | 0.59% | $2,327 | $241,927 | $1.65M | TOP4, top_holder | 大额卖出, 高盈利地址 |
| `5URyNU...c19Y` | 0.17% | $7,100 | $502,508 | $1.04M | TOP36, bundler, transfer_in | 大额卖出, 高盈利地址, 关键标签地址 |
| `CLM6E4...Kg1Q` | 1.06% | $130,830 | $515.28 | $1.35M | TOP2, bundler, top_holder, whale | 大额买入后仍持仓, 高盈利地址, 关键标签地址 |
| `HTpoBR...cS9y` | 0.21% | $696,950 | $522,178 | $187,433 | TOP27, bundler | 大额卖出, 高盈利地址, 关键标签地址 |
| `3CPHk5...FkWY` | 0.19% | $269,232 | $327,186 | $576,359 | TOP32, bundler, fomo, whale | 大额卖出, 高盈利地址, 关键标签地址 |
| `2S8E25...RX7d` | 0.15% | $493,601 | $401,045 | $165,119 | TOP40, bundler, whale | 大额卖出, 高盈利地址, 关键标签地址 |
| `9aP2vS...SR5T` | 0.12% | $7,720 | $250,004 | $653,885 | TOP54, axiom, bundler | 大额卖出, 高盈利地址, 关键标签地址 |
| `9H9HU7...C4AZ` | 0.23% | $368,148 | $212,614 | $253,953 | TOP24, bundler, fresh_wallet, whale | 大额卖出, 高盈利地址, 关键标签地址 |
| `vsTw91...CWDr` | 0.13% | $76,419 | $230,541 | $499,506 | TOP53, bundler, gmgn | 大额卖出, 高盈利地址, 关键标签地址 |
| `6btcCb...g5eT` | 0.12% | $0 | $261,754 | $535,145 | TOP59, transfer_in | 大额卖出, 高盈利地址 |
| `6Hcrxu...8UMg` | 0.33% | $29,030 | $102,445 | $615,202 | TOP9, axiom, top_holder, transfer_in | 大额卖出, 高盈利地址 |
| `4aArED...xTu3` | 0.08% | $172,265 | $299,939 | $258,483 | TOP93, bundler, whale | 大额卖出, 高盈利地址, 关键标签地址 |
| `GA1G2w...9j4e` | 0.14% | $16,802 | $152,912 | $472,602 | TOP43, bundler, fomo, fresh_wallet | GMGN suspicious 标记, 大额卖出, 高盈利地址, 关键标签地址 |
| `78thMY...oMDM` | 0.08% | $49,503 | $187,840 | $393,765 | TOP35, dex_bot, fomo, fresh_wallet | GMGN suspicious 标记, 大额卖出, 高盈利地址 |
| `5FGoPP...rp8V` | 0.31% | $1.05 | $90,231 | $456,680 | TOP11, fomo, top_holder, transfer_in | 大额卖出, 高盈利地址 |
| `HQdFfm...fzeH` | 0.09% | $60,641 | $151,483 | $320,163 | TOP87, fomo, whale | 大额卖出, 高盈利地址 |
| `ACTbvb...y831` | 0.07% | $7,393 | $139,852 | $362,544 | TOP40, axiom, bundler, dex_bot | 大额卖出, 高盈利地址, 关键标签地址 |
| `GkdYWR...Atac` | 0.37% | $297,612 | $0 | $201,807 | TOP8, bundler, top_holder, transfer_in | 高盈利地址, 关键标签地址 |
| `HDixbr...XN3o` | 0.38% | $0 | $0 | $481,962 | TOP7, fomo, top_holder, transfer_in | 高盈利地址 |
| `3inTyf...rTg2` | 0.30% | $181,296 | $25,427 | $261,695 | TOP12, bundler, padre | 高盈利地址, 关键标签地址 |
| `GfePXR...8Ew2` | 0.20% | $279,930 | $171,631 | $13,432 | TOP30, bundler, transfer_in, whale | 大额卖出, 关键标签地址 |
| `LCTTbB...NiqX` | 0.10% | $206,473 | $143,926 | $105,858 | TOP71, bundler | 大额卖出, 高盈利地址, 关键标签地址 |

## Top holders 快照

| # | 地址 | 持仓% | 余额 | USD | transfer-in | 标签 |
|---:|---|---:|---:|---:|---|---|
| 1 | `GV6UUm...dC52` | 58.66% | 586.63M | $79.03M | True | TOP1, bundler, top_holder, transfer_in |
| 2 | `CLM6E4...Kg1Q` | 1.06% | 10.63M | $1.43M | False | TOP2, bundler, top_holder, whale |
| 3 | `Ac9Y9Q...zSZM` | 0.95% | 9.50M | $1.28M | True | TOP3, top_holder, transfer_in |
| 4 | `CxCTVj...rdtT` | 0.59% | 5.88M | $792,250 | False | TOP4, top_holder |
| 5 | `FnzKY6...L3CC` | 0.53% | 5.26M | $708,255 | False | TOP5, fresh_wallet, top_holder |
| 6 | `HCgo8g...2uYC` | 0.46% | 4.56M | $614,460 | True | TOP6, fresh_wallet, top_holder, transfer_in |
| 7 | `HDixbr...XN3o` | 0.38% | 3.80M | $511,916 | True | TOP7, fomo, top_holder, transfer_in |
| 8 | `GkdYWR...Atac` | 0.37% | 3.71M | $499,535 | True | TOP8, bundler, top_holder, transfer_in |
| 9 | `6Hcrxu...8UMg` | 0.33% | 3.30M | $444,669 | True | TOP9, axiom, top_holder, transfer_in |
| 10 | `F5hkYs...xqs6` | 0.32% | 3.23M | $434,876 | False | TOP10, bundler, fomo, top_holder |
| 11 | `5FGoPP...rp8V` | 0.31% | 3.11M | $418,301 | True | TOP11, fomo, top_holder, transfer_in |
| 12 | `3inTyf...rTg2` | 0.30% | 3.02M | $407,281 | False | TOP12, bundler, padre |
| 13 | `ASTyfS...iaJZ` | 0.29% | 2.93M | $394,754 | False | TOP13 |
| 14 | `3SdVtY...bgou` | 0.28% | 2.82M | $380,031 | False | TOP14, whale |
| 15 | `Cqku64...sUpw` | 0.26% | 2.63M | $354,265 | False | TOP15, bundler, fresh_wallet |
| 16 | `3J9Sq1...Fdxb` | 0.26% | 2.62M | $353,325 | False | TOP16, bundler |
| 17 | `8MHU3N...JP7b` | 0.26% | 2.61M | $351,635 | False | TOP17, bundler, whale |
| 18 | `DopmpJ...PcSU` | 0.25% | 2.50M | $336,901 | False | TOP18, bundler |
| 19 | `6T8Var...WW6N` | 0.24% | 2.40M | $323,201 | False | TOP19, bundler, fomo, fresh_wallet |
| 20 | `37Byuj...NEYN` | 0.24% | 2.39M | $322,210 | False | TOP20 |

## 数据缺口

- GMGN 基础接口均返回成功。深度 swap/transfer provenance 仍需要 Helius/Shyft/Vybe 接入。

## 方法边界

- 本报告不等同于 Binance Alpha EVM forensic；Solana 的 MM/派发/套现判断以 GMGN 标签和行为特征为主。
- DEX 卖出额是样本下界，不包含链下 OTC、CEX 内部账本、跨钱包后续兑换。
- 下一阶段需要接 Helius/Shyft/Vybe 解析 SPL transfer、Jupiter/Raydium/Meteora inner instructions，才能接近完整派发链。
