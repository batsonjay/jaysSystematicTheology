# System Patterns – Jay’s Systematic Theology

This project is **not a software system** but a structured body of theological writing. "Patterns" here refer to how the content is organized and developed over time.

## Content Architecture

- **One file per major locus or subtopic** where practical (e.g., `existence-of-god.md`, `salvation.md`, `God-and-time.md`).
- A **high-level outline** in [`../../high-level-outline.md`](../../high-level-outline.md) (when present) and the root [`../../README.md`](../../README.md) guides what topics belong in the system.
- Each doctrinal locus file may:
  - Survey multiple views (historical, philosophical, doctrinal).
  - Mark which views are **adopted**, which are **rejected**, and which are **deferred**.
  - Evolve over time as study continues.

## Methodological Patterns

- **Survey → Evaluate → Adopt/Defer** is the recurring pattern:
  - Gather representative positions.
  - Weigh them in light of Scripture, tradition, reason, and experience.
  - Explicitly state which view(s) are adopted and why.
  - Note alternatives that remain open questions.
- **Humble revision** is expected; documents are living, not final.

## Document Conventions (Intent)

These conventions describe the *intended* style; the actual files may not always match perfectly but should trend in this direction over time:

- Use clear sectioning (e.g., background, survey of views, arguments, objections, adopted position, open questions).
- Prefer **explicit labels** where helpful, such as:
  - “Adopted view”
  - “Deferred / open question”
- Keep tone charitable and historically informed, reflecting the aims described in the memory-bank `productContext.md`.

## Doctrine File Normalization Pattern

For locus-level doctrine files (e.g., `predestination.md`, `salvation.md`, `problem-of-evil.md`, `God-and-time.md`), the default **normalized structure** is:

1. **Background and biblical foundations**
2. **Survey of major views**
3. **Evaluation and arguments**
4. **Adopted position(s)**
5. **Implications / pastoral considerations** (optional but encouraged)
6. **Objections and responses**
7. **Open questions / deferred issues**

When **normalizing** a doctrine file, the assistant should:

- Preserve all substantive content, relocating it under these headings rather than deleting it.
- Make the **survey → evaluate → adopt/defer** pattern explicit in the sectioning and labels.
- Mark the **adopted view** clearly (even if provisional) and keep room for revision.
- Add or strengthen cross-links to closely related loci where helpful (e.g., predestination ↔ salvation ↔ problem of evil ↔ God and time, anthropology, divine attributes).
- Clearly label sections or bullets that are still **in progress** or **deferred/open questions**.

Normalizing is about bringing a file into a **clear, reusable spine**, not about forcing premature closure on contested doctrines.

## How Cline Should Use This File

- Use these patterns to keep new or edited documents structurally consistent.
- When adding content, ask:
  - Does this follow the *survey → evaluate → adopt/defer* pattern where appropriate?
  - Is it clear what is **adopted** vs. **still under exploration**?
- When a doctrine file’s structure is jumbled or ad hoc, **normalize** it to the standard outline above, preserving content and marking open questions.
- When in doubt about overall structure, consult:

  - [`README.md`](../../README.md)
  - [`high-level-outline.md`](../../high-level-outline.md) (if present).
