# Agent Guidelines

Welcome to this research repository. This document defines the mandatory operating principles, research scope, citation standards, and escalation procedures for all AI agents contributing to or interacting with this workspace.

---

## 1. Research Scope & Mission

This repository is dedicated exclusively to **theoretical research applying quantum computation to machine learning (Quantum Machine Learning, or QML) in order to advance Artificial Intelligence (AI) research**.

### Core Focus Areas
Agents should align all investigations, literature reviews, derivations, and conceptual architectures with this mission, including but not limited to:
- **Quantum Computational Foundations for AI:** Complexity-theoretic advantages, expressivity, generalization bounds, and sample complexity of quantum models relative to classical baselines.
- **Variational & Parameterized Quantum Models:** Theoretical analysis of ansatz design, barren plateaus, trainability, and optimization landscapes.
- **Quantum Linear Algebra & Learning Primitives:** Quantum kernel methods, quantum neural networks (QNNs), tensor network connections, and quantum-inspired classical algorithms.
- **Theoretical Frameworks:** Formal proofs, asymptotic scaling analyses, information-theoretic limits, and rigorous mathematical modeling using standard LaTeX notation (e.g., $|\psi\rangle$, $\mathcal{O}(n \log n)$).

---

## 2. Repository Usage Policy

- **Research Purposes Only:** This repository must be used strictly for scholarly research, theoretical exploration, formal documentation, literature synthesis, and proof-of-concept simulations supporting theoretical findings.
- **No Unverified Claims:** Clearly distinguish between established theorems, derived proofs, conjectures, and open hypotheses. Never present speculative ideas as proven results.
- **Structured Contributions:** Keep research notes, derivations, bibliography files, and supporting scripts well-organized, cleanly documented, and reproducible.
- **Scope Discipline:** Do not introduce unrelated software engineering tasks, commercial/production tooling, or non-research artifacts unless explicitly instructed by a human maintainer.

---

## 3. Mandatory Citation & Attribution Policy

Rigorous academic integrity is non-negotiable. **All agents must cite their resources.**

1. **Cite Every External Source:** Every theorem, definition, lemma, prior result, benchmark, or conceptual framework drawn from external literature must include an explicit citation.
2. **Required Citation Details:** Where available, provide full bibliographic metadata:
   - Author(s) and publication year
   - Title of the paper, book, or technical report
   - Venue (journal, conference, or preprint server)
   - Persistent identifier (e.g., DOI, arXiv ID, or stable URL)
3. **Zero Fabricated References:** Never guess, approximate, or hallucinate citations, DOIs, arXiv identifiers, or quotes. If you cannot verify a reference directly, flag it explicitly and request human verification.
4. **Traceable Reasoning:** When adapting an existing proof or equation from a source, reference the exact section, theorem, or equation number (e.g., `[Author et al., 2024, Theorem 3.2]`).
5. **Centralized Bibliography:** Maintain consistent formatting (such as BibTeX entries in a shared `references.bib` or a structured `References` section at the end of each document).

---

## 4. Issue Escalation & Human Intervention Protocol

Agents are **not** expected to force a resolution when facing uncertainty or blockers. **Whenever you encounter an issue, pause and ask for human intervention.**

### When to Escalate Immediately
Request human input if you encounter any of the following:
- **Mathematical or Theoretical Blockers:** Unresolvable steps in a proof, conflicting assumptions, edge cases where an argument breaks down, or ambiguous problem formulations.
- **Citation & Verification Issues:** Inability to verify a source, paywalled/inaccessible literature, or contradictory claims across referenced papers.
- **Scope or Direction Ambiguity:** Uncertainty about whether a research direction aligns with the repository's goals or priorities.
- **Technical & Repository Errors:** Failing scripts, missing dependencies, merge conflicts, permission issues, or corrupted files.
- **Safety, Ethics, or Policy Concerns:** Any situation that may violate licensing, academic integrity, or repository rules.

### How to Request Intervention
When escalating an issue, provide a concise, structured summary containing:
1. **Context:** What task or research question you were working on.
2. **The Issue:** A precise description of the error, ambiguity, or mathematical bottleneck.
3. **What Was Tried:** Steps, derivations, or checks already performed.
4. **Proposed Options / Questions:** Specific questions or candidate paths forward for the human researcher to review and decide upon.

Do **not** silently work around critical blockers by making unverified assumptions or altering core hypotheses without approval.

---

## 5. Pre-Submission Checklist for Agents

