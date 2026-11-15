# Software Testing Skill

Provide confidence that changes work, preserve existing behavior, and fail safely.

## Test levels
1. Static checks: formatting, lint, type-check, schema validation.
2. Unit tests: deterministic business rules and isolated logic.
3. Integration tests: database, queues, filesystem, and service boundaries.
4. Contract tests: API/event compatibility.
5. End-to-end tests: critical user journeys.
6. Load, resilience, and security tests for high-risk paths.

## Test quality
- Test observable behavior, not private implementation details.
- Include success, boundary, invalid-input, and failure cases.
- Use deterministic fixtures and isolated test data.
- Avoid order-dependent tests and uncontrolled external services.
- Mock external boundaries, not the business logic under test.
- Keep assertions specific and failure messages useful.

## Regression and safety
Reproduce bugs with a failing test before fixing where practical. Cover the original failure and adjacent behavior. Use disposable databases or isolated schemas; never use production secrets or real personal data. Ensure tests cannot accidentally target production.

## Reporting
Report exact commands and outcomes. Distinguish passed, failed, skipped, and not-run checks. Never claim coverage or confidence without evidence.
