# UX Guidelines

Status: Draft

## Primary Workflows

Document the project's highest-value workflows and optimize those first.

For each important workflow define:
- entry point
- required information
- decision points
- success state
- recoverable failures
- destructive transitions
- permission requirements
- exit/cancel behavior

## Navigation

Navigation should reflect user tasks and product domains rather than implementation details.

Users should be able to understand:
- current location
- available next actions
- how to return safely

## Feedback

Every meaningful user action should have appropriate feedback.

Avoid both:
- silent success/failure
- excessive notifications for trivial actions

## Forms

Prefer:
- clear labels
- logical grouping
- useful defaults
- progressive disclosure
- preserving entered data after validation failures

Do not request information before it is needed without a product reason.

## Validation

Client validation improves UX.
Server validation remains authoritative.

Explain how to correct an error rather than merely saying input is invalid.

## Confirmation

Do not add confirmation dialogs to every action.

Use confirmation when:
- action is destructive
- action is financially significant
- action has external effects
- action is difficult to reverse
- accidental execution is plausible

## Optimistic UI

Use optimistic UI only when failure can be safely reconciled.

Financial, security-sensitive, inventory-critical, or irreversible operations should not appear finalized before authoritative confirmation unless the design explicitly handles reconciliation.

## Search and Filtering

Document:
- default sort
- search scope
- filters
- reset behavior
- URL/state persistence where useful
- empty results

## Keyboard and Power Users

For workflow-heavy applications, define useful keyboard behavior without making keyboard use mandatory.

## Touch Workflows

For touch-heavy products such as POS systems:
- prioritize large targets
- minimize precision requirements
- reduce unnecessary typing
- make primary actions easy to reach
- prevent accidental destructive actions

## Notifications

Choose the least disruptive feedback mechanism that communicates the result.

## Unsaved Changes

Define whether and how users are warned about meaningful unsaved work.

## Permissions

Do not hide the existence of important capabilities when users benefit from understanding why access is unavailable.
Use appropriate disabled/permission messaging.
