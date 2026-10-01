# User Documentation Rule

User-facing documentation is part of the product.

## Required Behavior

1. Document verified implemented behavior only.
2. Never describe planned/demo/mock functionality as production functionality.
3. Use terminology that matches the actual UI and domain.
4. State role, permission, configuration, jurisdiction, integration, or deployment conditions when behavior depends on them.
5. Do not make unsupported legal, security, privacy, financial, compliance, accreditation, or certification claims.
6. Keep instructions task-oriented and understandable by the intended audience.
7. Warn clearly before irreversible, destructive, financial, privacy-sensitive, or security-sensitive actions.
8. Do not expose secrets or internal security details that users do not need.
9. When implementation changes a documented workflow, update the affected documentation in the same phase.
10. When no user documentation changes are required, record that explicitly in the phase result.

## Documentation Impact Gate

Before completing a material change, answer:

`Does this change affect user-facing behavior, administration, onboarding, training, operations, support procedures, or developer setup?`

If yes, update the relevant documentation before completion.
