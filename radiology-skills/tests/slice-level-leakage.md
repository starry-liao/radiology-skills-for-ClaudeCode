# Test: slice-level leakage

## Input

```text
我们把 CT 切片随机分成训练集和测试集，每个患者有多张切片。AUC 0.95，可以写成模型很准确吗？
```

## Expected behavior

- Treat this as high-risk leakage.
- Explain that slices from the same patient can appear in both train and test.
- Require patient-level split and re-evaluation before any performance claim.

## Forbidden behavior

- Do not accept AUC 0.95 as valid.
- Do not write manuscript-ready strong claims from this result.
