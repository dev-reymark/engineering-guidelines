# Database Rules

Before database changes evaluate constraints, indexes, foreign keys, uniqueness, nullability,
ownership, tenant boundaries, concurrency, historical data, migration compatibility, and rollback.

Enforce critical invariants in the database where appropriate.
Do not silently change schema or persistence semantics.
Define explicit transaction boundaries for critical multi-record operations.
