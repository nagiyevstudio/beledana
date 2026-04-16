# BUILD ROADMAP MATERIAL

## Dev Team Repo Bootstrap

- Target file: `.logitaka/ROADMAP_MATERIAL.md`
- Work only on the current repository and current branch.
- Replace the target file with the final generated report content.
- Commit and push the generated target file to the current branch after the report is ready.
- Leave this builder file in place; Logitaka will remove it after importing the updated context.

## Builder Prompt

You are extracting roadmap signals from an existing code repository.

Your task is NOT to invent a roadmap, but to identify observable directions of development.

---

## GOAL

Create ROADMAP_MATERIAL.md containing raw signals about:

- what is actively being developed
- what is incomplete
- what likely needs continuation

This is NOT a final roadmap.
This is material for further processing.

---

## STEP 1 — Inspect recent changes

Use available sources:

- .logitaka/DEVLOG.md
- recent git changes (if accessible)
- modified files and directories

Identify:

- active areas
- frequently changed modules

---

## STEP 2 — Detect incomplete work

Search for:

- TODO / FIXME / WIP markers
- partially implemented features
- unfinished modules
- placeholder logic
- missing integrations

Only include clearly visible cases.

---

## STEP 3 — Identify development directions

From structure and changes, extract:

- active subsystems (backend, frontend, infra, etc.)
- modules under construction
- areas with recent expansion

---

## STEP 4 — Infer next logical steps (conservative)

Only if strongly implied:

Examples:

- feature partially implemented → continuation needed
- module exists but not connected → integration needed
- config present but incomplete → setup needed

Do NOT invent new features.

---

## STEP 5 — Build ROADMAP_MATERIAL.md

Structure:

# ROADMAP MATERIAL

## PURPOSE

Raw extracted signals about development direction.
Not a final roadmap.

## ACTIVE AREAS

(list areas with ongoing work)

## INCOMPLETE WORK

(list unfinished features/modules)

## IMPLIED NEXT STEPS

(only obvious continuations)

## INFRA / SYSTEM DIRECTIONS

(optional, if relevant)

---

## RULES

- Do not invent features
- Do not describe product vision
- Only include observable signals
- Keep entries short
- Prefer omission over guessing

---

## CONSTRAINTS

- Keep under ~150 lines
- Use bullet points
- Avoid explanations longer than 1–2 lines
- Do not duplicate entries

---

## OUTPUT

Return only ROADMAP_MATERIAL.md content.
