# Prompt & Execution Registry

This registry tracks significant AI-agent work.

The exact prompt for each significant task must be stored as `XXX-descriptive-name.md`.
Do not fabricate historical prompts that were not preserved.

## Prompt Status

- Draft
- Approved
- In Progress
- Completed
- Blocked
- Superseded

## Registry

| ID | Prompt | Type | Status | Depends On | Findings / Requirements | Result |
|---|---|---|---|---|---|---|
| 000 | Project Discovery | Discovery | Draft | — | — | — |

## Required Prompt Metadata

Each prompt document should record:

- Prompt ID
- Title
- Status
- Created date
- Approved/executed date when applicable
- Type
- Implementation allowed?
- Production code changes allowed?
- Dependencies
- Findings/requirements addressed
- Expected outputs
- Required result document
- Purpose
- Exact prompt

## Rules

1. Use sequential IDs: 000, 001, 002...
2. Store the exact significant execution prompt.
3. Update status as work progresses.
4. `Completed` means the task was actually completed, not merely attempted.
5. Every implementation/remediation prompt must identify its required result document.
6. Link applicable findings/requirements.
7. Never rewrite an executed prompt to make history look cleaner; supersede it with a new prompt when necessary.
