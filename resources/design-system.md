# Design System Standards

## Purpose

A design system creates a shared visual and interaction language across the product. It should make the interface more consistent, faster to build, easier to maintain, more accessible, and easier to improve.

## Core Principle

Prefer a small, coherent system over a huge collection of arbitrary tokens and one-off components.

Before creating a new visual rule, check whether an existing token or component already solves the problem.

## Design Tokens

Centralize recurring values for:

- Colors
- Typography
- Spacing
- Radius
- Shadows
- Motion
- Breakpoints
- Elevation/z-index where needed

Prefer semantic tokens over raw implementation values.

Examples:

- `background`
- `foreground`
- `muted`
- `primary`
- `primary-foreground`
- `border`
- `success`
- `warning`
- `destructive`
- `focus-ring`

## Color System

Build a semantic palette rather than scattering raw colors throughout the UI.

Support roles for:

- Background surfaces
- Foreground/text hierarchy
- Borders
- Primary actions
- Secondary actions
- Success
- Warning
- Error/destructive
- Informational states

Reserve strong accent colors for meaningful actions and states.

Do not use accent colors everywhere simply to make the interface look more colorful.

## Typography System

Define a predictable hierarchy:

- Display
- H1
- H2
- H3
- Body large
- Body
- Body small
- Label
- Caption

Typography should scale intentionally across breakpoints.

Avoid creating a separate font size for every component.

## Spacing System

Use a consistent spacing scale.

A practical default can include:

`4, 8, 12, 16, 20, 24, 32, 40, 48, 64, 80, 96, 128`

Use spacing to communicate relationships:

- Tight → strongly related
- Medium → grouped
- Large → separate sections

Do not use arbitrary spacing to compensate for weak layout structure.

## Layout System

Define reusable layout primitives such as:

- Container
- Stack
- Grid
- Section
- Page header
- Sidebar shell

Prefer predictable max-widths and gutters.

Avoid arbitrary widths that break at intermediate viewport sizes.

## Radius System

Define a small set of radii.

Example hierarchy:

- Small controls
- Inputs/buttons
- Cards
- Large surfaces
- Full pills

Equivalent component types should share equivalent radii.

## Elevation and Shadows

Create a restrained elevation hierarchy:

```text
Base → Raised → Floating → Overlay
```

Use subtle shadows for depth. Avoid heavy shadows on every component.

## Surface Hierarchy

Create hierarchy through a controlled combination of:

- Background changes
- Borders
- Elevation
- Typography
- Spacing
- Accent color

Premium interfaces often benefit from subtle tonal separation instead of excessive decoration.

## Component States

Every interactive component should consider:

- Default
- Hover
- Focus-visible
- Active
- Selected
- Disabled
- Loading
- Success
- Error
- Empty where applicable

States should be visually and semantically consistent across the product.

## Buttons

Define a controlled button system.

Common variants:

- Primary
- Secondary
- Outline
- Ghost
- Destructive
- Link

Also define:

- Sizes
- Icon behavior
- Loading state
- Disabled state
- Focus behavior

Do not create custom button styles for every page.

## Inputs

Inputs should share:

- Height system
- Border treatment
- Radius
- Typography
- Focus ring
- Error treatment
- Disabled treatment

Different input types should still feel like members of the same component family.

## Forms

Forms should use consistent:

- Label placement
- Input sizing
- Helper text
- Validation
- Error messaging
- Required/optional treatment
- Action placement

Keep form patterns reusable and accessible.

## Cards

Cards should group meaningful information or actions.

Define consistent:

- Padding
- Radius
- Border
- Surface
- Header/content/footer structure

Do not turn every section into a card.

## Tables

Tables should share predictable:

- Header treatment
- Row height
- Alignment
- Status styles
- Action patterns
- Selection behavior
- Loading/empty/error states

Large datasets should use appropriate pagination or virtualization.

## Feedback Components

Standardize:

- Toasts
- Alerts
- Banners
- Empty states
- Loading states
- Error states
- Success states

Users should not encounter unrelated feedback patterns across different screens.

## Navigation

Navigation should communicate where the user is and what they can do.

Use:

- Stable primary navigation
- Clear active states
- Logical grouping
- Predictable labels
- Search when navigation becomes large

Avoid excessive nesting.

## Responsive System

Breakpoints should be based on layout needs rather than specific device models.

At every breakpoint evaluate:

- Navigation
- Content order
- Grid columns
- Table behavior
- Form layout
- Button placement
- Typography
- Spacing
- Touch targets

Do not simply shrink desktop UI.

## Motion System

Define a small motion vocabulary for:

- State changes
- Navigation feedback
- Progressive disclosure
- Focus/attention

Use motion consistently and respect `prefers-reduced-motion`.

Avoid making every component animate differently.

## Accessibility

Accessibility is part of the design system, not a final QA step.

Define expectations for:

- Semantic HTML
- Keyboard navigation
- Focus visibility
- Accessible names
- Contrast
- Touch targets
- Reduced motion
- State communication

## Dark Mode

If supported, create semantic tokens for both themes.

Do not simply invert colors.

Review:

- Surface hierarchy
- Text contrast
- Borders
- Status colors
- Focus rings
- Images
- Shadows

## Implementation Rules

When working in an existing codebase:

1. Inspect existing tokens and components.
2. Reuse them where appropriate.
3. Extend the system only when a real repeated need exists.
4. Avoid breaking established patterns without a reason.
5. Keep design and implementation terminology aligned.
6. Avoid unnecessary global CSS changes.

## Performance

A design system should encourage efficient implementation.

Prefer:

- Lightweight primitives
- Server-compatible components where possible
- Isolated client behavior
- Optimized assets
- Minimal unnecessary JavaScript
- Reusable components instead of duplicated implementations

Do not add heavy dependencies merely for a small visual effect.

## Documentation

Document meaningful system decisions.

For important components, document:

- Purpose
- Variants
- Usage
- States
- Accessibility requirements
- Important constraints

## Quality Review

Ask:

- Is the UI consistent?
- Can spacing be improved?
- Can typography be improved?
- Are colors semantic?
- Are components reusable?
- Are component states complete?
- Is accessibility built into the system?
- Does the system support responsive layouts?
- Does it encourage performant implementations?
- Does it support a premium visual language without excessive decoration?
- Is the system simple enough for developers to use correctly?
- Is this something I'd be proud to ship?
