# Literature Notes & Thematic Reviews

This directory houses structured analyses of external Quantum Machine Learning and quantum information literature supporting the repository's theoretical mission ([`AGENTS.md`](../AGENTS.md)).

---

## Directory Layout

- `notes/` — Individual per-paper notes, named strictly after their verified BibTeX citekey:
  - Filename format: `literature/notes/<citekey>.md` (e.g., `lastnameYYYYkeyword.md`).
  - Instantiate from [`templates/literature-note.md`](../templates/literature-note.md).
- `reviews/` — Cross-paper thematic surveys, comparative assumption tables, and synthesis reports:
  - Filename format: `literature/reviews/<topic-slug>.md`.

---

## Authoring Standards

1. **Verified Bibliography First:** Every paper summarized in `notes/` must have a verified entry in [`bibliography/references.bib`](../bibliography/references.bib). If verification is incomplete or blocked by a paywall, log the citation in [`bibliography/PENDING_VERIFICATION.md`](../bibliography/PENDING_VERIFICATION.md) and escalate before citing it as established.
2. **Traceable Anchors (`AGENTS.md` §3.4):** Every extracted theorem, lemma, bound, or definition must cite the exact section, theorem/lemma number, and equation number (e.g., `[Author et al., YYYY, Theorem X.Y]`).
3. **Separate External Claims from Commentary (`AGENTS.md` §2):** Clearly distinguish verbatim/restated claims of the paper (`[ESTABLISHED]`) from your own critique, proof gaps, or conjectures (`[CONJECTURE]` / `[OPEN HYPOTHESIS]`).
4. **Notation Alignment:** Map any paper-specific symbols to [`NOTATION.md`](../NOTATION.md) in the note's **Formal Setup & Assumptions** section.
