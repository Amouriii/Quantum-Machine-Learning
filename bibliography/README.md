# Bibliography & Citation Verification Standards

All citations across this repository are governed by the **Mandatory Citation & Attribution Policy** in [`AGENTS.md`](../AGENTS.md) (§3).

---

## Two-Tier Bibliography Architecture

1. **[`references.bib`](references.bib) — Verified Canonical Bibliography:**
   - Contains **only** references whose full bibliographic metadata and persistent identifiers have been directly verified.
   - Zero guessed, memory-recalled, or partial entries are permitted.
2. **[`PENDING_VERIFICATION.md`](PENDING_VERIFICATION.md) — Unverified Citation Quarantine:**
   - Any reference that cannot be directly verified (e.g., paywalled paper, missing DOI/arXiv ID, unconfirmed author list or theorem numbering) must be recorded here and escalated via [`escalations/README.md`](../escalations/README.md) using [`templates/escalation.md`](../templates/escalation.md).
   - Once a human maintainer verifies the entry, move its complete BibTeX record into `references.bib` and update its status in `PENDING_VERIFICATION.md`.

---

## Citekey Convention

Use deterministic, lowercase ASCII citekeys of the form:

```text
<firstauthor><YYYY><keyword>
```

- `<firstauthor>`: Surname of the first author in lowercase ASCII without spaces or diacritics (e.g., `lastname`).
- `<YYYY>`: Four-digit publication or preprint year.
- `<keyword>`: First meaningful content word from the title (skipping articles/prepositions such as `a`, `an`, `the`, `on`, `of`), e.g., `lastnameYYYYkeyword`.
- Disambiguate collisions with an alphabetical suffix: `lastnameYYYYkeyworda`, `lastnameYYYYkeywordb`.

---

## Required BibTeX Fields

Every entry in [`references.bib`](references.bib) must include:

- `author` — Full author list (`Last, First and Last, First`).
- `title` — Exact title (brace-protect mathematical acronyms and proper nouns, e.g., `{QML}`, `{Hilbert}`).
- `year` — Publication or preprint year (`YYYY`).
- Venue — `journal` (for `@article`), `booktitle` (for `@inproceedings`), `publisher` (for `@book`), or `howpublished` / `institution` (for `@misc` / `@techreport`).
- Persistent identifier — `doi` and/or arXiv metadata (`eprint`, `archivePrefix = {arXiv}`, `primaryClass`), plus a stable `url`.
- Verification comment immediately above or inside the entry:
  ```bibtex
  % verified: YYYY-MM-DD by <human-name or verification-source>
  ```

---

## Traceable Inline Citations

When citing a source in `research/`, `literature/`, or `manuscripts/`, include the exact structural anchor (section, theorem, lemma, definition, or equation number) per `AGENTS.md` §3.4:

- Prose format: `[Author et al., YYYY, Theorem X.Y]` or `[Author and Coauthor, YYYY, Eq. (Z)]`
- LaTeX format: `\cite[Theorem~X.Y]{lastnameYYYYkeyword}`
