---
title: "<Concise Research Topic Title>"
focus_area: foundations # foundations | variational-models | learning-primitives | frameworks
status: draft           # draft | in-review | verified | blocked
blocker: null           # e.g., escalations/ESC-NNN-<slug>.md when status is blocked
citations_verified: false
created: YYYY-MM-DD
updated: YYYY-MM-DD
---

<!-- When instantiating into research/<focus-area>/<topic-slug>.md, update relative paths from ../ to ../../ -->

# <Concise Research Topic Title>

## 1. Research Question & Scope

State the exact theoretical question, how it advances QML/AI research ([`AGENTS.md`](../AGENTS.md) §1), and what is explicitly out of scope.

---

## 2. Notation & Assumptions

Follow [`NOTATION.md`](../NOTATION.md). Declare any additional symbols or local overrides explicitly before stating definitions or theorems.

- **Hilbert space / architecture:** e.g., $\mathcal{H}_n = (\mathbb{C}^2)^{\otimes n}$, parameterized circuit $U(\boldsymbol{\theta})$.
- **Standing assumptions:** (List all regularity, distribution, noise, or oracle assumptions clearly.)

---

## 3. Established Background

<!-- Every claim here MUST carry [ESTABLISHED] and cite a verified entry in bibliography/references.bib with exact section/theorem/equation anchor. -->

- **[ESTABLISHED]** *(Placeholder statement)* — `[Author et al., YYYY, Theorem X.Y]` (`lastnameYYYYkeyword`).

---

## 4. Theoretical Results & Derivations

### Result 1 — [DERIVED — UNVERIFIED] <Theorem / Lemma / Proposition Title>

**Statement.** State the precise mathematical claim, explicitly listing all hypotheses and asymptotic dependencies.

**Proof.**
Provide step-by-step derivation. Cite external lemmas with exact anchors (`[Author et al., YYYY, Lemma X.Y]`).

$$\text{(Display equations here)}$$

$\square$

### Conjecture / Hypothesis — [CONJECTURE] or [OPEN HYPOTHESIS] <Title>

**Statement.** State the conjectured bound or open hypothesis. Also log this item in [`research/OPEN_QUESTIONS.md`](../research/OPEN_QUESTIONS.md).

---

## 5. Limitations, Edge Cases & Open Questions

- Identify boundary regimes where the argument weakens or breaks down.
- List open follow-up questions (cross-referenced with `OQ-NNN` IDs in [`research/OPEN_QUESTIONS.md`](../research/OPEN_QUESTIONS.md)).
- If a mathematical or verification blocker halts progress, set `status: blocked` in frontmatter and open a ticket in `escalations/`.

---

## 6. Supporting Simulations

<!-- Optional: link proof-of-concept numerical checks under simulations/ (see simulations/README.md). -->

- None yet (`simulations/README.md`: [`simulations/README.md`](../simulations/README.md)).

---

## References

<!-- Every cited entry must match a verified entry in ../bibliography/references.bib -->

- `lastnameYYYYkeyword`: Author(s) (YYYY). *Exact Title*. Venue. DOI / arXiv: `10.xxxx/xxxxx` / `arXiv:YYYY.NNNNN`. (See [`references.bib`](../bibliography/references.bib).)

---

## Pre-Submission Checklist (`AGENTS.md` §5)

- [ ] The work directly supports theoretical research in Quantum Machine Learning to advance AI.
- [ ] All repository activities remain strictly within research purposes.
- [ ] Every external claim, theorem, and resource is accurately cited and verified.
- [ ] Mathematical notation is clean, consistent, and rigorously checked (aligned with [`NOTATION.md`](../NOTATION.md)).
- [ ] Any unresolved issues, ambiguities, or unverified assumptions have been clearly flagged for human intervention.
