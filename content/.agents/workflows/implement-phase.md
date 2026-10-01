# Workflow — Implement Phase

1. Read active prompt and dependencies.
2. Confirm baseline.
3. Confirm allowed/forbidden scope.
4. Implement the smallest coherent approved change.
5. Add/update required tests.
6. Run focused tests.
7. Run full required verification.
8. Inspect the complete diff.
9. Update phase results, prompt registry, and relevant ADR/docs.
10. Document deferred/new findings.
11. STOP; never automatically start the next phase.

## Mandatory Completion Records

Before completion:
- update `docs/findings/FINDINGS.md`
- update `docs/prompts/README.md`
- create/update the phase result
- update `docs/results/README.md`
- update relevant ADRs/documentation
- verify the complete diff
