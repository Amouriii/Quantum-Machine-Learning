# Quantum Machine Learning — Theoretical Research Repository

This repository hosts **theoretical research applying quantum computation to machine learning (Quantum Machine Learning, or QML) to advance Artificial Intelligence (AI)**. All contributions—human or AI-assisted—operate under the mandatory governance, citation integrity, and escalation rules defined in [`AGENTS.md`](AGENTS.md).

---

## Repository Structure

```text
Quantum-Machine-Learning/
├── AGENTS.md                         # Mandatory operating principles, citation rules & routing
├── README.md                         # Research overview, epistemic legend & contribution workflows
├── NOTATION.md                       # Canonical LaTeX & mathematical conventions
├── .gitignore                        # LaTeX build outputs, Python/Jupyter caches, OS files
├── .github/
│   └── PULL_REQUEST_TEMPLATE.md      # Pre-submission review checklist (§5 of AGENTS.md)
├── bibliography/
│   ├── README.md                     # Citekey standard, required fields & verification rules
│   ├── references.bib                # Canonical BibTeX bibliography (verified entries only)
│   └── PENDING_VERIFICATION.md       # Quarantine queue for unverified/paywalled sources
├── literature/
│   ├── README.md                     # Literature note & thematic survey conventions
│   ├── notes/                        # Per-paper notes keyed 1:1 to bibliography citekeys
│   └── reviews/                      # Comparative surveys across multiple works
├── research/
│   ├── OPEN_QUESTIONS.md             # Central registry of conjectures & open hypotheses
│   ├── foundations/                  # Complexity, expressivity, generalization, sample complexity
│   ├── variational-models/           # Ansatz design, barren plateaus, trainability, landscapes
│   ├── learning-primitives/          # Quantum kernels, QNNs, tensor networks, QML-inspired models
│   └── frameworks/                   # Cross-cutting formal proofs, scaling & info-theoretic limits
├── simulations/
│   └── README.md                     # Proof-of-concept numerical checks supporting theory
├── manuscripts/
│   └── README.md                     # Formal LaTeX (.tex) drafts built from verified results
├── escalations/
│   ├── README.md                     # Human intervention protocol & ticket lifecycle
│   └── resolved/                     # Archived escalations with recorded human decisions
└── templates/
    ├── research-note.md              # Template for research/ derivations
    ├── literature-note.md            # Template for literature/notes/ summaries
    ├── simulation-readme.md          # Template for simulations/<experiment-slug>/README.md
    └── escalation.md                 # Template for escalations/ESC-NNN-<slug>.md
```

---

## Epistemic Labels & Document Status

To strictly separate established theorems, original proofs, and speculative ideas (see [`AGENTS.md`](AGENTS.md) §2):

### Claim-Level Tags
- `[ESTABLISHED]` — Proven result from verified literature; must carry an inline citation with exact section/theorem/equation anchor (`[Author et al., YYYY, Theorem X.Y]`).
- `[DERIVED — UNVERIFIED]` — New derivation or proof pending review.
- `[DERIVED — VERIFIED]` — Original derivation verified and accepted by a human maintainer.
- `[CONJECTURE]` — Stated mathematical conjecture without a complete proof.
- `[OPEN HYPOTHESIS]` — Exploratory research question or unverified working assumption.

### Note-Level Frontmatter `status`
- `draft` — Work in progress; derivations or citations incomplete.
- `in-review` — Complete draft ready for verification against §5 checklist.
- `verified` — All proofs, notation, and citations reviewed and accepted.
- `blocked` — Halted due to an unresolved issue; `blocker` must link to an open ticket in `escalations/`.

---

## Quick-Start Workflows

1. **Verifying & Adding Literature:**
   - Verify full bibliographic metadata and persistent identifier (DOI, arXiv ID, or stable URL) using [`bibliography/README.md`](bibliography/README.md).
   - Add verified BibTeX entries to [`bibliography/references.bib`](bibliography/references.bib) using citekey format `firstauthorYYYYkeyword`.
   - Create a structured note at `literature/notes/<citekey>.md` from [`templates/literature-note.md`](templates/literature-note.md).
   - If a source cannot be verified or accessed, log it in [`bibliography/PENDING_VERIFICATION.md`](bibliography/PENDING_VERIFICATION.md) and open an escalation instead of adding it to `references.bib`.

2. **Authoring Theoretical Research:**
   - Choose the matching focus area under `research/`:
     - [`foundations/`](research/foundations/README.md)
     - [`variational-models/`](research/variational-models/README.md)
     - [`learning-primitives/`](research/learning-primitives/README.md)
     - [`frameworks/`](research/frameworks/README.md)
   - Start topics as a single file `research/<focus-area>/<topic-slug>.md` copied from [`templates/research-note.md`](templates/research-note.md). Promote to a folder `research/<focus-area>/<topic-slug>/index.md` with sub-files only when a line of work grows multi-part.
   - Adhere strictly to [`NOTATION.md`](NOTATION.md) and log open problems in [`research/OPEN_QUESTIONS.md`](research/OPEN_QUESTIONS.md).

3. **Supporting Proof-of-Concept Simulations:**
   - Place numerical verification scripts under `simulations/<experiment-slug>/` following [`simulations/README.md`](simulations/README.md) and [`templates/simulation-readme.md`](templates/simulation-readme.md).
   - Every simulation must declare the exact `research/` claim it tests and pin random seeds for reproducibility.

4. **Escalating Blockers:**
   - Whenever encountering mathematical blockers, unverified citations, scope ambiguity, or repository errors, follow [`escalations/README.md`](escalations/README.md) and create `escalations/ESC-NNN-<slug>.md` from [`templates/escalation.md`](templates/escalation.md).

5. **Drafting Manuscripts:**
   - Assemble verified results from `research/` into formal LaTeX drafts under `manuscripts/<manuscript-slug>/` following [`manuscripts/README.md`](manuscripts/README.md).

---

## Governance & Conventions

- Mandatory agent principles and §5 Pre-Submission Checklist: [`AGENTS.md`](AGENTS.md)
- Canonical mathematical & LaTeX notation: [`NOTATION.md`](NOTATION.md)
- Pull request review template: [`.github/PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md)
