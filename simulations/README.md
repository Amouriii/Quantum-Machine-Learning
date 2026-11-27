# Proof-of-Concept Simulations

Per [`AGENTS.md`](../AGENTS.md) §2, this repository is dedicated to **theoretical QML research**. Numerical simulations are permitted strictly as **proof-of-concept sanity checks, scaling experiments, or counterexample searches supporting theoretical findings**—not as production software engineering or benchmark suites.

---

## Directory Structure

Each numerical experiment must reside in its own subdirectory:

```text
simulations/
├── README.md
└── <experiment-slug>/
    ├── README.md          # Created from templates/simulation-readme.md
    ├── run.py             # Minimal self-contained script (or notebook)
    └── results/           # Small text/CSV/plot summaries only (no large binaries)
```

---

## Mandatory Reproducibility & Scope Rules

1. **Theory-Linked:** Every experiment must reference the exact file and claim ID/tag (`[DERIVED — UNVERIFIED]`, `[CONJECTURE]`, etc.) in `research/` that it tests, using [`templates/simulation-readme.md`](../templates/simulation-readme.md).
2. **Stack-Agnostic & Minimal:** Keep scripts lightweight and declare exact minimal dependencies inside `<experiment-slug>/README.md`. Do not introduce repository-wide CI/CD pipelines, packaging boilerplate, or production tooling.
3. **Deterministic Seeds:** Pin all pseudo-random number generator seeds explicitly and document the exact execution command.
4. **Epistemic Discipline:** Numerical agreement at small system sizes ($n \le 12$ qubits, etc.) provides **empirical evidence only**—it never converts a `[CONJECTURE]` into a proven theorem.
5. **Notation Consistency:** Use variable and observable names matching [`NOTATION.md`](../NOTATION.md) and the linked `research/` note.
