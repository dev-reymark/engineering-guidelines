# .agents

Operational instructions for AI coding agents.

- `rules/` — standing engineering rules.
- `workflows/` — repeatable engineering procedures.
- `skills/` — optional project-specific specialized instructions.

Do not duplicate requirements, ADRs, findings, prompts, or results here.

Instruction hierarchy:
1. `AGENTS.md`
2. `docs/ENGINEERING-STANDARD.md`
3. `.agents/rules/*`
4. Active `docs/prompts/XXX-*.md`
5. Relevant requirements, architecture, compliance docs, and ADRs

The active prompt controls task scope. Core security, data-integrity, and verification rules
must not be casually bypassed.
