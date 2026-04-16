# BUILD CONTEXT MATERIAL

## Dev Team Repo Bootstrap

- Target output: one or more `.logitaka/*_CONTEXT_MATERIAL.md` files
- Work only on the current repository and current branch.
- Create or replace the generated files exactly where the builder prompt requires.
- If the builder decides to create zone-specific files, remove any pending placeholder file that no longer reflects the final result.
- Commit and push the generated files to the current branch after the report set is ready.
- Leave this builder file in place; Logitaka will remove it after importing the updated context.

## Builder Prompt

You are extracting zone-based context from an existing code repository.

Your task is to create zone-specific context materials for Logitaka.

---

## GOAL

Extract operational context for each major system zone.

Each zone must produce a separate material file.

This is NOT full documentation.
This is compact, task-relevant context.

---

## STEP 1 — Detect zones

Inspect project structure and identify major zones.

Examples:

- frontend
- backend
- admin
- infra
- shared

Rules:

- Only create zones if they are clearly separated
- If project is small, create a single zone: "core"

---

## STEP 2 — For each zone, extract context

For each detected zone:

### Identify purpose

- what this zone represents (1–2 lines max)

### Identify key modules

- important directories or files
- entry points if visible

Do NOT list everything.

---

### Identify constraints

- important technical rules
- boundaries
- fragile areas

Only include visible constraints.

---

### Identify active areas

- recently changed modules
- areas under development

Use DEVLOG or recent file changes if available.

---

### Identify incomplete/problem areas

- partially implemented modules
- TODO / FIXME (only if relevant)
- missing connections or integrations

Only include obvious cases.

---

## STEP 3 — Create separate files

For each zone, create a separate file:

Format:

# <ZONE NAME> CONTEXT MATERIAL

## PURPOSE

Operational context for this zone.

## ZONE OVERVIEW

(short description)

## KEY MODULES

(list important modules)

## CONSTRAINTS

(list important rules)

## ACTIVE AREAS

(list active parts)

## INCOMPLETE OR PROBLEM AREAS

(list gaps)

---

## STEP 4 — Naming

Use:

- BACKEND_CONTEXT_MATERIAL.md
- FRONTEND_CONTEXT_MATERIAL.md
- INFRA_CONTEXT_MATERIAL.md
- etc.

If only one zone:

- CORE_CONTEXT_MATERIAL.md

---

## RULES

- Do not describe full architecture
- Do not duplicate SYSTEM_MAP
- Do not invent behavior
- Keep each zone compact
- Prefer omission over guessing

---

## CONSTRAINTS

- Each file under ~120 lines
- Bullet points only
- No long explanations
- No business/product context

---

## OUTPUT

Return all generated files.
Each file must be clearly separated.
Do not include explanations outside files.
