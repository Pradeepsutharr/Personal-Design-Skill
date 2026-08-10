# Color System Standards

## Purpose

Color should create hierarchy, communicate meaning, reinforce brand identity, and make interfaces feel polished. Premium products use color with restraint and consistency.

## Core Principle

Do not choose colors one component at a time. Establish semantic roles first, then apply those roles consistently across the product.

## Semantic Roles

Define at minimum:

- Background
- Surface
- Surface elevated
- Surface muted
- Foreground
- Foreground secondary
- Foreground muted
- Border
- Border strong
- Primary
- Primary foreground
- Secondary
- Accent
- Success
- Warning
- Destructive
- Focus ring

Prefer semantic tokens such as `--color-primary` rather than scattering raw color values throughout components.

## Neutral Foundation

A strong SaaS interface usually begins with a carefully tuned neutral scale.

Use neutrals for:

- Page background
- Cards and surfaces
- Borders
- Primary text
- Secondary text
- Disabled text

Avoid using pure black and pure white everywhere when a slightly softened neutral creates better visual comfort.

## Accent Color

Use one primary accent to establish product identity.

Accent color should generally be reserved for:

- Primary CTAs
- Important links
- Selected states
- Key metrics
- Active navigation
- Product highlights

Do not make every element colorful. Scarcity makes the accent more meaningful.

## Status Colors

Use consistent semantic colors.

### Success

For completed, healthy, enabled, or positive states.

### Warning

For attention, caution, or incomplete states.

### Destructive

For errors, destructive actions, failed operations, or irreversible actions.

### Informational

For neutral guidance or system information.

Status colors should not be the only indicator. Pair them with text, icons, patterns, or labels when appropriate.

## Contrast

Accessibility is mandatory.

Verify text and interactive elements have sufficient contrast against their backgrounds. Do not use low-contrast gray text merely because it looks fashionable.

Important content must remain readable in bright and dark environments.

## Dark Mode

Dark mode should be designed as a system, not implemented by simply swapping black and white.

Consider:

- Elevated surface levels
- Border visibility
- Text contrast
- Accent intensity
- Shadow visibility
- Status colors
- Chart colors

Use layered dark neutrals rather than a single black surface everywhere.

## Gradients

Gradients can create premium visual moments when used intentionally.

Good uses:

- Hero atmosphere
- Brand highlights
- Background glow
- Large feature visuals
- Subtle CTA emphasis

Avoid:

- Gradients on every card
- Rainbow gradients without brand purpose
- High-saturation backgrounds behind readable text
- Decorative gradients that increase visual noise

## Glass and Transparency

Use glass effects selectively.

If using transparency:

- Maintain readable contrast.
- Provide a stable fallback surface.
- Avoid excessive blur.
- Do not make important information visually unstable.

Glass should enhance depth, not become the entire design language.

## Color Hierarchy

A useful hierarchy is:

1. Primary action/accent
2. Important content
3. Secondary content
4. Supporting metadata
5. Background and structural surfaces

If everything has high contrast, nothing has hierarchy.

## Data Visualization

Charts need accessible and distinguishable colors.

- Avoid relying on red vs green alone.
- Use enough perceptual separation between series.
- Keep the palette consistent across the product.
- Reserve semantic colors for semantic meanings.
- Use labels and legends clearly.

## Interactive States

Every interactive element should have clear visual feedback for:

- Hover
- Focus-visible
- Active
- Selected
- Disabled
- Loading

Do not change colors so subtly that users cannot recognize the state.

## Brand Consistency

Once a primary palette is established, reuse it across:

- Buttons
- Links
- Navigation
- Forms
- Notifications
- Charts
- Illustrations
- Marketing sections

Do not introduce new accent colors without a clear reason.

## Color and Performance

Prefer simple CSS colors, gradients, and effects over heavy image assets when the visual can be produced efficiently in CSS.

Avoid unnecessarily expensive filters and large decorative assets.

## Color Review

Before shipping, ask:

- Is the palette visually premium?
- Is the accent used with restraint?
- Is hierarchy obvious?
- Is contrast accessible?
- Are status colors semantically consistent?
- Does dark mode feel intentionally designed?
- Are gradients purposeful?
- Is the UI too colorful or too flat?
- Do charts remain understandable?
- Does every component belong to the same visual system?
