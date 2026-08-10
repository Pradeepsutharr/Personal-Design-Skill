# Motion Standards

Motion should make the interface feel responsive, understandable, and premium without adding unnecessary client-side cost.

## Principles

- Every animation needs a purpose.
- Prefer subtle motion over spectacle.
- Keep interaction feedback fast.
- Preserve usability when motion is disabled.
- Avoid animation that causes layout shifts.

## Motion Hierarchy

### Micro interactions

Use for:

- Hover
- Focus
- Toggle changes
- Button feedback
- Small state changes

### Component transitions

Use for:

- Dialogs
- Drawers
- Dropdowns
- Tabs
- Expand/collapse

Motion should communicate spatial relationships.

### Page/section motion

Use sparingly for:

- Hero entrances
- Section reveals
- Major transitions

Do not make important content depend on an entrance animation.

## Timing

Use short, consistent durations.

Suggested starting ranges:

- Micro feedback: 100–150ms
- Standard interaction: 150–250ms
- Larger surface transition: 250–400ms

Tune based on the actual interaction rather than applying a duration mechanically.

## Performance

Prefer animating:

- `transform`
- `opacity`

Avoid frequent animation of layout properties such as:

- `width`
- `height`
- `top`
- `left`

Avoid expensive continuous effects such as large blur regions or heavy shadow animation.

## CSS vs JavaScript

Use CSS transitions for simple state changes.

Use JavaScript animation libraries only when sequencing, gestures, physics, or complex state-driven animation genuinely requires them.

Do not introduce a large animation dependency for a simple hover transition.

## Reduced Motion

Respect `prefers-reduced-motion`.

Reduce or remove decorative movement while preserving understandable state changes.

## Mobile

Reduce heavy effects on mobile and lower-powered devices where appropriate.

Avoid excessive parallax and continuous decorative animation.

## Accessibility

Motion must never:

- Prevent interaction
- Hide important information
- Trap focus
- Flash rapidly
- Become necessary to understand state

## Review

Before shipping, ask:

- Does this animation improve UX?
- Can CSS handle it?
- Can it use transform/opacity?
- Does it cause layout shift?
- Is it smooth on lower-powered devices?
- Does reduced motion work?
- Is the interface still excellent with motion disabled?
