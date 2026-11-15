# Modern Stack Guidance

A practical, AI-agent-oriented engineering handbook for modern full-stack applications.

## Scope
This repository defines reusable skills for frontend, backend, databases, security, testing, and DevOps. It complements project-specific instructions and does not replace them.

## Layout
- `AGENTS.md`: rules for AI agents adopting this repository.
- `skills/frontend/SKILL.md`: browser, UI, React, Next.js, CSS.
- `skills/backend/SKILL.md`: Node.js, APIs, services, integrations.
- `skills/database/SKILL.md`: schema, SQL, migrations, indexing.
- `skills/security/SKILL.md`: application security and threat-aware design.
- `skills/testing/SKILL.md`: unit, integration, contract, and E2E testing.
- `skills/devops/SKILL.md`: deployment, CI/CD, Linux operations.
- `standards/`: cross-cutting architecture, code quality, and performance standards.

## How agents should use it
1. Read `AGENTS.md`.
2. Identify the layers affected by the task.
3. Read the matching skill files and relevant cross-cutting standards.
4. Inspect the actual project versions, conventions, and runtime before changing code.
5. Make the smallest safe change that satisfies the request.
6. Report exactly which validation commands were run and their outcomes.

## Upstream references
For modern browser and web-platform guidance, consult [GoogleChrome/modern-web-guidance](https://github.com/GoogleChrome/modern-web-guidance). Its focus is modern web platform practices; this repository adds broader backend, data, security, testing, and operations guidance.

## Principles
Correctness and data integrity first; security and privacy by default; compatibility before novelty; measurable performance; incremental, reviewable changes.

Initial baseline. Contributions should add actionable instructions, examples, version notes, and validation criteria rather than generic advice.
