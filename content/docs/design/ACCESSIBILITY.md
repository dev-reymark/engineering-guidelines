# Accessibility Standard

Status: Draft

Target: Define the applicable accessibility target for this project. WCAG 2.2 AA is a common baseline for web applications unless project requirements specify otherwise.

## Required Practices

- Use semantic HTML/native controls where possible.
- Ensure keyboard access to interactive functionality.
- Provide visible focus indicators.
- Maintain logical focus order.
- Provide accessible names for controls.
- Associate labels and form fields correctly.
- Announce meaningful dynamic status/error changes where needed.
- Do not rely on color alone to communicate state.
- Maintain sufficient contrast.
- Provide text alternatives for meaningful images.
- Hide decorative imagery/icons appropriately from assistive technology.
- Ensure dialogs manage focus correctly.
- Ensure errors are identifiable and understandable.
- Respect reduced-motion preferences.
- Support zoom/text resizing without loss of critical functionality where applicable.

## Touch Targets

Define a minimum target appropriate to the product and platform.
Avoid controls that require high pointer precision.

## Tables

Use proper headers and semantics.
Do not simulate data tables with arbitrary div structures when a semantic table is appropriate.

## Testing

Use a combination of:
- automated accessibility checks
- keyboard testing
- focus testing
- screen-reader spot checks for critical workflows
- contrast review
- responsive/zoom review

Automated checks alone are insufficient.
