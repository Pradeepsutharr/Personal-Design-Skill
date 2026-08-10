# Tailwind CSS Standards

## Purpose

Use Tailwind CSS to implement consistent, responsive, accessible, and maintainable interfaces without turning utility classes into an unstructured collection of arbitrary values.

## Core Principle

Tailwind is the implementation layer for the design system, not a replacement for the design system.

Follow the project's existing tokens, spacing scale, typography, color roles, and component conventions.

## Use the Existing System

Before adding new classes or values, inspect the project.

Look for:

- Existing design tokens
- Theme configuration
- CSS variables
- Shared components
- Utility classes
- Existing responsive conventions

Do not introduce a second visual system accidentally.

## Prefer Design Tokens

Use semantic CSS variables and theme tokens for values that represent product roles.

Prefer:

- Primary color token
- Surface token
- Border token
- Foreground token
- Spacing token
- Radius token

Avoid scattering raw hex values throughout JSX when a semantic token already exists.

## Avoid Arbitrary Values by Default

Arbitrary values are useful for genuine one-off optical adjustments, but should not become the normal design strategy.

Before using an arbitrary value, ask:

- Does an existing token solve this?
- Should this value become part of the design system?
- Is this truly a one-off requirement?

## Responsive Design

Use mobile-first responsive utilities.

Design the base layout for smaller screens, then progressively enhance it for larger viewports.

Explicitly consider:

- Container width
- Grid columns
- Flex direction
- Typography
- Padding
- Gap
- Navigation
- Table behavior
- Form layout

Do not rely on desktop layouts merely shrinking automatically.

## Class Organization

Keep class strings understandable.

When a class list becomes difficult to read or repeated across multiple components, consider:

- Component extraction
- A reusable variant pattern
- A shared component
- A small semantic utility

Do not create abstractions merely to shorten a class string.

## Component Variants

For components with meaningful variants, use a predictable variant strategy.

Examples:

- Button: primary, secondary, destructive, ghost
- Badge: success, warning, error, neutral
- Card: default, elevated, interactive

Keep variant behavior consistent across the application.

## Spacing

Use the project's spacing scale.

Default to a consistent 8px-oriented rhythm where the design system supports it.

Avoid arbitrary margins and padding that create visual drift between components.

## Typography

Use the established typography tokens.

Do not create random text sizes for every heading.

Responsive typography should be intentional and can use fluid sizing when it improves the design.

## Colors

Use semantic color tokens.

Avoid raw color values when an existing design token represents the intended role.

Keep status colors consistent across:

- Alerts
- Badges
- Tables
- Forms
- Charts
- Notifications

## States

Tailwind should express all relevant component states:

- `hover:`
- `focus-visible:`
- `active:`
- `disabled:`
- `aria-*`
- `data-*`
- `group-*`
- `peer-*`

Use visible focus styles.

## Accessibility

Do not use Tailwind utilities to visually hide important interactive information without ensuring it remains accessible appropriately.

Be careful with:

- `hidden`
- `opacity-0`
- `pointer-events-none`
- `sr-only`
- Disabled-looking elements that remain interactive

Visual state and semantic state must agree.

## Layout

Prefer flex and grid for layout.

Use:

- `flex` for one-dimensional relationships
- `grid` for two-dimensional structures
- `gap-*` for collection spacing
- `max-w-*` for readable content widths
- `mx-auto` for centered containers

Avoid layout hacks involving excessive absolute positioning.

## Absolute Positioning

Absolute positioning is appropriate for:

- Badges attached to controls
- Decorative backgrounds
- Floating controls
- Overlay elements
- Intentional visual compositions

Do not use absolute positioning to compensate for poor layout structure.

## Containers

Use consistent container conventions across pages.

A typical pattern may include:

- Full-width section
- Centered inner container
- Responsive horizontal padding
- Maximum readable width

Keep major sections aligned.

## Responsive Navigation

For mobile navigation:

- Provide an obvious trigger.
- Ensure keyboard access.
- Preserve focus behavior.
- Avoid horizontal overflow.
- Keep important actions accessible.

## Dark Mode

Use the project's theme strategy rather than independently styling every component.

Verify:

- Contrast
- Borders
- Surfaces
- Status colors
- Inputs
- Focus states
- Shadows

Dark mode should feel intentionally designed.

## Animation

Use Tailwind transitions for simple interactions.

Good candidates:

- Color transitions
- Opacity
- Transform
- Border changes

Avoid excessive animation utilities across large DOM trees.

Respect reduced motion where appropriate.

## Performance

Tailwind itself should not become an excuse for inefficient UI.

Performance still depends on:

- DOM size
- React rendering
- Client JavaScript
- Images
- Fonts
- Dependencies
- Animation strategy

Do not create huge DOM trees merely because utility classes make them easy to write.

## Avoid Overuse of `!important`

Do not use important modifiers as a normal conflict-resolution strategy.

If styles conflict, determine why and fix the architecture or class ordering.

Use important modifiers only when there is a clear and justified need.

## Existing CSS

When a project already contains global CSS or a component library:

- Understand the cascade before modifying it.
- Avoid destructive global resets.
- Avoid overriding library styles globally for a single component.
- Scope custom styles appropriately.

## Component Libraries

When using Tailwind with shadcn/ui, Ant Design, or another component library:

- Preserve the library's accessibility behavior.
- Customize through supported APIs where possible.
- Avoid duplicating a component the library already provides unless the custom behavior is justified.
- Maintain visual consistency between library and custom components.

## Tailwind Review

Before shipping, ask:

- Is the design system being followed?
- Are tokens used instead of arbitrary values where possible?
- Is the class structure maintainable?
- Are responsive states handled?
- Are focus and accessibility states present?
- Is dark mode consistent if supported?
- Are components reusable?
- Is absolute positioning being used intentionally?
- Is the DOM structure reasonable?
- Is the UI visually premium?
