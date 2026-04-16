# BUILD SYSTEM MAP

## Dev Team Repo Bootstrap

- Target file: `.logitaka/SYSTEM_MAP.md`
- Work only on the current repository and current branch.
- Replace the target file with the final generated report content.
- Commit and push the generated target file to the current branch after the report is ready.
- Leave this builder file in place; Logitaka will remove it after importing the updated context.

## Builder Prompt

You are initializing a technical system map for an existing code repository.

Your task is to create a SYSTEM_MAP.md file that describes the structure, relationships, and constraints of the system.

---

## GOAL

Create a concise technical map of the system that helps future agents understand:

- how the project is structured
- how main parts are connected
- where boundaries exist
- what rules must be respected

This is NOT a product description.

---

## STEP 1 — Scan structure

- Inspect top-level folders
- Identify main subsystems (frontend, backend, infra, etc.)
- Detect project type (language, framework) using config files

Do NOT analyze full code logic.
Do NOT infer business meaning.

---

## STEP 2 — Identify system components

Define major components:

Examples:

- frontend app
- backend API
- database layer
- worker/jobs
- shared modules
- infra/deployment

Only include clearly identifiable components.

---

## STEP 3 — Identify relationships

Describe how components interact:

- frontend → backend API
- backend → database
- backend → external services
- workers → backend or DB
- shared modules used by multiple parts

Only include relationships that are visible from structure/config.

Do NOT invent flows.

---

## STEP 4 — Identify boundaries

Define clear boundaries:

- what should not directly access what
- separation of concerns
- module isolation (if visible)

Examples:

- frontend must not access DB directly
- API layer separates frontend and data
- env config handled centrally

---

## STEP 5 — Identify critical constraints

List constraints that can break the system if violated:

Examples:

- env variables required
- config files
- build system
- routing entry points
- deployment setup

Only include real constraints.

---

## STEP 6 — Build SYSTEM_MAP.md

Structure must be:

# SYSTEM MAP

## PURPOSE

Explain that this file describes system structure and constraints.

## RULES

- Do not describe business logic
- Do not guess missing parts
- Only include observable structure
- Keep concise

## UPDATE RULES

- Update when structure or architecture changes
- Do not add speculative information
- Remove outdated parts

## Project Type

(language, framework if detected)

## System Components

(list components with short descriptions)

## Relationships

(component → component interactions)

## Boundaries

(what should not cross)

## Constraints

(critical technical rules)

---

## CONSTRAINTS

- Keep under ~200 lines
- Prefer accuracy over completeness
- If unsure — omit
- Do not hallucinate architecture

---

## OUTPUT

Return only SYSTEM_MAP.md content.
Do not include explanations.
