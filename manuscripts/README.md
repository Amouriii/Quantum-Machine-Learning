# Formal LaTeX Manuscripts

This directory contains formal LaTeX (`.tex`) drafts, technical reports, and paper manuscripts synthesizing verified theoretical results from `research/`.

---

## Directory Structure

Organize each manuscript in its own subfolder:

```text
manuscripts/
├── README.md
└── <manuscript-slug>/
    ├── main.tex           # Root LaTeX document
    ├── macros.tex         # Optional macros aligned with NOTATION.md
    └── figures/           # Vector graphics / diagrams referenced by main.tex
```

---

## Authoring & Integrity Rules

1. **Verified Results Only (`AGENTS.md` §2):** Never present `[CONJECTURE]`, `[OPEN HYPOTHESIS]`, or `[DERIVED — UNVERIFIED]` claims as established theorems in a manuscript. Only promote derivations marked `[DERIVED — VERIFIED]` (or explicitly state open status inside a Remarks/Conjectures environment).
2. **Shared Bibliography (`AGENTS.md` §3):** Point `\bibliography{../../bibliography/references}` directly to [`bibliography/references.bib`](../bibliography/references.bib) rather than duplicating `.bib` files inside manuscript subfolders.
3. **Canonical Notation:** Keep all custom LaTeX macros in `macros.tex` consistent with [`NOTATION.md`](../NOTATION.md).
4. **Clean Version Control:** LaTeX auxiliary build files (`*.aux`, `*.bbl`, `*.log`, `*.pdf` if generated) should not pollute commits—see `.gitignore` at the repository root.
5. **Pre-Submission Gate:** Every manuscript update must pass the §5 checklist in [`AGENTS.md`](../AGENTS.md).
