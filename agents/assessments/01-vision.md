# MVP Goals & Requirements Questionnaire

Instructions: A senior engineer should answer each question **in bold** directly below it.

## 1) Need, Purpose, Scope
1. What problem are we solving, and for whom?
**We are optimizing the workflow of agent-driven development. The users will be engineers**
2. Why is this problem worth solving now?
**I specifically need this, I am an engineer increasingly doing agent-driven development.**
3. What is the smallest scope that still delivers clear value (MVP boundary)?
**Runnable binary/program/script to scaffold files, templates and structures for agent-driven design.**
4. What is explicitly out of scope for the MVP?
**MVP will target only codex+bash but no other agents.**
5. What are the top 3 user outcomes that define success for the MVP?
**- User should be able to install program via a curl+chmod+./install.sh**
**- Installed program will allow user to scaffold files for agentic development with workflows, templates, memory helpers, etc...**
6. What assumptions are we making that must be validated early?
**Users should have bash installed**

## 2) MVP Goals
7. What is the single primary goal of the MVP?
**A script that creates files in a codebase - which will prepare that codebase for agent driven development**
8. What are the secondary goals (if any), ranked by priority?
**Installation script**
9. What would make this MVP a failure even if it ships?
**If we run the program/script and it fails to create new files in a certain location that will help coding agents, such as codex use workflows.**
10. What is the target audience profile for the MVP (roles, experience, environment)?
**Senior engineers**

## 3) Product Requirements
11. List the core user workflows the MVP must support.
**- vision: defines the goals and requirements of the application's MVP**
**- constrain: writes agent rules and constrains while developing, testing, or interacting with the application**
**- architect: creates the high-level architecture of the components/microservices of the application**
**- roadmap: defines a high-level milestone plan for delivering the MVP**
**- suggest: create a questionnare to the user in order to make suggestions to the implementation of a milestone's task**
**- plan: defines a series of prompts / tasks for the specified milestone.**
**- revisit: make revisions to agent files: constitution, commandments, plan, prompts.**
**- execute: perform the task described in the prompt-file requested.**
12. What are the minimum data inputs/outputs required for each workflow?
**filling in questionnares and outputting into templates**  

13. What integrations (if any) are required for the MVP?
**I will only be testing with codex - but this project should be agent agnostic** 
14. What UX requirements are non‑negotiable for the MVP?
**CLI tool**

15. What content or templates must exist on day one?
**Templates:**
**1. questionnare.md**
**2. constitution.md**
**3. roadmap.md**
**4. architecture.md**
**5. memory.md**
**4. rca.md**

## 4) Technical Approach
16. What is the preferred tech stack (language, framework, runtime) and why?
**Python or Rust - but maybe this project could be a single bash functions that you curl+chmod+./init.sh. i am the most comfortable with these. All I am doing is creating a series of files in specific locations**

17. What constraints do we have around tooling, hosting, or deployment?
**Will not be hosting, users should compile / install themselves**

18. What architectural pattern should the MVP follow (e.g., monolith, modular, CLI, web app)?
**monolith CLI, but a well structured MVC**

19. What quality attributes matter most for the MVP (e.g., reliability, speed, simplicity, portability)?
**Simplicity and portability**

20. What existing code, scripts, or assets can be reused?


## 5) Runtime & Infrastructure
21. What is the expected runtime environment (local, CI, container, cloud)?
**Local**

22. What are the MVP’s infrastructure requirements (storage, secrets, CI/CD, logging)?
**None**

23. What dev workflow is preferred (branching strategy, linting, testing)?
**Maybe docker / pytest**

24. What minimum test coverage or validation is required before shipping?
**All tests pass**
## 6) Milestones & Delivery
25. What are the top 3 milestones for delivering the MVP?
**Installable/init script, script creates a series of files in current codebase directory, script creates a series of files in .codex directory** 
26. What should be included in the first milestone (boilerplate/runtime/infrastructure)?
**Most commands/workflows**
27. What is the target timeline for the MVP (dates or ranges)?
**None**
28. What risks or dependencies could derail the plan?
**Testing infrastructure, testing the actual LLM**
## 7) Success Criteria
29. What metrics or qualitative signals define MVP success?
**who knows**
30. What would trigger a follow‑on phase (post‑MVP)?
**who nows**
31. Who are the stakeholders and what are their acceptance criteria?
**Myself**
## 8) Constraints & Guardrails
32. What must not change about the current repo or workflow?
**Nothing**
33. Are there any security, privacy, or compliance requirements for the MVP?
**We will see**
34. What is the budget/time cap for the MVP?
**None**
35. What trade‑offs are acceptable to ship the MVP faster?
**None**