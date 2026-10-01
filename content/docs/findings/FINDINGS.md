# Findings Registry

This is the central registry for verified project findings.

Every material audit/review finding must receive a stable ID and be registered here.
Do not silently delete resolved findings; change their status and retain traceability.

## Statuses

- Open
- Approved
- In Progress
- Resolved
- Verified
- Deferred
- Blocked
- Accepted Risk
- Superseded

## Severity

- Critical
- High
- Medium
- Low

## Registry

| ID | Severity | Area | Summary | Status | Source/Audit | Remediation Phase | Verification |
|---|---|---|---|---|---|---|---|
| — | — | — | No findings recorded yet | — | — | — | — |

## Rules

1. IDs are permanent once assigned.
2. Never reuse an old finding ID for a different issue.
3. Resolution requires implementation evidence.
4. Verification requires test/review evidence where applicable.
5. Deferred and Accepted Risk findings require rationale.
6. Blocked findings must state the blocker.
7. Link findings to the prompt/phase that remediates them.
8. New unrelated findings discovered during implementation are recorded, not silently fixed.
