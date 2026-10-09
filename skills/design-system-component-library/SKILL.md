---
name: design-system-component-library
description: Use when defining, standardizing, refactoring, or scaling a reusable design system and component library across a website or web application.
---

# Design System and Component Library

## Objective
Create a coherent reusable visual and interaction system so the product feels like one system instead of a collection of one-off pages.

## Start with foundations

Define tokens before creating many components.

### Color tokens
Use semantic roles:
- background
- surface
- elevated surface
- text primary
- text secondary
- muted
- border
- brand primary
- brand secondary
- accent
- success
- warning
- danger
- info

Avoid using raw hex values repeatedly throughout components.

### Typography tokens
Define:
- display
- H1
- H2
- H3
- body large
- body
- small
- label
- caption
- mono/code when relevant

For each define:
- font family
- size
- line height
- weight
- letter spacing

### Spacing
Use a deliberate spacing scale.

Example logic:
4 / 8 / 12 / 16 / 24 / 32 / 48 / 64 / 96

The exact scale may vary, but avoid arbitrary spacing values everywhere.

### Radius
Define a small radius family:
- small
- medium
- large
- full

Do not randomly mix many corner styles.

### Shadows
Define:
- subtle
- elevated
- modal/overlay

Prefer borders and spacing over heavy shadows when possible.

### Layout
Define:
- max content width
- narrow text width
- section spacing
- gutters
- grid behavior
- responsive breakpoints

## Component hierarchy

Build components in layers.

### Primitives
- Button
- Link
- Input
- Textarea
- Select
- Checkbox
- Radio
- Switch
- Badge
- Icon
- Divider
- Skeleton

### Composite components
- FormField
- SearchInput
- Card
- ProductCard
- PricingCard
- Testimonial
- Alert
- Toast
- Accordion
- Tabs
- Breadcrumb
- Pagination
- Dropdown
- Tooltip

### Structural components
- Header
- Navigation
- Sidebar
- Footer
- Section
- Container
- Grid
- Modal
- Drawer
- Command palette

## Component API rules

A component should:
- solve one clear UI problem
- have predictable props
- avoid huge prop surfaces
- expose variants only when genuinely needed
- remain composable
- support accessibility by default

Avoid components with dozens of boolean props.

Prefer clear variants:
- size
- intent
- emphasis
- state

## Variants

Use controlled variants instead of copy-pasted component forks.

Example for buttons:
- primary
- secondary
- outline
- ghost
- destructive

Sizes:
- small
- medium
- large

States:
- default
- hover
- focus
- active
- disabled
- loading

## Accessibility built in

Components should ship with:
- semantic roles
- keyboard behavior
- focus styles
- labels
- aria attributes only when necessary
- disabled/loading behavior
- contrast compliance

Accessibility should not be added after implementation.

## Responsive behavior

Define component behavior across breakpoints.

Examples:
- navigation collapses intentionally
- cards stack predictably
- tables adapt or become scrollable
- buttons remain usable
- modals become drawers when appropriate
- spacing scales down consistently

Avoid component-specific breakpoint chaos.

## States

Every interactive/data component should consider:
- default
- hover
- focus
- active
- disabled
- loading
- empty
- error
- success

Do not design only the happy path.

## Content resilience

Components must tolerate:
- long titles
- translated text
- missing images
- large numbers
- empty values
- variable list lengths

Avoid designs that only work with demo content.

## Tailwind / shadcn guidance

When using Tailwind/shadcn:
- centralize tokens in theme variables
- extend primitives instead of duplicating them
- keep variant logic consistent
- avoid excessive arbitrary values
- preserve accessible Radix/shadcn behaviors
- customize styling without breaking interaction semantics

## Documentation

For important components document:
- purpose
- variants
- props
- accessibility notes
- usage examples
- anti-patterns

## Refactoring existing UI

When standardizing an existing product:
1. audit repeated patterns
2. identify near-duplicate components
3. define tokens
4. choose canonical primitives
5. migrate incrementally
6. verify visual regressions
7. remove obsolete duplicates

Do not rewrite the whole UI at once without need.

## Quality gate

Before calling the system mature, verify:
- color tokens are semantic
- typography hierarchy is consistent
- spacing follows a scale
- components share interaction language
- states are covered
- accessibility is built in
- mobile behavior is predictable
- new pages can be built without inventing new visual rules each time
