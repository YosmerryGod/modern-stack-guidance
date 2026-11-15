# Backend Engineering Skill

Design and maintain reliable server-side applications, APIs, background jobs, and integrations.

## Inspect first
Identify runtime/framework versions, entry points, middleware, API contracts, deployment model, dependencies, and error conventions. Map trust boundaries and privileged operations.

## API design
- Validate path, query, headers, and body at the boundary with explicit schemas.
- Use consistent HTTP methods, status codes, and response formats.
- Return actionable errors without leaking stack traces, secrets, SQL, or internal topology.
- Paginate and bound potentially large collections.
- Make retried create/payment/message operations idempotent or deduplicated.
- Preserve compatibility; version breaking public API changes.

## Node.js
- Use supported runtime versions and the project's module system.
- Prefer asynchronous non-blocking I/O.
- Bound concurrency, payload sizes, execution time, and resource use.
- Handle promise failures and graceful shutdown deliberately.
- Close database, queue, socket, and HTTP resources on shutdown.
- Avoid unbounded in-memory queues, caches, and listeners.
- Move CPU-heavy work off the event loop when justified.

## Reliability and data consistency
- Set timeouts on outbound calls.
- Retry only transient failures with bounded backoff and jitter; do not blindly retry non-idempotent actions.
- Make jobs safe against duplicate delivery and observable.
- Use transactions for related writes that must succeed or fail together.
- Handle race conditions with constraints, locks, optimistic concurrency, or atomic updates.
- Keep external side effects outside DB transactions where possible; consider an outbox or compensating workflow.

## Observability
Use structured logs and correlation IDs. Track latency, error rate, throughput, saturation, and dependency health. Redact credentials, tokens, session cookies, private message contents, and sensitive personal data.

## Validation
Test success and failure paths, invalid input, authorization, timeouts, dependency failures, and API compatibility. Run type-check, lint, and production build when applicable.
