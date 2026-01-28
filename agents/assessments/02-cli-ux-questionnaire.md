# CLI Command UX Questionnaire

Instructions: A senior engineer should answer each question **in bold** directly below it.

## 1) Command Surface & Naming
1. What is the primary CLI command name and why is it memorable/obvious?
**vibe**
2. What subcommands are required for MVP (list only the essentials)?
**vibe init**
**vibe preflight**
**vibe help**
3. Which subcommands must be aliases (if any) for discoverability or muscle memory?
4. What should the default command (no args) do?
**vibe help**
5. What should happen if the user runs an unknown subcommand?
**vibe help**

## 2) Installation & Invocation
6. What is the exact one-line install flow we want users to follow?
**once users install the app, they shall create a new coding project or cd into an existing project, then they shall run vibe init, which will create a series of files: AGENTS.MD, and required agents/. Agents will have the following subdirectories: assessments, memory, prompts, templates, specialists - with their respective files.**
7. Should the CLI support a `--version` or `version` command? What should it output?
**no**
8. Should the CLI support `--help` and per-subcommand help? What depth is required?
**sure, but should be simple (like the program)**
9. Should the CLI require being run from a repo root, or should it accept a `--path` flag?
**yes**
10. What is the expected behavior if the target path is not a git repo?
**should prompt to user: git repo required**

## 3) Inputs, Flags, and Prompts
11. Which commands must be fully non-interactive (scriptable) vs. interactive (prompts)?
**almost none**
12. For interactive flows, which prompts are required and which can be skipped with flags?
**maybe installing only certain agents**
13. What are the required flags for MVP (e.g., `--force`, `--dry-run`, `--yes`)?
**--dry-run**
14. What defaults should apply when flags are omitted?
**
15. How should the CLI handle invalid or missing input values?

## 4) Output & Messaging
16. What should the CLI print on success for each command (brief, verbose, or both)?
17. Should the CLI support a `--quiet` or `--json` output mode?
18. What is the expected format for file creation logs (single line vs. grouped summary)?
19. Should the CLI show a diff/preview before writing files? If yes, when?
20. What is the minimum level of progress feedback required for long operations?

## 5) Errors, Exit Codes, and Recovery
21. What are the standard exit codes for: success, user error, and system error?
22. What errors must be fatal vs. recoverable (e.g., missing directories, existing files)?
23. What should the CLI do when files already exist (skip, overwrite, prompt, fail)?
24. How should the CLI behave on partial failures (some files written, some not)?
25. What actionable error messages are required (include example text expectations)?

## 6) Determinism, Idempotence, and Safety
26. What does "deterministic" mean for this CLI in practice?
27. Which commands must be idempotent (re-running produces same result)?
28. Should there be a `--dry-run` mode for all write operations? If yes, what detail level?
29. What safety checks are required before writing to disk?
30. Are there any directories or files the CLI must never touch?

## 7) Discoverability & Documentation
31. What are the top 3 example commands that should appear in the README?
32. What is the minimum help text for each subcommand?
33. Should the CLI include a `doctor` or `status` command? If yes, what should it check?

## 8) Automation & CI Use
34. Which commands must be stable for CI usage (no prompts, deterministic output)?
35. What environment variables, if any, should configure behavior?
36. Should the CLI support config files? If yes, where and with what precedence?
37. What logging or artifacts should be produced for CI debugging (if any)?

## 9) Compatibility & Environment
38. Which shells and OSes must be supported for MVP?
39. What terminal capabilities can we assume (colors, unicode, width)?
40. Should output be ASCII-only for maximum portability?

## 10) Success Criteria
41. What user behavior signals that the CLI UX is "good enough" for MVP?
42. What would be the top UX complaint that would require immediate fixes?
43. What can we defer until after MVP without harming core workflows?
