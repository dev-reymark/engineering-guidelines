# Security Rules

- Authenticate and authorize sensitive operations server-side.
- Never use hidden/disabled UI as authorization.
- Never trust client-provided tenant ownership or authoritative financial totals.
- Enforce tenant/branch/resource ownership at trusted boundaries.
- Validate untrusted input at runtime.
- Protect secrets and avoid unnecessary sensitive logging.
- Treat refunds, voids, overrides, destructive operations, and privilege changes as sensitive.
- Add security regression tests where appropriate.
