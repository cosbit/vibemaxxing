# Vibemaxxing Commandments

## Purpose
- Maximize agent-driven development throughput for senior engineers by producing a reliable, simple, portable CLI scaffold.

## Core Principles
1. Ship a working CLI scaffold before adding features or integrations.
2. Favor simplicity and portability over cleverness or unnecessary abstraction.
3. Optimize for local, agent-agnostic workflows that are validated with Codex first.
4. Keep the MVP scope tight; avoid scope creep.
5. Ensure the tool is deterministic: same inputs produce the same files.
6. Do not assume; follow user requirements exactly.

## Operational Rules
- Always load the content of `01-constitution.md`, `02-commandments.md` and `03-architecture.md` at the start of new contexts.
- Always create required files in the correct locations (repo + `.codex`).
- Never modify user files unless explicitly requested.
- Fail loudly with actionable errors; do not silently skip work.
- Keep all workflows CLI-first and scriptable.
- Ensure installation is one-step: `curl` → `chmod` → `./install.sh`.
- If requirements are unclear or missing, ask the user for clarification before proceeding.
- Log memory of application components in `agents/memory/03-architecture.md`.
- Log the high-level roadmap of milestones to completion in `agents/memory/04-roadmap.md`
- When troubleshooting, create an RCA report in `agents/memory/05-rcas.md`.
- When asked to create questionnares or assessments, save them sequentially in `agents/assessments/`
- When running shell commands for troubleshooting or verification, follow the user's execution preferences (e.g., Makefile-only, Docker-only, `.venv`-only).

## MVP Guardrails
- Only support Codex + bash for MVP testing.
- No web UI, hosting, or external services.
- Templates required on day one: questionnaire, constitution, roadmap, architecture, memory, rca.

## Quality Bar
- Tests must pass before shipping.
- Favor clear, predictable behavior over feature breadth.
- Document every workflow the CLI supports.

## Workflow Directives
- vision: define MVP goals, requirements, and scope.
- constrain: write agent rules and constraints.
- architect: produce high-level architecture for the MVP.
- roadmap: provide milestones for delivery.
- suggest: ask clarifying questions that improve a milestone plan.
- plan: define task prompts for a milestone.
- revisit: revise constitution, commandments, plan, prompts.
- execute: carry out tasks described in prompt files.

## Decision Heuristics
- If unsure, choose the simplest implementation that satisfies the constraints.
- If a change risks breaking scaffolding, add a test or skip it for MVP.
- If a feature does not improve agent workflows, defer it.

## Output Discipline
- Always write templates with clear headings and minimal boilerplate.
- Use stable filenames and folder structure.
- Prefer small, readable scripts over large frameworks.

## Security Guidelines
- Minimize sensitive data exposure; avoid logging secrets or credentials.
- Do not execute untrusted code or commands without explicit user approval.
- Follow least-privilege practices for file access and command execution.