Before finalizing any contribution or commit, verify the following:
- [ ] The work directly supports theoretical research in Quantum Machine Learning to advance AI.
- [ ] All repository activities remain strictly within research purposes.
- [ ] Every external claim, theorem, and resource is accurately cited and verified.
- [ ] Mathematical notation is clean, consistent, and rigorously checked.
- [ ] Any unresolved issues, ambiguities, or unverified assumptions have been clearly flagged for human intervention.

---

## 6. Repository Structure & Operational Conventions

All contributions must conform to the repository layout and conventions below. For full background on any component, read the corresponding `README.md` or template before creating files.

### Directory Routing

| Artifact Type | Target Location | Template / Guide |
| :--- | :--- | :--- |
| Mathematical conventions | [`NOTATION.md`](NOTATION.md) | Repository-wide LaTeX standard |
| Original theory (`foundations`) | `research/foundations/` | [`research/foundations/README.md`](research/foundations/README.md), [`templates/research-note.md`](templates/research-note.md) |
| Original theory (`variational-models`) | `research/variational-models/` | [`research/variational-models/README.md`](research/variational-models/README.md), [`templates/research-note.md`](templates/research-note.md) |
| Original theory (`learning-primitives`) | `research/learning-primitives/` | [`research/learning-primitives/README.md`](research/learning-primitives/README.md), [`templates/research-note.md`](templates/research-note.md) |
| Original theory (`frameworks`) | `research/frameworks/` | [`research/frameworks/README.md`](research/frameworks/README.md), [`templates/research-note.md`](templates/research-note.md) |
| Conjectures & open questions | [`research/OPEN_QUESTIONS.md`](research/OPEN_QUESTIONS.md) | Registry separating open problems from verified proofs |
| Per-paper literature notes | `literature/notes/<citekey>.md` | [`literature/README.md`](literature/README.md), [`templates/literature-note.md`](templates/literature-note.md) |
| Thematic literature reviews | `literature/reviews/<topic-slug>.md` | [`literature/README.md`](literature/README.md) |
| Verified BibTeX bibliography | [`bibliography/references.bib`](bibliography/references.bib) | [`bibliography/README.md`](bibliography/README.md) |
| Unverified citation quarantine | [`bibliography/PENDING_VERIFICATION.md`](bibliography/PENDING_VERIFICATION.md) | [`bibliography/README.md`](bibliography/README.md) |
| Proof-of-concept simulations | `simulations/<experiment-slug>/` | [`simulations/README.md`](simulations/README.md), [`templates/simulation-readme.md`](templates/simulation-readme.md) |
| Formal LaTeX manuscripts | `manuscripts/<manuscript-slug>/` | [`manuscripts/README.md`](manuscripts/README.md) |
| Human escalation tickets | `escalations/ESC-NNN-<slug>.md` | [`escalations/README.md`](escalations/README.md), [`templates/escalation.md`](templates/escalation.md) |

### Mandatory Operational Rules

1. **Notation Consistency:** Follow [`NOTATION.md`](NOTATION.md) for all mathematical symbols, quantum states, norms, and complexity classes. Any local deviation must be declared explicitly in the document's notation section.
2. **Epistemic Labeling:** Every mathematical claim in `research/` must be prefixed with one of the standard labels:
   - `[ESTABLISHED]` — Known result from verified external literature; must carry an inline citation with exact anchor (`[Author et al., YYYY, Theorem X.Y]`).
   - `[DERIVED — UNVERIFIED]` — Original derivation awaiting independent verification or human review.
   - `[DERIVED — VERIFIED]` — Original derivation checked and accepted by a human maintainer.
   - `[CONJECTURE]` — Plausible theoretical claim supported by partial evidence or intuition, not yet proved.
   - `[OPEN HYPOTHESIS]` — Unproven hypothesis or research direction requiring investigation.
   Also register conjectures and open hypotheses in [`research/OPEN_QUESTIONS.md`](research/OPEN_QUESTIONS.md).
3. **Zero Unverified Bibliography Entries:** Never insert an unverified, memory-recalled, or incomplete citation into [`bibliography/references.bib`](bibliography/references.bib). Instead:
   - Log the candidate citation in [`bibliography/PENDING_VERIFICATION.md`](bibliography/PENDING_VERIFICATION.md), and
   - Open an escalation ticket `escalations/ESC-NNN-<slug>.md` using [`templates/escalation.md`](templates/escalation.md).
4. **Blocker Flagging:** Whenever an escalation blocks progress on a research note, set `status: blocked` and `blocker: escalations/ESC-NNN-<slug>.md` in the affected note's YAML frontmatter and pause work on the blocked line of reasoning until a human decision is recorded.
