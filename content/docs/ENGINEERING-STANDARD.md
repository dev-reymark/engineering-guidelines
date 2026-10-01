# Software Project Engineering & AI-Agent Development Standard

Version: 1.0

## Purpose

Use this standard for serious software projects developed with AI coding agents. The goal is controlled, traceable engineering rather than uncontrolled code generation.

Trace important work as:

`Requirement → Research → Finding → Decision → Prompt → Implementation → Test → Result`

## Core priorities

1. Correctness
2. Security
3. Data integrity
4. Transaction integrity
5. Business-rule correctness
6. Regulatory/compliance correctness where applicable
7. Maintainability
8. Testability
9. Observability
10. Simplicity

Do not optimize for abstraction count, architectural novelty, or amount of generated code.

## Source-of-truth responsibilities

- `project/PROJECT.md` — what and why.
- `project/REQUIREMENTS.md` — what the system must do.
- `project/DOMAIN.md` — terminology, workflows, invariants, business rules.
- `architecture/ARCHITECTURE.md` — how the system is structured.
- `architecture/DATA-MODEL.md` — data ownership, relationships, constraints.
- `architecture/SECURITY.md` — authentication, authorization, isolation, security controls.
- `compliance/*` — externally imposed regulatory requirements and authoritative sources.
- `decisions/ADR-*` — why important long-lived decisions were made.
- `prompts/*` — exact instructions given to coding agents.
- `results/*` — what changed and what verification passed.
- source code/tests/schema — what is actually implemented.

## New-project lifecycle

### Stage 0 — Project definition
Define objective, users, workflows, business model, deployment model, constraints, security environment, regulatory environment, MVP scope, future scope, and non-goals. Produce `PROJECT.md`, `REQUIREMENTS.md`, and `DOMAIN.md` before major implementation.

### Stage 1 — Research
Research external facts that affect correctness: laws/regulations, APIs, providers, framework capabilities, statutory calculations, and operational constraints. Prefer authoritative/current sources.

### Stage 2 — Architecture design
Establish framework, database, authentication, authorization, feature boundaries, client/server boundaries, validation, transaction strategy, errors, logging, tests, and deployment architecture. Avoid unnecessary enterprise patterns.

### Stage 3 — Risk analysis
Identify high-risk workflows: money, payments, auth, authorization, tenant isolation, statutory calculations, inventory, destructive operations, concurrent writes, migrations, and external integrations.

### Stage 4 — Roadmap
Break work into independently verifiable phases. Do not ask an agent to build the whole application in one uncontrolled run.

### Stage 5+ — Implement, verify, document, review
For each phase: establish baseline, implement approved scope, test, review diff, document result, stop for human approval.

## Prompt standard

Every significant AI-agent task gets a sequential prompt ID (`000`, `001`, ...). Store the exact execution prompt under `docs/prompts/` and register it in `docs/prompts/README.md`.

Allowed prompt statuses: `Draft`, `Approved`, `In Progress`, `Completed`, `Blocked`, `Superseded`.

A prompt is completed only after its acceptance criteria and verification requirements pass.

## Phase standard

Every implementation phase should define:

- Objective
- Requirements/findings addressed
- Allowed changes
- Forbidden/out-of-scope changes
- Expected files
- Database/migration changes
- Business/UI/security/compliance impact
- Unit/integration/compliance tests
- Manual verification
- Rollback strategy
- Acceptance criteria
- Explicitly deferred items
- Required result document
- Stop point

## Baseline and verification

Before major changes, run the applicable existing test suite, type-check, lint, and production build. Record pre-existing failures. Do not silently fix unrelated failures.

Before completion, rerun required verification and inspect the complete diff. Ensure only intended files changed and dependencies/migrations are intentional.

## Test safety net

Critical existing behavior should have regression coverage before major refactoring. Prioritize money, tax, discounts, payments, payroll, permissions, tenant isolation, inventory, state transitions, refunds, and financial reports.

## Database and transactions

Explicitly consider constraints, indexes, foreign keys, uniqueness, nullability, ownership, concurrency, historical records, rollback, and migration compatibility. Use database constraints for critical invariants where appropriate.

Identify operations that must commit or fail atomically. Partial financial operations are high risk.

## Money

For money-handling systems, define an authoritative representation, currency, rounding, tax, and discount ordering. Avoid uncontrolled floating-point arithmetic. Client totals should not be authoritative unless the architecture explicitly and safely requires it.

## Authentication and authorization

Authentication answers who the actor is; authorization answers what the actor may do. Hidden UI, disabled controls, client roles, and client-provided tenant IDs are not authoritative controls. Sensitive operations require server-side authorization.

## Multi-tenancy

Define ownership for tenant-controlled resources and test cross-tenant isolation. The expected relationship is `User → Authorized Tenant → Resource`.

## Validation

Treat external input as untrusted: `Untrusted Input → Validation → Authorized Context → Typed Input → Business Logic → Persistence`. Static types do not replace runtime validation.

## Auditability

Security-sensitive and financially important systems should record appropriate audit events: actor, action, time, tenant/context, and relevant before/after state. Avoid mutable/deletable fiscal or security history where requirements demand immutability.

## Error handling and observability

Use consistent error boundaries. Do not expose raw database errors, swallow failures, leak secrets, or return arbitrary error shapes. Define logging/monitoring for application errors, security events, failed jobs/integrations, transaction failures, and critical performance issues.

## Findings

Use stable namespaces such as `ARCH-001`, `SEC-001`, `DATA-001`, `PERF-001`, `COMP-001`, or a domain-specific namespace. Do not renumber published findings. Use realistic severity: Critical, High, Medium, Low.

## Scope control

If unrelated issues are discovered, document them instead of automatically fixing them unless they block safe completion of the approved scope.

## Decisions

Use ADRs only for important long-lived decisions. ADRs explain context, decision, alternatives, consequences, compliance/security basis where relevant, and conditions for reconsideration.

## Compliance

Regulated projects should maintain a compliance matrix, roadmap, and source register. Current authoritative sources establish legal/regulatory requirements. Software capability must be distinguished from registration, accreditation, merchant configuration, operational compliance, and professional confirmation.

## Production readiness

Before launch, perform a dedicated review of correctness, security, database integrity, reliability, observability, performance, compliance, operations, backup/recovery, configuration, and documentation. A passing build is not equivalent to production readiness.

Potential blockers may be classified as `SOFTWARE BLOCKER`, `SECURITY BLOCKER`, `DATA-INTEGRITY BLOCKER`, `FINANCIAL-INTEGRITY BLOCKER`, `COMPLIANCE BLOCKER`, `EXTERNAL-REGISTRATION BLOCKER`, `CONFIGURATION BLOCKER`, or `PROFESSIONAL CONFIRMATION REQUIRED`.

## Final agent behavior

Agents must inspect before changing, use repository evidence, avoid invented requirements, avoid unnecessary dependencies/overengineering, verify their work, inspect the diff, document outcomes, and stop at phase boundaries.

AI accelerates engineering; it does not replace engineering discipline.
