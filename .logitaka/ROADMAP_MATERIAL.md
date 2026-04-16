# ROADMAP MATERIAL

## PURPOSE

Raw extracted signals about development direction. Not a final roadmap.

## ACTIVE AREAS

- **Logitaka Bootstrap**: Initial setup of the repository context and metadata layer.
- **Architectural Specification**: Finalizing the conceptual framework and decomposition methodology in `docs/`.

## INCOMPLETE WORK

- **Stage 1 (Infrastructure)**: Missing Docker/n8n deployment, SSL configuration, and server resource preparation.
- **Stage 2 (Core Logic)**: Master-workflow and sub-workflow implementation in n8n is not yet started.
- **Agent Definitions**: Translating visual/conceptual agents (Director, Scraper, SDR) into actual prompter/logic blocks.

## IMPLIED NEXT STEPS

- **Environment Provisioning**: Setting up the n8n instance and Docker environment as per `docs/bele-dana.md`.
- **Orchestration Layer**: Building the initial n8n master workflow to manage context and agent instructions.
- **Communication Flow**: Defining the data exchange format between the "Scraper" and "Filter" agents.

## INFRA / SYSTEM DIRECTIONS

- **Workflow-as-Code**: Transitioning from Markdown-only specification to functional n8n workflows.
- **Containerization**: Target deployment remains a Docker-based instance with a reverse-proxy setup.
