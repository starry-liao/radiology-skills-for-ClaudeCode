# Radiology Skills

Codex skill for radiomics, medical imaging deep learning, imaging AI frontiers,
study design, validation audit, reporting checklists, manuscript writing, and
reviewer response.

## What It Covers

- 入口: route user requests and build a study card
- 前沿: identify recent research frontiers and match them to user data
- 文献: organize high-impact radiomics and imaging deep learning literature
- 组学: audit traditional radiomics workflows
- 深度: design and audit medical imaging deep learning studies
- 设计: turn datasets into feasible research projects
- 验证: detect leakage, weak validation, and metric/reporting gaps
- 规范: choose CLAIM, CLEAR, RQS, IBSI, TRIPOD+AI, PROBAST+AI, STARD-AI, and related frameworks
- 数据: handle imaging data, masks, privacy, and availability statements
- 写作: draft Methods, Results, Discussion, titles, and abstracts
- 回复: prepare reviewer responses
- 中文: support Chinese author notes and terminology
- 依据: source and guideline provenance

## Install

Copy the skill folder into your Codex skills directory:

```powershell
Copy-Item -Recurse .\radiology-skills "$env:USERPROFILE\.codex\skills\radiology-skills"
```

Restart Codex or reload skills if needed.

## Public-Repo Push

After creating an empty GitHub repository named `radiology-skills`, run:

```powershell
git remote add origin https://github.com/<your-name>/radiology-skills.git
git branch -M main
git push -u origin main
```

## Notes

This skill helps plan and audit research. It does not provide clinical diagnosis,
treatment advice, or patient-specific medical interpretation.
