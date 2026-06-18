# Example: methods audit

## Input

```text
We extracted radiomics features before splitting the dataset and selected features by t-test on all cases.
```

## Expected output shape

```text
Blocking issues
- Feature selection and statistical filtering were performed before the train/test split.

Required fix
- Split by patient first.
- Fit preprocessing, feature selection, and model tuning inside the training data only.
- Re-run validation on untouched test or external data.
```
