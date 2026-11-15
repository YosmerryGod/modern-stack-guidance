# Database Engineering Skill

Protect data integrity while designing schemas, queries, migrations, and data-access layers.

## Inspect first
Identify database engine/version, schema ownership, ORM/query builder, migration tooling, data volume, backup process, and deployed application compatibility requirements.

## Schema and queries
- Choose accurate data types; define keys, foreign keys, unique/check constraints, and nullability deliberately.
- Normalize transactional data by default; denormalize only for a demonstrated access pattern.
- Store timestamps consistently (prefer UTC) and convert at the application boundary.
- Parameterize all values; never concatenate untrusted input into SQL.
- Select only required columns and use deterministic ordering for pagination.
- Add indexes based on query predicates, joins, ordering, and measured query plans.
- Avoid N+1 access and unbounded scans.

## Transactions and concurrency
Keep transactions short. Choose isolation and locking based on correctness requirements. Handle constraint and serialization conflicts. Use atomic updates for balances, counters, inventory, and other contested values; read-then-write application logic is not automatically race-safe.

## Migrations
- Prefer additive, backward-compatible changes.
- For risky changes use expand → backfill → switch → contract.
- Make backfills bounded, resumable, observable, and safe to rerun.
- Avoid long locks and destructive peak-traffic migrations.
- Define rollback or forward-recovery before production changes.
- Never run destructive production migrations without explicit approval and a verified backup.

## Privacy and recovery
Minimize personal data, define retention, restrict DB roles, encrypt backups, and periodically test restore procedures.

## Validation
Test migrations against representative schema/data, verify constraints and query plans, and confirm old/new app versions can coexist during rolling deployment.
