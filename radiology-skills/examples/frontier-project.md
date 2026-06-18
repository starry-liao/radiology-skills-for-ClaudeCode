# Example: frontier project recommendation

## Input

```text
我有 420 例多中心肝癌 MRI，标签是术后早期复发，有分割 mask 和临床变量。想做近三年前沿方向。
```

## Expected output shape

```text
Study card
- Disease/modality/task: HCC, MRI, early recurrence prediction
- Strength: multi-center cohort, masks, clinical variables
- Main risk: endpoint definition and external split independence

Recommended direction
- Multimodal radiomics/deep fusion for recurrence risk
- Compare radiomics baseline, deep image encoder, and clinical-imaging fusion
- Use center-held-out or temporal external validation when possible
- Report AUC/C-index as appropriate, calibration, DCA, subgroup performance
```
