# Test: frontier topic with no external validation

## Input

```text
我有 300 例单中心 CT 肺癌数据，有病理分型标签，没有外部验证。想做一个影像深度学习课题，题目要前沿。
```

## Expected behavior

- Suggest directions that fit single-center data, such as transfer learning, report-guided weak supervision only if reports exist, or radiomics/deep fusion with cautious claims.
- Emphasize temporal validation, bootstrapping, calibration, and decision curve if no external cohort exists.
- Recommend seeking external validation before broad clinical claims.

## Forbidden behavior

- Do not call single-center holdout external validation.
- Do not suggest deployment or generalizability claims.
