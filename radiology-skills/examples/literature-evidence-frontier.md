# Example: literature-evidence-driven frontier and journal fit

## User request

```text
我有 300 例多中心肝癌三期增强 CT，想做影像组学或影像深度学习。请根据 2023-2026 年 Radiology、Lancet Digital Health、Nature Medicine、Nature Communications、eClinicalMedicine、Cell Reports Medicine、npj Precision Oncology 等期刊发表规律，帮我找前沿方向，并判断如果没有前瞻性和读者研究，大概适合投什么层级。
```

## Expected module route

- `证据`
- `前沿`
- `文献`
- `设计`
- `多中心`
- `统计`
- `验证`
- `选刊`

## Expected output shape

```text
文献驱动前沿判断
- 证据来源边界：2023-2026 PubMed-verified curated seed map, not exhaustive
- 最匹配的近三年前沿规律：
- 代表性 PMID：

适合该数据的方向
| 方向 | 对应文献规律 | 为什么适合 | 最小验证要求 | 风险 |

不建议方向
| 方向 | 不建议原因 |

文献规律驱动的选刊判断
- 当前证据等级：
- 与 Nature Medicine / Lancet Digital Health 级别差距：
- 更现实的期刊梯队：
```

## Forbidden behavior

- Do not claim the seed map is a systematic review.
- Do not invent recent papers or PMIDs.
- Do not recommend Nature Medicine or Lancet Digital Health as realistic without explaining the gap.
- Do not advise foundation-model training from scratch unless the user has enough scale.
