# Prompt XXX — [Audit Name]

Status: Draft
Created: YYYY-MM-DD
Executed:
Type: Audit
Implementation Allowed: No
Production Code Changes Allowed: No

Depends On:
- ...

Expected Outputs:
- ...

Purpose:
...

---

# Exact Execution Prompt

Read `AGENTS.md`, `docs/ENGINEERING-STANDARD.md`, and all relevant project documentation first.

## Objective

## Scope

## Allowed Changes
Documentation only unless explicitly stated.

## Forbidden Changes
- production behavior
- schema/migrations
- dependencies
- unrelated refactors

## Required Inspection

## Finding Namespace
Use `[PREFIX]-001`, `[PREFIX]-002`, ... without renumbering published findings.

## Finding Format
- Severity
- Area
- Current behavior
- Evidence
- Problem
- Risk
- Target behavior
- Tests required
- Related requirements/decisions
- Status

## Required Outputs

## Verification
Confirm production code/schema/dependencies were not modified and run baseline verification where appropriate.

## Completion
Recommend the next phase and STOP. Do not implement findings.
