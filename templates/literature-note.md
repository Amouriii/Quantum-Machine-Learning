---
citekey: lastnameYYYYkeyword
title: "<Exact Paper Title>"
authors: "<First Author, Second Author, ...>"
year: YYYY
venue: "<Journal, Conference, or Preprint Server>"
identifier: "<DOI: 10.xxxx/xxxxx | arXiv:YYYY.NNNNN>"
focus_areas: []         # foundations | variational-models | learning-primitives | frameworks
verified: false         # Must be true and present in bibliography/references.bib before citing as [ESTABLISHED]
---

<!-- When instantiating into literature/notes/<citekey>.md, update relative paths from ../ to ../../ -->

# <Exact Paper Title> (`lastnameYYYYkeyword`)

## 1. Core Contribution & Relevance to QML/AI

Summarize the paper's central theoretical contribution and why it matters to Quantum Machine Learning and AI ([`AGENTS.md`](../AGENTS.md) §1).

---

## 2. Formal Setup & Assumptions

Map the paper's mathematical notation to [`NOTATION.md`](../NOTATION.md) and list every modeling assumption (e.g., circuit family, data distribution, noise model, oracle access).

| Paper Symbol | Repository Symbol (`NOTATION.md`) | Meaning |
| :--- | :--- | :--- |
| <!-- e.g., $D$ --> | <!-- $L_{\mathrm{depth}}$ --> | <!-- Circuit depth --> |

---

## 3. Key Theorems, Lemmas & Bounds

<!-- Cite exact Section, Theorem/Lemma, and Equation numbers per AGENTS.md §3.4. -->

1. **[ESTABLISHED] `[Author et al., YYYY, Theorem X.Y]`** (Section X, Eq. (Z)):
   - **Statement:** ...
   - **Dependencies / Caveats:** ...

---

## 4. Proof Techniques & Dependencies

- Summarize the core mathematical machinery (e.g., unitary $t$-designs, concentration of measure, Rademacher complexity, tensor rank bounds, query complexity).
- Note key external lemmas the proof relies on (with exact citations).

---

## 5. Limitations & Open Gaps

- Where do the paper's bounds become vacuous, non-constructive, or restricted to idealized assumptions?
- Distinguish claims proven in the paper from informal conjectures or `[OPEN HYPOTHESIS]` observations.

---

## 6. Connections to Repository Research

- Link relevant notes in `research/` (e.g., `research/<focus-area>/<topic-slug>.md`) or entries in `research/OPEN_QUESTIONS.md`.

---

## References

- Primary source (`lastnameYYYYkeyword`): verified entry in [`bibliography/references.bib`](../bibliography/references.bib).

---

## Pre-Submission Checklist (`AGENTS.md` §5)

- [ ] The work directly supports theoretical research in Quantum Machine Learning to advance AI.
- [ ] All repository activities remain strictly within research purposes.
- [ ] Every external claim, theorem, and resource is accurately cited and verified.
- [ ] Mathematical notation is clean, consistent, and rigorously checked (aligned with [`NOTATION.md`](../NOTATION.md)).
- [ ] Any unresolved issues, ambiguities, or unverified assumptions have been clearly flagged for human intervention.
