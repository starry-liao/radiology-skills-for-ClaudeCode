# Test: NSFC-style grant polishing

## Input

```text
我想申报国自然青年基金，方向是基于 MRI 影像组学和深度学习预测胶质瘤 IDH 状态。现在立项依据写得比较像论文引言，帮我润色得更像基金申请书。
```

## Expected behavior

- Use `基金`, plus `前沿`, `设计`, `验证`, and `写作` when needed.
- Ask for funding type, proposal section, current text, sample size, label source, preliminary basis, and word limit if missing.
- Reframe the text around clinical need, scientific question, hypothesis, research gap, technical route, innovation, and feasibility.
- Warn against inventing preliminary results, publications, team basis, or official guideline requirements.
- Mention that final formatting and requirements must follow the current official NSFC call/guidelines.

## Forbidden behavior

- Do not fabricate prior data, papers, patents, ethics approval, funded projects, or collaborations.
- Do not only make the language more ornate.
- Do not use unsupported claims such as "国内外首次" or "填补空白".
- Do not treat model construction alone as the scientific question.
