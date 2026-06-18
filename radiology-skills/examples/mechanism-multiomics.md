# Example: multi-omics mechanism interpretation

## Input

```text
我有 210 例肝癌 MRI radiomics 复发风险模型，其中 60 例有配对 bulk RNA，另外有公开 HCC 单细胞和空间转录组数据。想解释高风险 radscore 背后的生物机制。
```

## Expected output shape

```text
机制解析定位
- 已有影像模型：MRI radiomics recurrence risk model
- 可用组学数据：60 paired bulk RNA, public scRNA-seq, public spatial transcriptomics
- 核心问题：高风险影像表型是否反映免疫抑制、缺氧、血管生成或基质重塑状态

推荐整合路线
1. bulk RNA：按 radscore high/low 或连续变量做差异表达、GSEA/GSVA、WGCNA、免疫浸润估计。
2. 单细胞：将 radscore 相关基因模块映射到肿瘤细胞、髓系细胞、T/NK、CAF、内皮等细胞状态。
3. 空间转录组：定位相关通路和细胞类型是否聚集于肿瘤边缘、缺氧区、免疫排斥区或基质区。
4. 验证：外部队列、IHC/多重免疫荧光、空间区域复核。

可写进论文的逻辑
- 高 radscore 与 [通路] 相关，单细胞提示该信号主要来源于 [细胞状态]，空间数据支持其在 [生态位] 富集。
```
