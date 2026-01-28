# Vibemaxxing Architecture

## Summary
A monolith Bash CLI that scaffolds agent-driven development files into a target repo and a `.codex` directory. The system is intentionally simple, portable, and deterministic, optimized for senior engineers running locally.

## Architectural Goals
- Deterministic scaffolding: same inputs → same output files.
- Minimal dependencies; portable local execution.
- Clear separation of concerns (MVC-style): input parsing, workflow logic, and filesystem writes.
- Agent-agnostic templates validated with Codex.

## Core Components
1. **CLI Entrypoint**
   - A Bash script that parses args, loads user preferences, and routes to workflows.
2. **Workflow Router**
   - Maps commands to workflow handlers: vision, constrain, architect, roadmap, suggest, plan, revisit, execute.
3. **Template Library**
   - Stores canonical templates and any default content (plain text files).
4. **Renderer**
   - Bash-based token substitution to fill templates with user answers and context.
5. **Filesystem Writer**
   - Bash utilities create directories, write files, and enforce stable filenames/paths.
6. **Validation & Error Handling**
   - Bash checks ensure required inputs are present and outputs are created; fail loudly on errors.

## Data & Files
- **Inputs:** user answers to questionnaires, CLI flags, and existing project context.
- **Outputs:** scaffolded markdown files in repo + `.codex`.
- **Persistent Memory:**
  - `agents/memory/01-constitution.md`
  - `agents/memory/02-commandments.md`
  - `agents/memory/03-architecture.md`
  - `agents/memory/04-rcas.md` (when troubleshooting)

## File/Folder Targets
- Project repo: `agents/`, `src/templates/`, and related workflow assets.
- `.codex` directory: agent-specific runtime or memory helpers (as required by the CLI).

## Workflow Mapping
- **vision:** capture MVP goals, scope, and requirements.
- **constrain:** define rules and constraints for agent behavior.
- **architect:** generate or update this architecture summary.
- **roadmap:** create milestones and delivery plan.
- **suggest:** gather missing information to improve a milestone plan.
- **plan:** convert milestones into prompt/task files.
- **revisit:** revise constitution, commandments, plan, prompts.
- **execute:** carry out a task using the scaffolded context.

## Execution Preferences
- When running commands for troubleshooting/verification, follow user preferences (Makefile-only, Docker-only, `.venv`-only, etc.).

## Non-Goals
- No web UI or hosted service.
- No integrations beyond Codex for MVP.
- No hidden background processes.

## Quality & Testing
- Tests must pass before shipping.
- Favor small, readable scripts over frameworks.
