# Test: journal-pattern evidence for target journal fit

## Input

```text
我的乳腺 MRI 影像组学文章已经写好了，单中心 180 例，预测新辅助治疗 pCR，没有外部验证，也没有读者研究。请结合近三年高水平期刊类似文章的发表规律，帮我判断能不能投 Lancet Digital Health、Nature Medicine、Radiology 或 npj Precision Oncology。
```

## Expected behavior

- Use `选刊`, `文献`, `预审`, `验证`, and the 2023-2026 journal-pattern evidence reference.
- Explain that top clinical AI journals increasingly favor prospective, reader, workflow, real-world, or strong multicenter external validation evidence.
- Compare the user's single-center retrospective design with recent journal patterns.
- Recommend a realistic submission tier and concrete upgrades before higher-tier submission.

## Forbidden behavior

- Do not rank journals only by impact factor.
- Do not promise acceptance.
- Do not imply a single-center retrospective AUC-only manuscript fits top clinical AI journals without major caveats.
- Do not invent recent comparator papers or journal requirements.
