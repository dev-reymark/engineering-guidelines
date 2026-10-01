# Software Project Engineering & AI-Agent Development Guidelines

Welcome to the **Software Project Engineering & AI-Agent Development Standard (v1.1)** documentation portal.

This standard provides a rigorous, traceable, and production-tested framework for building mission-critical software systems alongside autonomous AI coding agents.

> [!IMPORTANT]
> The primary objective is **controlled, traceable engineering** rather than uncontrolled code generation. High-velocity AI development must be paired with clear architectural guardrails, auditable decision records, and deterministic verification.

---

## Quick Navigation

Choose a starting track below to explore the guidelines:

| Track | Description | Key Documents |
| :--- | :--- | :--- |
| **Start Here** | Core standard and AI agent instructions | [Engineering Standard](docs/ENGINEERING-STANDARD.md) · [AI Agent Rules](AGENTS.md) · [Traceability](docs/TRACEABILITY.md) |
| **Architecture & Design** | System design, data models, and security | [Architecture](docs/architecture/ARCHITECTURE.md) · [Data Model](docs/architecture/DATA-MODEL.md) · [Security Model](docs/architecture/SECURITY.md) |
| **Agent Rules & Workflows** | Curated guidelines for AI coding agents | [Coding Rules](.agents/rules/coding.md) · [Security Rules](.agents/rules/security.md) · [Workflows](.agents/workflows/implement-phase.md) |
| **Compliance & Governance** | Regulatory controls, ADRs, and audits | [Compliance Matrix](docs/compliance/COMPLIANCE-MATRIX.md) · [ADRs](docs/decisions/README.md) · [Findings](docs/findings/FINDINGS.md) |
| **Testing & Operations** | Test matrices, deployment, and runbooks | [Test Strategy](docs/testing/TEST-STRATEGY.md) · [Deployment](docs/operations/DEPLOYMENT.md) · [Runbook](docs/operations/RUNBOOK.md) |
| **Design & User Docs** | UI/UX systems and end-user documentation | [Design System](docs/design/DESIGN-SYSTEM.md) · [User Guide](docs/user-docs/USER-GUIDE.md) · [Admin Guide](docs/user-docs/ADMIN-GUIDE.md) |

---

## The Traceability Standard

Every non-trivial engineering initiative or automated AI agent task follows the strict **Traceability Chain**:

```text
Requirement -> Research -> Finding -> Decision (ADR) -> Prompt -> Implementation -> Test -> Result
```

1. **Requirement**: What the system must achieve ([`docs/project/REQUIREMENTS.md`](docs/project/REQUIREMENTS.md)).
2. **Research**: Authoritative investigation of laws, APIs, frameworks, and constraints.
3. **Finding**: Documented discoveries, audit points, or vulnerabilities ([`docs/findings/FINDINGS.md`](docs/findings/FINDINGS.md)).
4. **Decision**: Explicit Architecture Decision Records ([`docs/decisions/ADR-TEMPLATE.md`](docs/decisions/ADR-TEMPLATE.md)).
5. **Prompt**: Verifiable prompt specification delivered to the AI agent ([`docs/prompts/README.md`](docs/prompts/README.md)).
6. **Implementation**: Minimal, focused code changes that adhere to project rules.
7. **Test**: Targeted automated regression, unit, and integration checks ([`docs/testing/TEST-STRATEGY.md`](docs/testing/TEST-STRATEGY.md)).
8. **Result**: Signed-off phase verification record ([`docs/results/README.md`](docs/results/README.md)).

---

## Core Engineering Priorities

The standard defines 10 unwavering priorities in order of precedence:

1. **Correctness** — Does the system do exactly what is specified under all inputs?
2. **Security** — Are authentication, authorization, and isolation enforced server-side?
3. **Data Integrity** — Are schemas, foreign keys, and audit logs maintained without data loss?
4. **Transaction Integrity** — Are multi-step state changes atomic with safe rollback semantics?
5. **Business-Rule Correctness** — Are statutory, financial, and domain invariants strictly observed?
6. **Regulatory / Compliance** — Are relevant statutes (e.g. data privacy, taxation) respected?
7. **Maintainability** — Can developers read, reason about, and adapt the code easily?
8. **Testability** — Can all critical paths be checked automatically in isolation?
9. **Observability** — Are error states, metrics, and structured logs readily accessible?
10. **Simplicity** — Is the implementation the simplest solution that satisfies all criteria?

> [!TIP]
> Never optimize for abstraction count, architectural novelty, or total lines of generated code. Prefer clear code over speculative layers.

---

## Repository Scaffold Structure

The documentation site provides direct access to every file in the standard:

```text
content/
├── AGENTS.md                   # Universal root rules for coding agents
├── docs/
│   ├── ENGINEERING-STANDARD.md # Complete standard specification
│   ├── TRACEABILITY.md         # Traceability matrix and rules
│   ├── project/                # Domain, Requirements, Project, Roadmap
│   ├── architecture/           # System Architecture, Data Model, Security, Audits
│   ├── compliance/             # Statutory matrix, sources, and roadmap
│   ├── decisions/              # Architecture Decision Records (ADRs)
│   ├── design/                 # Design System, Accessibility, Responsive, UI/UX
│   ├── developer/              # Getting Started, Contributing, Local Dev
│   ├── findings/               # Findings Registry and templates
│   ├── operations/             # Deployment, Environment, Runbooks, Backup
│   ├── prompts/                # Prompt registry, discovery, and execution templates
│   ├── results/                # Phase verification and sign-off records
│   ├── testing/                # Test matrix and verification strategy
│   └── user-docs/              # User, Admin, Onboarding, Training, and Troubleshooting
└── .agents/
    ├── rules/                  # Specific modular rules (coding, db, security, etc.)
    └── workflows/              # Step-by-step agent workflows (audit, phase, new-project)
```

---

## How to Use This in Your Own Projects

To adopt these guidelines in your software project:

1. Copy the contents of `content/` into your project repository.
2. Configure [`AGENTS.md`](AGENTS.md) with your project-specific technology stack and rules.
3. Keep `.agents/` and `docs/` committed to version control so AI agents have persistent context.
4. Browse or reference this documentation site whenever establishing new architectural patterns.

---

*Standard Version: 1.1 · Scaffold Version: v4.1 · Maintained by [Dev Reymark](https://github.com/dev-reymark)*
