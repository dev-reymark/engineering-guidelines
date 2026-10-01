# Design System

Status: Draft
Version: 1.0

## 1. Design Principles

Define 3–6 principles for the product, for example:
- clear
- consistent
- efficient
- accessible
- calm
- trustworthy

## 2. Brand Foundation

Document:
- product personality
- logo usage
- brand colors
- imagery/illustration direction
- icon direction
- light/dark mode policy

## 3. Design Tokens

Prefer semantic tokens over arbitrary values.

### Color

Define semantic roles such as:
- background
- surface
- surface-muted
- foreground
- foreground-muted
- border
- primary
- primary-foreground
- secondary
- success
- warning
- danger
- info
- focus

Do not encode meaning by color alone.

### Typography

Define:
- font families
- display
- heading levels
- body
- small/meta
- labels
- numeric/tabular styles where needed

### Spacing

Define a consistent spacing scale.

### Radius

Define a small radius scale.

### Elevation / Shadows

Use only when hierarchy requires it.

### Motion

Define:
- duration
- easing
- reduced-motion behavior

## 4. Layout

Document:
- content widths
- page gutters
- grids
- sidebars
- headers
- dense vs comfortable layouts

## 5. Breakpoints

Reference `RESPONSIVE-DESIGN.md`.

## 6. Icons

Define:
- icon library
- default sizes
- stroke/fill conventions
- accessible labeling rules

Do not mix icon libraries without a reason.

## 7. Core Components

For every component define variants, sizes, states, accessibility, and usage.

Cover as applicable:
- Button
- Icon Button
- Link
- Input
- Textarea
- Select
- Combobox
- Checkbox
- Radio
- Switch
- Form Field
- Date/Time Input
- Search
- Card
- Table/Data Grid
- List
- Badge
- Alert
- Toast
- Dialog/Modal
- Drawer/Sheet
- Dropdown/Menu
- Tabs
- Tooltip
- Popover
- Pagination
- Breadcrumb
- Navigation
- Sidebar
- Header
- Empty State
- Loading State
- Skeleton
- Error State
- Confirmation Dialog

## 8. Component State Standard

Consider, where applicable:
- default
- hover
- focus-visible
- active
- selected
- disabled
- loading
- success
- warning
- error
- read-only
- permission denied

## 9. Forms

Define:
- label placement
- required/optional indication
- help text
- validation timing
- error placement
- disabled/read-only behavior
- submit/loading behavior
- destructive confirmation

## 10. Tables and Data-Dense UI

Define:
- alignment
- numeric formatting
- sorting
- filtering
- pagination
- empty/loading/error states
- row actions
- bulk actions
- mobile fallback

## 11. Feedback

Define appropriate use of:
- inline validation
- alerts
- toast notifications
- progress indicators
- confirmation screens

## 12. Accessibility

`ACCESSIBILITY.md` is authoritative for accessibility requirements.

## 13. Responsive Behavior

`RESPONSIVE-DESIGN.md` is authoritative for responsive behavior.

## 14. Implementation Mapping

Document how design tokens map to the project's actual implementation:
- CSS variables
- Tailwind theme
- component library
- native styles
- other framework

Do not create a second competing token system.
