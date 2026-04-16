# BUILD INDEX

## Dev Team Repo Bootstrap

- Target file: `.logitaka/INDEX.md`
- Work only on the current repository and current branch.
- Replace the target file with the final generated report content.
- Commit and push the generated target file to the current branch after the report is ready.
- Leave this builder file in place; Logitaka will remove it after importing the updated context.

## Builder Prompt

You are initializing a navigation index for an existing code repository.

Your task is to create a concise INDEX.md file that helps future agents quickly navigate the project.

---

## GOAL

Create a navigation router for the project.

The index must:

- show where important parts of the system are located
- highlight entry points and critical files
- group the project into logical zones
- avoid listing all files

---

## STEP 1 — Scan project structure

- List top-level directories
- Identify main code areas (frontend, backend, admin, infra, etc.)
- Detect project type using common files (package.json, requirements.txt, etc.)

Do NOT read all files. Focus on structure and filenames.

---

## STEP 2 — Identify key zones

Group the project into high-level zones:

Examples:

- frontend
- backend
- admin
- infra
- shared
- scripts
- docs (only if useful)

Only include meaningful zones.

---

## STEP 3 — Identify entry points

Find main entry files such as:

- app entry (main.tsx, index.tsx, app.js, etc.)
- server entry (server.ts, main.py, etc.)
- routing files
- main config files
- environment config

Only include critical entry points.

---

## STEP 4 — Identify critical system areas

Find important directories that define core behavior:

Examples:

- auth
- workflows
- api layer
- storage
- state management

Only include if clearly important.

---

## STEP 5 — Build INDEX.md

Structure must be:

# INDEX

## PURPOSE

Explain that this file is a navigation router, not a full file list.

## RULES

- Include only high-value paths
- Do not list all files
- Keep file short
- Prefer zones and entry points
- Avoid explanations of business logic

## UPDATE RULES

- Update when structure changes
- Add only meaningful entries
- Remove stale paths

## Logitaka Files

- .logitaka/SYSTEM_MAP.md
- .logitaka/DEVLOG.md

## Main Code Zones

(list zones with short descriptions)

## Key Entry Points

(list entry files)

## Critical System Areas

(optional, only if needed)

---

## CONSTRAINTS

- Keep total length under ~150 lines
- Prefer clarity over completeness
- Do not guess business logic
- Do not invent files that do not exist

---

## OUTPUT

Return only the final INDEX.md content.
Do not include explanations.
