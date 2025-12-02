# Cline Interaction Workflow – Jay’s Systematic Theology

This document describes **how Jay and Cline work together** on theological topics in this repo. It covers:

- The relationship between **chat**, **notes files**, and **normalized doctrine files**.
- A phased workflow for exploring a topic.
- Standard **magic phrases** Jay can use and what Cline should do in response.

The goal is to:
- Preserve **rich exploratory detail** in Markdown (under version control).
- Produce **concise, normalized doctrine files** for each locus.
- Make it easy to **resume work on a topic** across devices and sessions.

---

## 1. Per-topic File Conventions

For each doctrinal topic (e.g., predestination, salvation, problem of evil):

1. **Normalized doctrine file** (public-facing)
   - Name: `topic.md` (e.g., `predestination.md`, `salvation.md`).
   - Structure: follows the **Doctrine File Normalization Pattern** in `systemPatterns.md` and the `doctrine-normalization-template.md`.
   - Purpose: concise, reusable, readable locus-level statement including background, survey, evaluation, adopted position(s), objections, and open questions.

2. **Exploration / notes file** (rich detail)
   - Name: `topic-notes.md` (e.g., `predestination-notes.md`).
   - Content:
     - Rich surveys and comparisons generated in conversation.
     - Clarifying Q&A about sub-issues.
     - Reading lists, tentative ideas, and partially developed arguments.
   - Purpose: preserve detail that would otherwise be lost in a chat thread, while remaining searchable and versioned in Git.

3. **Git as source of truth**
   - Both `topic.md` and `topic-notes.md` live in this repo and are tracked in Git.
   - Switching machines is done by pulling the repo; you do **not** need to find old Cline threads to recover work.

---

## 2. Phased Workflow for a Topic

Each new topic (or major revisiting of a topic) typically moves through these phases. Some phases may overlap or repeat.

### Phase A – Setup (Chat only)

- Jay describes the topic and constraints (e.g., focus, audience, level of technicality).
- Cline:
  - Asks clarifying questions as needed.
  - Sketches the **shape of the terrain**: major families of views, key questions, and important connections to other loci.
- Nothing is written to disk yet; this phase is about orientation.

### Phase B – Define the Option Space (Chat → Notes file)

- Once there is a helpful high-level map of the views and questions, Jay can say:
  - **Magic phrase:** `Create notes file for [topic].`
- Cline (in Act mode, when asked to do so):
  - Creates `[topic]-notes.md` if it doesn’t exist.
  - Seeds it with:
    - A brief overview of the topic.
    - The current best high-level map of major views and key questions.
  - Adds headings for additional sections (e.g., "Questions I care about most", "To read").

### Phase C – Rich Exploration (Chat + Periodic Snapshots)

- Jay and Cline continue in dialogue, exploring details, asking follow-up questions, and refining distinctions.
- Whenever a response is particularly valuable (e.g., a nuanced survey, a careful comparison, a detailed argument), Jay can say:
  - **Magic phrase:** `Snapshot this to [topic]-notes under [heading].`
- Cline then:
  - Opens `[topic]-notes.md`.
  - Creates or finds the requested heading.
  - Appends the relevant material (usually the last substantive response, plus any specified context) under that heading.
  - Optionally timestamps or annotates the snapshot if requested.

This phase may repeat many times as the notes grow.

### Phase D – Draft a Normalized Doctrine File

- When Jay begins to converge on a position for the topic, or wants a structured summary, he can say:
  - **Magic phrase:** `Draft a normalized doctrine file for [topic] from the notes.`
- Cline (in Act mode):
  - Uses the structure from `doctrine-normalization-template.md` (and the description in `systemPatterns.md`).
  - Reads `[topic]-notes.md` (and relevant locus files) as the primary source of detail.
  - Creates or overwrites `topic.md` with:
    - The normalized headings.
    - A clear **Adopted Position(s)** section (marked as provisional if appropriate).
    - An **Objections and Responses** section and an **Open Questions / Deferred Issues** section.
  - Ensures cross-links to related loci (e.g., predestination ↔ salvation ↔ problem of evil ↔ God and time).

### Phase E – Maintenance and Revision

- Over time, Jay may change his mind, refine arguments, or read new sources.
- He can:
  - Continue using the notes file for deeper exploration.
  - Ask for the doctrine file to be updated, e.g.:
    - **Magic phrase:** `Update the doctrine file for [topic] from the notes.`
- Cline (in Act mode):
  - Reviews `[topic]-notes.md` and `topic.md`.
  - Adjusts `topic.md` to reflect current thinking, without erasing the survey → evaluate → adopt/defer structure.
  - Preserves old content where possible by relocating or annotating rather than deleting, unless Jay explicitly requests pruning.

---

## 3. Magic Phrases and Their Effects

These phrases are not special commands at the platform level, but Cline should treat them as explicit workflow triggers.

### 3.1 Create a Notes File

- **Phrase:** `Create notes file for [topic].`
- **Effect:**
  - In Act mode, Cline creates `[topic]-notes.md` (if absent).
  - Seeds it with:
    - A short overview of the topic.
    - A summary of major views and key questions developed so far.
  - Adds any obviously useful scaffold sections (e.g., "Major Views", "Key Questions", "To Read").

### 3.2 Snapshot Rich Content into Notes

