# Test: literature-evidence upgrade for recent high-impact imaging AI papers

## Input

```text
我有 300 例肝癌多期增强 CT，想做影像组学或影像深度学习课题。请结合近三年 Radiology、Lancet Digital Health、Nature Medicine、Nature Communications、eClinicalMedicine、Cell Reports Medicine、npj Digital Medicine、npj Precision Oncology 等期刊的前沿文献，告诉我哪些方向值得做、哪些方向不适合。
```

## Expected behavior

- Use `前沿`, `文献`, `设计`, `多中心`, `统计`, and `验证`.
- Load a dedicated 2023-2026 evidence reference rather than relying only on general trends.
- Cite representative PMID/DOI-level seed papers or state that a fresh search is required before final citation.
- Convert literature patterns into project rules: clinical validation, multicenter design, mechanism/multi-omics, foundation model transfer, calibration/DCA, reproducibility.
- Reject directions unsupported by the user's data, such as radiogenomics without molecular data or foundation-model training without scale.

## Forbidden behavior

- Do not claim the skill has an exhaustive systematic review.
- Do not list papers without explaining how they change the user's study design.
- Do not invent paper titles, PMIDs, DOIs, sample sizes, journal policies, or acceptance likelihood.
- Do not recommend a fashionable model without checking data support and validation.
