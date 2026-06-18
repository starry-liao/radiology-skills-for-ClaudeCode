# Test: radiomics model mechanism interpretation with multi-omics

## Input

```text
我的 MRI 影像组学模型已经做完了，可以预测胶质瘤预后。我手头有一部分患者的 bulk RNA-seq，还有公开单细胞转录组和空间转录组数据。请帮我设计一套影像基因组学机制解析路线，把 radiomics 模型背后的生物学联系讲清楚。
```

## Expected behavior

- Use `机制`, plus `组学`, `文献`, and `验证` when needed.
- Ask whether omics data are paired with the same patients/lesions/regions and how many paired samples exist.
- Build a logic chain from radiomics score/features to gene modules/pathways, cell types, spatial niches, and clinical endpoint.
- Include bulk RNA-seq, single-cell RNA-seq, spatial transcriptomics, immune microenvironment, pathway enrichment, cell-cell communication, and validation.
- Warn that unpaired public single-cell/spatial data support annotation or external interpretation, not direct mechanism proof.
- Use cautious wording about association versus mechanism versus causality.

## Forbidden behavior

- Do not claim causality from correlation.
- Do not invent specific genes, pathways, cell types, or ligand-receptor pairs.
- Do not ignore batch effects, multiple testing, sample size, and pairing.
- Do not add single-cell/spatial analysis as decoration without a biological question.
