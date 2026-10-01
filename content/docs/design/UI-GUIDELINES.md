# UI Guidelines

Status: Draft

## Consistency

Reuse existing components and tokens before creating new ones.

Do not introduce:
- arbitrary colors
- arbitrary spacing
- duplicate components
- one-off typography systems
- inconsistent border radii
- unexplained icon libraries

## Visual Hierarchy

Each screen should make clear:
1. where the user is
2. what the primary task is
3. what the primary action is
4. what information is secondary
5. what actions are destructive or exceptional

## Component Composition

Prefer reusable primitives and composed domain components.

Do not turn every small piece of markup into a component.

## Page States

Consider, where applicable:
- initial/loading
- populated
- empty
- filtered-empty
- error
- offline
- permission denied
- disabled/unavailable
- success

## Forms

- Use persistent labels for important inputs.
- Keep validation close to the field.
- Preserve user input after recoverable errors.
- Prevent accidental duplicate submission.
- Clearly distinguish destructive actions.
- Use appropriate input types and autocomplete semantics.

## Destructive Actions

Destructive actions must:
- be visually distinguishable
- require confirmation when impact is significant or difficult to reverse
- explain the object/action being affected
- avoid ambiguous labels such as `OK`

## Data Presentation

Use tables for genuinely tabular data.
Use cards/lists when comparison across columns is not important.

Numbers, currency, dates, and statuses should use consistent formatting.

## Loading

Avoid layout jumps where practical.
Use skeletons only when they improve comprehension.
Use progress indicators for operations that materially take time.

## Empty States

Explain:
- what is empty
- why it may be empty
- the next useful action, when one exists

## Error States

Errors should explain what happened in user-appropriate language and what the user can do next.

Do not expose raw stack traces, database errors, or secrets.
