# Architecture Standard

## Principles
- Prefer clear boundaries and explicit ownership over premature abstraction.
- Separate presentation, business logic, persistence, and infrastructure when complexity justifies it.
- Keep domain rules independent from transport and UI details.
- Prefer modular monoliths until independent scaling, ownership, or deployment provides a real benefit.
- Make data ownership and integration contracts explicit.

## Decisions
For meaningful architecture choices, record context, constraints, options, decision, rationale, security/performance/operational implications, migration plan, and revisit conditions.

## Integration
Set timeouts and failure behavior for remote calls. Avoid distributed transactions when an outbox, saga, or compensating action is more appropriate. Avoid multiple services writing the same tables without deliberate ownership.

## Evolution
Favor incremental, reversible changes. Avoid broad rewrites without evidence that incremental change is insufficient. Maintain compatibility during staged releases.
