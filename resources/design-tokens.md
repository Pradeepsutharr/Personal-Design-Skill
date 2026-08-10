# Design Tokens Standards

Design tokens are the shared vocabulary between design and implementation.

## Core Principle

Use semantic tokens for repeated visual decisions instead of scattering raw values throughout components.

## Token Categories

Define tokens for:

- Colors
- Typography
- Spacing
- Radius
- Shadows/elevation
- Motion
- Breakpoints
- Z-index where required

## Semantic Naming

Prefer names based on purpose:

- `background`
- `surface`
- `foreground`
- `muted`
- `primary`
- `border`
- `success`
- `warning`
- `destructive`
- `focus-ring`

Avoid names tied to a specific page such as `blue-card` or `dashboard-gray`.

## Color Tokens

Keep raw palette values separate from semantic roles when the design system is large enough to justify it.

Example:

```css
--color-primary: ...;
--color-primary-foreground: ...;
--color-background: ...;
--color-surface: ...;
--color-border: ...;
```

## Spacing Tokens

Use a predictable scale rather than arbitrary values everywhere.

Spacing should communicate relationships:

- Small → related elements
- Medium → groups
- Large → sections

## Typography Tokens

Create tokens for meaningful type roles rather than every possible size.

Example roles:

- Display
- Heading
- Body
- Label
- Caption

## Radius Tokens

Use a small radius vocabulary across equivalent components.

Do not create a unique radius for every card or button.

## Shadow Tokens

Define elevation levels rather than arbitrary shadows.

Use the smallest elevation that clearly communicates hierarchy.

## Motion Tokens

Standardize common durations and easing values so interactions feel consistent.

Respect reduced-motion preferences.

## Responsive Tokens

Breakpoints should describe layout changes rather than device names.

Do not add breakpoints simply to patch isolated problems.

## Implementation Rules

When working in an existing project:

1. Inspect existing tokens first.
2. Reuse existing semantic values.
3. Add a token only for a repeated need.
4. Avoid breaking existing components unnecessarily.
5. Keep tokens discoverable and documented.

## Quality Review

Ask:

- Is the token semantic?
- Is it reused enough to justify abstraction?
- Does it improve consistency?
- Does it support responsive design?
- Does it preserve accessibility?
- Does it help the UI remain visually premium?
- Does it reduce future maintenance?
