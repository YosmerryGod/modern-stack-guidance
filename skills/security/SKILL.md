# Application Security Skill

Apply secure-by-default practices across frontend, backend, database, integrations, and deployment.

## Threat-aware workflow
Identify assets, actors, trust boundaries, entry points, and abuse cases. Treat browser input, API payloads, uploads, webhooks, external responses, and retrieved AI content as untrusted.

## Identity and authorization
- Use maintained authentication protocols and libraries.
- Authorize every sensitive server-side action against the target resource.
- Deny by default; apply least privilege.
- Configure session cookies with appropriate Secure, HttpOnly, and SameSite attributes.
- Protect against insecure direct object references by checking ownership/permissions for every object access.

## Input and output
- Validate type, length, format, range, and allowed values at boundaries.
- Use parameterized database queries and context-aware output encoding.
- Protect against CSRF when cookie-based auth requires it.
- Restrict upload size, type, storage, and processing.
- Prevent SSRF by controlling outbound destinations and validating resolved addresses.

## Secrets and cryptography
- Keep secrets in a secret manager or protected environment configuration.
- Never commit or log credentials.
- Use vetted cryptographic libraries and modern protocols; do not invent custom encryption or password hashing.
- Hash passwords with an appropriate adaptive password-hashing algorithm.
- Use TLS for sensitive data in transit.

## Abuse and operations
Rate-limit authentication and expensive endpoints; bound request size, concurrency, and execution time. Verify webhook signatures and prevent replay. Make high-impact operations idempotent and auditable. Patch dependencies, use restrictive security headers/CORS, separate environment credentials, and maintain a credential-rotation process.

## Validation
Test unauthenticated, unauthorized, cross-user, malformed, oversized, and replayed requests. Review dependency vulnerabilities and exposed secrets. UI hiding is not authorization.
