# SYSTEM MAP

## PURPOSE

This file describes the system structure, components, and technical constraints of the BeleDana project. It serves as a technical reference for understanding the organizational layout and design boundaries.

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

- **Project Category**: Architectural Specification & Documentation
- **Primary Medium**: Markdown
- **Target Implementation Environment**: n8n, Docker, AI Agents

## System Components

- **Documentation Hub (`docs/`)**: The primary repository of truth for the system philosophy, methodology, and implementation roadmap.
- **Logitaka Context Layer (`.logitaka/`)**: The metadata and automation layer used to maintain the project's state, context, and development logs.
- **Logitaka Builders (`.logitaka/builders/`)**: Orchestration files and templates used to generate or refresh project metadata and documentation.

## Relationships

- **Logitaka Builders → Logitaka Metadata**: Builders contain the logic for generating and updating the project's core metadata files (`INDEX.md`, `SYSTEM_MAP.md`, etc.).
- **Conceptual Blueprint → Implementation Plan**: `docs/bele-dana.md` provides the structural design that informs the milestones in `.logitaka/ROADMAP_MATERIAL.md`.

## Boundaries

- **Planning vs. Execution**: Current project scope is focused on architectural planning and documentation. Execution artifacts (n8n workflows, code) are managed as separate tasks.
- **Structural Integrity**: The `.logitaka` directory is reserved for system-level context and should not be used for general documentation or source code.

## Constraints

- **Single Source of Truth**: The `docs/bele-dana.md` file is the master reference for the system's conceptual architecture.
- **Automated Updates**: Metadata files in `.logitaka` should be updated exclusively via the provided logic in the `builders/` directory to maintain consistency.
