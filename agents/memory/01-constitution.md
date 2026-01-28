# Vibemaxxing Constitution

## Summary
Build a simple, installable CLI that scaffolds files, templates, and structures for agent-driven development, aimed at senior engineers working locally.

## Goals
- Primary: a runnable script/binary that creates the required agent-dev files in a codebase.
- Secondary: one-step installation via `curl + chmod + ./install.sh`.
- Support core workflows: vision, constrain, architect, roadmap, suggest, plan, revisit, execute.

## MVP Scope
- CLI-only, local runtime.
- Scaffolds into the project repo and a `.codex` directory.
- Day-one templates: questionnaire, constitution, roadmap, architecture, memory, rca.

## Non-Goals (MVP)
- Integrations with agents beyond Codex.
- Hosting, web UI, or backend services.

## Constraints & Guardrails
- Prefer simplicity and portability.
- Monolith CLI with clean internal structure (MVC-style).
- Assume bash is available.
- Tests must pass before shipping.

## Implementation Preferences
- Python or Rust, or a single bash script if sufficient.
- Agent-agnostic design, validated with Codex.

## Success Criteria
- Install path works (curl → chmod → run).
- Running the tool consistently creates files in the expected locations.
- Senior engineers can immediately start agent-driven workflows from the scaffolded output.
