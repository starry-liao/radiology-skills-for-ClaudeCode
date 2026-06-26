# Radiology Skills for Claude Code

> **适配版** — 由 [radiology-skills](https://github.com/huang-sir1/radiology-skills) 稍作修改而来，使其可在 **Claude Code** 中使用。

---

## 原始来源 / Original Source

本项目 fork 自 **[huang-sir1/radiology-skills](https://github.com/huang-sir1/radiology-skills)**。

**原作者 / Original Authors：黄sir组学工作室**

- **Huang Yuhong**（黄宇虹）—《Radiology》原创性研究第一作者
- **Gu Wenchao**（顾文超）—《Radiology》原创性研究第一作者
- **Song Xinyang**（宋新阳）—《Radiology》原创性研究第一作者

三位作者均为发表过《Radiology》原创性研究的第一作者，对影像组学领域有深刻认知。他们开发了这个面向影像组学、影像深度学习和医学影像 AI 研究的全开源技能包，涵盖从选题到发表的完整研究流程。

**本项目的所有核心内容（技能逻辑、参考文件、模块、脚本、红线规则）均来自原作者的工作**。我们只是在技术层面做了最小化的适配，使其能在 Claude Code 环境下运行。请充分尊重原作者的原创性和辛勤付出。

如果你觉得这个技能对你有帮助，请给原始仓库 [huang-sir1/radiology-skills](https://github.com/huang-sir1/radiology-skills) 点一个 Star ⭐。

---

## 修改说明 / Modifications

相比原始 Codex 版本，本项目做了以下修改：

| 修改 | 说明 |
|---|---|
| 删除 `agents/openai.yaml` | Claude Code 通过 SKILL.md 的 `description` 字段自动匹配技能，不需要 Codex 专属的代理配置文件 |
| 更新 `SKILL.md` 模块加载说明 | 将 "load the matching internal module under `modules/`" 改为明确的 Read 工具调用指引 |
| 更新安装路径 | `~/.codex/skills/` → `~/.claude/skills/`（或项目 `.claude/skills/`） |
| 更新调用语法 | `$radiology-skills` → `/radiology-skills`（或通过语义自动匹配触发） |
| 更新文档中的平台引用 | README.md 和 install.md 中的 "Codex" → "Claude Code" |

**未修改的部分：**
- ✅ 22 个子模块（`modules/`）— 全部保留
- ✅ 25+ 个参考文件（`references/`）— 全部保留
- ✅ 2 个 Python 辅助脚本（`scripts/`）— 全部保留
- ✅ 测试用例和示例（`tests/`, `examples/`）— 全部保留
- ✅ 红线规则、输出合约、路由表 — 全部保留
- ✅ MIT 许可证 — 保持不变

---

## 安装 / Installation

### 方法一：项目级安装（推荐）

将技能安装到当前项目的 `.claude/skills/` 目录下，仅在该项目中生效：

**Windows PowerShell:**
```powershell
git clone https://github.com/starry-liao/radiology-skills-for-ClaudeCode.git
cd radiology-skills-for-ClaudeCode
New-Item -ItemType Directory -Force ".claude\skills" | Out-Null
Copy-Item -Recurse -Force .\radiology-skills ".claude\skills\"
```

**macOS / Linux:**
```bash
git clone https://github.com/starry-liao/radiology-skills-for-ClaudeCode.git
cd radiology-skills-for-ClaudeCode
mkdir -p .claude/skills
cp -R radiology-skills .claude/skills/
```

### 方法二：用户级安装

安装到用户目录，所有项目均可使用：

**Windows PowerShell:**
```powershell
git clone https://github.com/starry-liao/radiology-skills-for-ClaudeCode.git
cd radiology-skills-for-ClaudeCode
New-Item -ItemType Directory -Force "$env:USERPROFILE\.claude\skills" | Out-Null
Copy-Item -Recurse -Force .\radiology-skills "$env:USERPROFILE\.claude\skills\"
```

**macOS / Linux:**
```bash
git clone https://github.com/starry-liao/radiology-skills-for-ClaudeCode.git
cd radiology-skills-for-ClaudeCode
mkdir -p ~/.claude/skills
cp -R radiology-skills ~/.claude/skills/
```

安装后重启 Claude Code 或重新加载技能即可使用。

---

## 使用 / Usage

在 Claude Code 中，有两种方式触发此技能：

1. **斜杠命令**：输入 `/radiology-skills`
2. **语义自动匹配**：直接描述你的需求，当内容涉及放射组学、影像 AI、深度学习影像等关键词时，Claude Code 会自动加载此技能

示例提示：
```text
/radiology-skills 我有 300 例多中心肝癌 MRI，想找近三年前沿方向并设计课题。
```

也可以直接用中文提问：
- 我有 300 例多中心肝癌 MRI，想找近三年前沿方向并设计课题。
- 影像组学模型做完了，我有 bulk RNA、单细胞和空间转录组，帮我设计机制解析路线。
- 帮我检查 LASSO、Cox、C-index、校准曲线和 DCA 的统计流程是否规范。
- ROI 是两位医生勾画的，帮我设计标注 SOP 和 Methods 写法。
- 投稿前帮我模拟审稿人做一次严格预审。

---

## 技能内容概览

本技能基于 2023-2026 年高水平文献，整理了 *Radiology*、*Radiology: Artificial Intelligence*、*The Lancet Oncology*、*The Lancet Digital Health*、*Nature Medicine*、*Nature Cancer*、*Nature Communications*、*Science Advances*、*eClinicalMedicine*、*eBioMedicine*、*Cell Reports Medicine*、*npj Digital Medicine* 等高影响力期刊中医学影像 AI、影像组学、影像深度学习、影像基因组学和临床转化相关研究的发表规律。

### 25 个研究场景

| # | 场景 | 说明 |
|---|---|---|
| 1 | 课题可行性判断 | 有数据但不确定能做什么研究 |
| 2 | 前沿方向与创新点 | 从高水平期刊中寻找影像 AI 前沿 |
| 3 | 文献证据 | 建议背后的近三年文献依据 |
| 4 | 系统文献梳理 | 整理特定方向的文献 |
| 5 | 公共数据库 | TCIA、TCGA、GEO、CPTAC、IDC 使用 |
| 6 | 影像组学研究 | Handcrafted radiomics 全流程 |
| 7 | ROI/标注规范 | 病灶选择、读片者一致性、质控 |
| 8 | 影像深度学习 | CNN、Transformer、基础模型设计 |
| 9 | 机制解析 | 影像基因组学、多组学、单细胞、空间转录组 |
| 10 | 课题设计 | 从数据到可投稿方案 |
| 11 | 基金申报 | 国自然、省自然等基金写作 |
| 12 | 模型验证 | 结果可靠性审查 |
| 13 | 统计分析 | LASSO、Cox、校准、DCA 等规范 |
| 14 | 多中心 | 多医院、多机器的验证与 harmonization |
| 15 | 报告规范 | CLAIM、CLEAR、RQS、IBSI、TRIPOD+AI 等 |
| 16 | 数据与隐私 | DICOM、NIfTI、mask、共享 |
| 17 | 伦理合规 | IRB、知情同意、隐私 |
| 18 | 可复现性 | 代码、特征表、模型参数 |
| 19 | 论文写作 | Methods、Results、Discussion |
| 20 | 图表规划 | ROC、校准、DCA、KM、SHAP 等 |
| 21 | 投稿预审 | 模拟审稿人挑问题 |
| 22 | 选刊投稿 | 冲刺/主投/备选梯队 |
| 23 | 临床转化 | 读者研究、前瞻验证、部署 |
| 24 | 回复审稿人 | 逐条回应策略 |
| 25 | 依据溯源 | 规则、建议的来源追溯 |

### 22 个内部模块

| 模块 | 用途 |
|---|---|
| `radiology-frontier` | 前沿方向、创新点和高水平期刊发表规律 |
| `radiology-design` | 课题可行性、研究设计和验证策略 |
| `radiology-search` | 文献和公共数据检索、PMID/DOI 核验 |
| `radiology-annotation` | ROI/VOI/mask 标注 SOP、一致性和质控 |
| `radiology-data` | DICOM 脱敏、数据共享、代码和 FAIR |
| `radiology-ethics` | 伦理、知情同意、隐私和数据治理 |
| `radiology-radiomics` | 传统影像组学流程、IBSI/CLEAR、泄漏检查 |
| `radiology-deep-learning` | 影像深度学习、CNN/Transformer/基础模型设计 |
| `radiology-radiogenomics` | 影像基因组学、多组学、单细胞和空间转录组机制解析 |
| `radiology-stats` | ROC、DeLong、校准、DCA、MRMC、生存和样本量 |
| `radiology-figure` | Radiology 风格图表、统计图和影像 panel |
| `radiology-reporting` | CLAIM、TRIPOD+AI、CLEAR、RQS、IBSI、STARD 等规范 |
| `radiology-writing` | Radiology 风格论文结构、摘要、Methods、Results、Discussion |
| `radiology-polishing` | 英文润色、统计表述和过度结论检查 |
| `radiology-reader` | 医学影像论文中英对照精读 |
| `radiology-citation` | 影像期刊范围内的引用检索和 RIS/ENW/BibTeX 导出 |
| `radiology-prereview` | 投稿前模拟审稿和 blocker/major/minor 问题清单 |
| `radiology-journal` | 选刊、投稿梯队和期刊匹配判断 |
| `radiology-response` | 审稿意见逐点回复和返修策略 |
| `radiology-translation` | 临床转化、读者研究、前瞻验证和部署路径 |
| `radiology-grant` | 国自然、省自然和院级课题申报写作 |
| `radiology-paper2ppt` | 影像论文中文汇报 PPT |

### 可选依赖

- 文献和引用：学术搜索 MCP（PubMed、Crossref、arXiv）
- 图表和统计：`numpy`, `pandas`, `scipy`, `scikit-learn`, `matplotlib`, `statsmodels`, `lifelines`
- PPT 生成：`python-pptx`

---

## 注意

这个 skill 用于研究设计、方法学审查和论文写作辅助，**不提供**临床诊断、治疗建议或针对具体患者的医学影像解读。

**本技能不应凭空编造 PMID、DOI、指标、p 值、登录号或性能结果。**

---

## 许可证 / License

MIT License — 与原始项目保持一致。详见 [LICENSE](LICENSE)。

原始项目版权所有 © 2026 Radiology Skills Contributors。
