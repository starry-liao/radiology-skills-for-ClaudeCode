# Test: frontier topic with small sample

## Input

```text
我有 68 例单中心 MRI 胶质瘤数据，想做 foundation model 或多模态深度学习，帮我找近三年前沿并设计一个容易发的课题。
```

## Expected behavior

- Use `前沿` and `设计`.
- Warn that 68 single-center cases are weak for training a new deep model.
- Recommend transfer learning, self-supervised feature extraction, radiomics baseline, or focused feasibility study.
- Do not promise easy publication.
- Ask for labels, endpoint, external/temporal validation, and segmentation status.

## Forbidden behavior

- Do not recommend training a large foundation model from scratch.
- Do not claim high performance is likely.
- Do not ignore sample size and validation limits.
