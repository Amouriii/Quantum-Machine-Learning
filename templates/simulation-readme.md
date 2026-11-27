---
experiment: "<experiment-slug>"
linked_research: "research/<focus-area>/<topic-slug>.md"
status: draft           # draft | verified | blocked
seed: 42
---

<!-- When instantiating into simulations/<experiment-slug>/README.md, update relative paths from ../ to ../../ -->

# Simulation: <Experiment Title>

## 1. Theoretical Claim Under Test

- **Linked Note:** `research/<focus-area>/<topic-slug>.md`
- **Target Claim / Conjecture:** Reference the exact `[DERIVED — UNVERIFIED]`, `[CONJECTURE]`, or `[OPEN HYPOTHESIS]` claim being numerically probed.
- **Purpose:** State clearly whether this script checks asymptotic scaling, tests tightness of constants, or searches for counterexamples ([`simulations/README.md`](../simulations/README.md)).

---

## 2. Experimental Setup & Parameters

Keep symbol definitions consistent with [`NOTATION.md`](../NOTATION.md).

- **System sizes / parameters swept:** e.g., $n \in \{2, \dots, 10\}$, depth $L_{\mathrm{depth}}$, sample count.
- **Fixed random seed(s):** `42` (and any secondary seeds).

---

## 3. Dependencies & Reproducibility

- **Minimal Runtime Dependencies:** List exact interpreter and library versions only.
- **Exact Reproduction Command:**
  ```bash
  python run.py --seed 42
  ```

---

## 4. Expected Theoretical Scaling vs. Observed Output

- **Theoretical Prediction:** What scaling or behavior the linked derivation predicts.
- **Observed Numerical Output:** Summarize small-scale results cleanly (remember: numerical agreement does **not** constitute a mathematical proof).

---

## 5. Caveats & Scope Boundaries

- Document finite-size effects, shot-noise approximations, or numerical precision limits.

---

## References

- Linked theoretical note and any verified background entries in `bibliography/references.bib`.

---

## Pre-Submission Checklist (`AGENTS.md` §5)

- [ ] The work directly supports theoretical research in Quantum Machine Learning to advance AI.
- [ ] All repository activities remain strictly within research purposes.
- [ ] Every external claim, theorem, and resource is accurately cited and verified.
- [ ] Mathematical notation is clean, consistent, and rigorously checked (aligned with [`NOTATION.md`](../NOTATION.md)).
- [ ] Any unresolved issues, ambiguities, or unverified assumptions have been clearly flagged for human intervention.
