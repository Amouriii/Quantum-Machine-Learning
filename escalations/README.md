# Human Escalation & Intervention Inbox

This directory implements the **Issue Escalation & Human Intervention Protocol** mandated by [`AGENTS.md`](../AGENTS.md) §4.

> **Core Principle:** Agents must **never** silently guess, fabricate citations, alter core hypotheses, or force unverified workarounds past a blocker. Whenever uncertainty or a blocker arises, pause, document it here, and wait for human review.

---

## Escalation Categories (`AGENTS.md` §4)

1. `mathematical-blocker` — Unresolvable proof steps, conflicting assumptions, broken edge cases, or ambiguous problem formulations.
2. `citation-verification` — Unverifiable bibliographic metadata, paywalled/inaccessible sources, or contradictory claims across papers (cross-link [`bibliography/PENDING_VERIFICATION.md`](../bibliography/PENDING_VERIFICATION.md)).
3. `scope-ambiguity` — Uncertainty over whether a research question or method fits the repository's QML-for-AI mission.
4. `technical-error` — Failing simulation scripts, missing dependencies, merge conflicts, permission errors, or corrupted files.
5. `policy-ethics` — Potential licensing, academic integrity, or repository policy concerns.

---

## Ticket Naming & Lifecycle

1. **Create Ticket:** Name files sequentially:
   ```text
   escalations/ESC-NNN-<short-slug>.md
   ```
   (e.g., `ESC-001-barren-plateau-measure-assumption.md`) using [`templates/escalation.md`](../templates/escalation.md), containing all four required sections (`Context`, `The Issue`, `What Was Tried`, `Proposed Options / Questions`).
2. **Flag Blocked Work:** In any affected `research/` note, update the YAML frontmatter:
   ```yaml
   status: blocked
   blocker: escalations/ESC-NNN-<short-slug>.md
   ```
3. **Pause & Notify:** Surface the escalation summary concisely to the human researcher and halt work on the blocked derivation or citation.
4. **Resolve & Archive:** Once a human decision is recorded under `## 5. Human Resolution`, update `status: resolved` in the ticket frontmatter, move the file into `escalations/resolved/`, and clear the `blocker` field on the affected research note.
