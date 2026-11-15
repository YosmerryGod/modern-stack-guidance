# DevOps and Operations Skill

Deploy and operate services predictably, securely, and with recoverable change processes.

## Inspect first
Check OS, runtime, process manager, deployment workflow, network topology, resource limits, service dependencies, and rollback options. Do not assume Docker, Kubernetes, or a cloud platform exists.

## Configuration and secrets
Keep environment-specific config outside source. Store secrets in protected environment variables or a secret manager. Restrict permissions, separate environments, and never print secrets in CI logs.

## Deployment
- Make builds reproducible and pin critical runtime/tool versions where appropriate.
- Run tests and build checks before deployment.
- Prefer immutable artifacts and atomic release switching when supported.
- Use health/readiness checks before routing traffic.
- Stage database/API changes for backward compatibility.
- Verify deployed version and critical flows after release.
- Maintain a tested rollback or forward-fix procedure.

## Host and process operations
Configure graceful shutdown, restart behavior, and resource limits. Monitor disk, memory, CPU, network, restarts, and log growth. Rotate logs, patch OS/runtime packages, restrict inbound ports, and use least-privilege service accounts.

## CI/CD
Use least-privilege tokens and short-lived credentials. Protect production environments and branches. Separate build/test permissions from deployment permissions. Pin third-party actions to trusted versions or immutable references where practical. Never expose secrets to untrusted pull-request code.

## Incident readiness
Maintain health endpoints, actionable alerts, runbooks, deployment identifiers, backups, and tested restore procedures.
