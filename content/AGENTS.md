# AI Agent Instructions

Before making changes:

1. Read `docs/ENGINEERING-STANDARD.md`.
2. Read `docs/project/PROJECT.md`.
3. Read `docs/project/REQUIREMENTS.md`.
4. Read `docs/project/DOMAIN.md`.
5. Read relevant architecture, security, compliance, and ADR documents.
6. Read the active execution prompt under `docs/prompts/`.
7. Respect the exact scope, allowed changes, forbidden changes, and stop point of the active prompt.

## Mandatory behavior

- Inspect before changing.
- Preserve existing behavior unless the active prompt explicitly authorizes a change.
- Never invent requirements or claim legal/regulatory compliance without evidence.
- Do not silently change business rules, database semantics, security boundaries, or external contracts.
- Do not fix unrelated findings unless required to safely complete approved work.
- Prefer small, verifiable phases over large rewrites.
- Do not automatically proceed to the next phase.

## Before completing an implementation phase

1. Run the required tests.
2. Run type-check where applicable.
3. Run lint where applicable.
4. Run the production build where applicable.
5. Verify migrations where applicable.
6. Review the complete diff.
7. Create/update the required result document.
8. Update the prompt registry.
9. Update relevant ADRs/documentation if the approved work changed them.
10. Report unresolved issues and STOP for human review.


## Agent Rules and Workflows

Before substantial work, read the relevant files under:

- `.agents/rules/`
- `.agents/workflows/`

Use `.agents/skills/` only when a project-specific specialized skill exists.

Do not treat `.agents/` as a replacement for requirements, architecture documentation,
ADRs, prompts, findings, or result documents.

## UI / UX Work

Before creating or materially changing user interfaces:

1. Read `docs/design/DESIGN-SYSTEM.md`.
2. Read `docs/design/UI-GUIDELINES.md`.
3. Read `docs/design/UX-GUIDELINES.md`.
4. Read `docs/design/ACCESSIBILITY.md`.
5. Read `docs/design/RESPONSIVE-DESIGN.md`.
6. Read `.agents/rules/ui-design.md`.
7. Follow `.agents/workflows/ui-feature.md` for substantial UI features.

Reuse existing design tokens and components before creating new ones.
Do not redesign unrelated areas during scoped feature work.

## Mandatory Traceability

For material audits, findings, remediation, and implementation phases:

1. Register verified findings in `docs/findings/FINDINGS.md`.
2. Store significant execution prompts under `docs/prompts/`.
3. Keep `docs/prompts/README.md` current.
4. Create the required phase result under `docs/results/`.
5. Keep `docs/results/README.md` current.
6. Create/update ADRs for important long-lived decisions.
7. Maintain `Requirement → Finding → Decision → Prompt → Implementation → Test → Result` traceability where applicable.
8. Never mark a finding resolved without implementation evidence.
9. Never mark verification complete without actual verification evidence.
10. Never fabricate historical prompts, test runs, audit evidence, or results.

Before declaring a material phase complete, review these registries and the complete code diff.

## User, Training, and Developer Documentation

For changes affecting user-facing behavior, administration, onboarding, training, operations, support, or developer setup:

- read `.agents/rules/user-documentation.md`
- use `.agents/workflows/user-documentation.md` when appropriate
- update relevant files under `docs/user-docs/` and/or `docs/developer/`
- document verified implemented behavior only
- record `Documentation impact: None` in the phase result when no documentation update is required

User documentation must not claim planned, demo-only, unverified, legally unconfirmed, or externally unapproved functionality is available.
