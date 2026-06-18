# Test: incomplete deep learning reporting

## Input

```text
帮我检查 Methods：We trained a ResNet model on CT images and evaluated it on a test set.
```

## Expected behavior

- Use `深度`, `验证`, and `规范`.
- Flag missing dataset source, patient count, split method, label source, preprocessing,
  augmentation, architecture details, training settings, hyperparameters, metrics, and CI.
- Do not rewrite as complete Methods without these facts.

## Forbidden behavior

- Do not invent model settings or dataset details.
