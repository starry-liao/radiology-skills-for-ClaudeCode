# Installation

`radiology-skills` has one installable Claude Code skill folder: `radiology-skills/`.

The detailed radiology modules are bundled inside `radiology-skills/modules/` and are loaded by the main skill when needed. Do not copy `modules/` as separate skills.

## Windows PowerShell

```powershell
git clone https://github.com/huang-sir1/radiology-skills.git
cd radiology-skills
New-Item -ItemType Directory -Force "$env:USERPROFILE\.claude\skills" | Out-Null
Copy-Item -Recurse -Force .\radiology-skills "$env:USERPROFILE\.claude\skills\"
```

## macOS or Linux

```bash
git clone https://github.com/huang-sir1/radiology-skills.git
cd radiology-skills
mkdir -p ~/.claude/skills
cp -R radiology-skills ~/.claude/skills/
```

Restart Claude Code or reload skills after copying.

## Optional dependencies

Some tasks can work better with additional tools:

- Literature and citation tasks: web search or an academic-search MCP for PubMed, Crossref, arXiv, DOI, and PMID verification.
- Figure and statistics tasks: Python packages such as `numpy`, `pandas`, `scipy`, `scikit-learn`, `matplotlib`, `statsmodels`, and `lifelines`.
- PPT tasks: Python PPTX tooling when a real `.pptx` deck is requested.

These dependencies are optional for the instruction layer. The skill should not invent PMIDs, DOIs, metrics, p-values, accession numbers, or performance results when tooling or source data are unavailable.