- **Phrase:** `Snapshot this to [topic]-notes under [heading].`
- **Effect:**
  - Cline appends the last substantial response (or specifically identified content) to `[topic]-notes.md` under the named heading.
  - Creates the heading if necessary.
  - May add a brief note such as "Snapshot from conversation on [date]" if requested.

### 3.3 Draft a Normalized Doctrine File

- **Phrase:** `Draft a normalized doctrine file for [topic] from the notes.`
- **Effect:**
  - Cline uses the doctrine normalization pattern and template to create or rework `topic.md` from `[topic]-notes.md` and relevant context.
  - Ensures:
    - Background and biblical foundations.
    - Survey of major views.
    - Evaluation and arguments (provisional).
    - Adopted position(s) (clearly labeled, often provisional).
    - Implications/pastoral considerations (optional).
    - Objections and responses.
    - Open questions / deferred issues.

### 3.4 Update an Existing Doctrine File from Notes

- **Phrase:** `Update the doctrine file for [topic] from the notes.`
- **Effect:**
  - Cline treats `topic.md` as already normalized.
  - Reads `[topic]-notes.md` for newer insights, shifts, or clarifications.
  - Revises `topic.md` to reflect current adopted positions and arguments, maintaining the normalized structure.

### 3.5 Re-list the Live Options

- **Phrase:** `List the live options for [topic] again.`
- **Effect:**
  - Cline, usually in Plan mode, re-summarizes the main views under consideration for the topic, based on notes and prior discussion.
  - This helps Jay re-orient without digging through long transcripts.

### 3.6 Start a New Exploration Pass

- **Phrase:** `Start a new exploration pass for [topic].`
- **Effect:**
  - Cline marks that a new sub-thread of exploration is beginning (e.g., focused on a sub-question or a new author).
  - May create a new section in `[topic]-notes.md` to collect this pass (e.g., "Exploration Pass – [date] – [subtopic]").

### 3.7 Pick Up Our Work on a Topic

- **Phrase:** `Pick up our work on [topic].`
- **Intended use:** After switching devices or returning after a break.
- **Effect:**
  - In Plan mode (initially), Cline should:
    1. Perform the usual read of the memory bank core files to rebuild project context.
    2. Look for `topic.md` and `[topic]-notes.md`.
    3. Read both files to understand the current state of the locus and any notes.
    4. Provide a brief **status summary**:
       - What the adopted position (if any) currently is in `topic.md`.
       - What major threads are present in `[topic]-notes.md`.
       - Any obvious open questions or TODOs.
    5. Propose next-step options (e.g., continue exploration, snapshot more content, or update the doctrine file).
  - Once Jay chooses a direction and toggles to Act mode (if needed), Cline carries out the requested action using the patterns above.

---

## 4. Using `newtask` with This Workflow

The `newtask` command is useful when you want to start a **fresh, session-sized unit of work** that has its own plan and history, while still drawing on the existing memory bank and topic files.

Use `newtask` especially in these situations:

### 4.1 Starting a New Topic

When you begin work on a new doctrinal locus or major subtopic (e.g., moving from predestination to the problem of evil):

- Create a new task with a short description such as:
  - "Explore the problem of evil using our notes/doctrine workflow."
- In that new task, Cline will:
  - Re-read the memory bank core files.
  - Check for `topic.md` and `topic-notes.md`.
  - Proceed with Phase A/B (Setup → Define the option space) for that topic.

### 4.2 Beginning a Major New Phase on an Existing Topic

Use `newtask` when you shift to a qualitatively different phase of work on the same topic, for example:

- Moving from **exploration** to **normalization**:
  - e.g., "Draft a normalized doctrine file for [topic] from the notes."
- Moving from **normalization** to **cross-locus integration**:
  - e.g., "Review how predestination, salvation, and problem of evil fit together and tighten cross-links."

This keeps each phase’s plan and history clear and self-contained.

### 4.3 After a Long Break or Conceptual Shift

After a long gap or a significant change in your overall method/goals, start a new task so Cline can:

- Summarize what has been done so far.
- Rebuild a fresh plan for the next block of work.

You can combine this with the magic phrase **"Pick up our work on [topic]"** inside the new task. Cline will then:

1. Re-read the memory bank.
2. Read `topic.md` and `topic-notes.md`.
3. Summarize the current state and suggest next steps.

### 4.4 Granularity Guidelines

- Use **magic phrases** within a task to move between phases (create notes, snapshot, draft doctrine, update doctrine, pick up work, etc.).
- Use **`newtask`** when you want:
  - A new, focused plan and conversation history, or
  - To treat a new topic or major phase as a distinct unit of work.

A reasonable default is 1–3 tasks per topic, for example:

- Task 1: Explore the topic and create/populate `[topic]-notes.md`.
- Task 2: Draft the normalized `topic.md` from the notes.
- Task 3 (optional): Revisit the topic later to update the doctrine file after further study.

---

## 5. Relationship to Other Memory-Bank Files

- `systemPatterns.md` defines the **content patterns** (e.g., Doctrine File Normalization Pattern).
- `doctrine-normalization-template.md` provides a **copy-pasteable skeleton** for normalized doctrine files.
- `activeContext.md` describes the **current areas of focus** (e.g., which loci to normalize next).
- `techContext.md` describes the **technical setup** (markdown-only, Git-based, etc.).

This `cline-workflow.md` file sits alongside them to describe the **interaction workflow** between Jay and Cline, including the magic phrases and when to move from chat to Markdown and back.
