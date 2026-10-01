# Prompt 000 — Project Discovery

Status: Draft
Created: YYYY-MM-DD
Executed:

Type: Audit / Project Definition
Implementation Allowed: No
Production Code Changes Allowed: No

Depends On:
- `docs/ENGINEERING-STANDARD.md`
- `AGENTS.md`

Expected Outputs:
- `docs/project/PROJECT.md`
- `docs/project/REQUIREMENTS.md`
- `docs/project/DOMAIN.md`
- initial update to `docs/project/ROADMAP.md`

Purpose:
Understand and document the project before architecture or implementation begins.

---

# Exact Execution Prompt

Read `AGENTS.md` and `docs/ENGINEERING-STANDARD.md` first.

This is Stage 0 — Project Discovery only.

Do not implement application code, modify database schema, add migrations, add dependencies, or begin architecture implementation.

Work with the human-provided project idea and repository evidence. If the repository already contains code, inspect it only as needed to distinguish existing behavior from intended behavior.

Create or update:

1. `docs/project/PROJECT.md`
2. `docs/project/REQUIREMENTS.md`
3. `docs/project/DOMAIN.md`
4. `docs/project/ROADMAP.md`

Document:
- objective and problem
- target users
- core workflows
- business model
- platforms/deployment assumptions
- integrations
- MVP and future scope
- explicit non-goals
- functional/security/data/operational/compliance requirements
- domain terminology, entities, workflows, state transitions, calculations, invariants, roles and permissions
- high-risk areas
- unresolved questions and assumptions

Do not invent business or regulatory requirements. Mark unknowns clearly.

At completion, summarize what was established, list unresolved questions, recommend the next design/audit prompt, and STOP for human approval.
