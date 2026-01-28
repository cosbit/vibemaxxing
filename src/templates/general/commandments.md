# Commandments Template
## How to use this file
The next section will be the template when generating `02-commandments.md`. You will copy sections verbatim except for the areas where you need to fill in the blank, which will be wrapped in underscores _. For example: Purpose: _explain purpose_

---

# _Title of project_ Commandments

## Purpose
- _State the purpose of these commandments and the desired agent outcomes._

## Core Principles
1. _Primary guiding principle._
2. _Secondary guiding principle._
3. _Additional guiding principle._
4. _Additional guiding principle._
5. _Additional guiding principle._
6. Do not assume; follow user requirements exactly.

## Operational Rules
- Always load the context of `02-commandments.md` at the start of every execution.
- _Define required behaviors that must always hold._
- _Define explicit constraints or forbidden actions._
- _Define error-handling expectations._
- _Define execution and delivery expectations._
- If requirements are unclear or missing, ask the user for clarification before proceeding.
- Log memory of application components in `agents/memory/03-architecture.md`.
- When troubleshooting, create an RCA report in `agents/memory/04-rcas.md`.
- When running shell commands for troubleshooting or verification, follow the user's execution preferences (e.g., Makefile-only, Docker-only, `.venv`-only).

## MVP Guardrails
- _List explicit scope limits or exclusions._
- _List platform or environment constraints._
- _List required day-one templates or artifacts._

## Quality Bar
- _Define testing/validation requirements._
- _Define behavioral standards for agent output._


## Decision Heuristics
- _Provide rules for choosing between alternatives._
- _Provide rules for deferring or skipping changes._

## Output Discipline
- _Define formatting, naming, or file-structure constraints._
- _Define expectations for clarity and minimal boilerplate._

## Security Guidelines
- Minimize sensitive data exposure; avoid logging secrets or credentials.
- Do not execute untrusted code or commands without explicit user approval.
- Follow least-privilege practices for file access and command execution.
