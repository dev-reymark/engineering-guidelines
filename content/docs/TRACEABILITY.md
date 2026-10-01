# Project Traceability

The project should maintain this chain for material work:

Requirement → Finding → Decision → Prompt → Implementation → Test → Result

Not every small change requires every artifact. Use judgment, but never lose traceability for:
- critical/high findings
- security changes
- financial/business-rule changes
- database/schema changes
- compliance changes
- architecture decisions
- production-risk changes

## Sources of Truth

- `docs/project/PROJECT.md` — what is being built
- `docs/project/REQUIREMENTS.md` — what it must do
- `docs/project/DOMAIN.md` — domain rules and invariants
- `docs/architecture/` — system design and audits
- `docs/design/` — UI/UX system
- `docs/compliance/` — external/regulatory requirements
- `docs/decisions/` — why durable decisions were made
- `docs/findings/FINDINGS.md` — status of verified issues
- `docs/prompts/` — what agents were instructed to do
- `docs/results/` — what actually happened
- source code, schema, migrations, and tests — what is actually implemented

When documentation conflicts with implementation, investigate and reconcile; do not silently assume either is correct.
