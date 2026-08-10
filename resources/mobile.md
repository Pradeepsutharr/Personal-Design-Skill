# Mobile UI Standards

## Purpose

Mobile design is not a smaller desktop layout. It is a deliberate experience optimized for touch, limited space, variable connectivity, and one-handed interaction.

## Core Principle

Preserve the user's primary task while removing unnecessary complexity.

Before adapting a desktop screen, identify:

- Primary mobile task
- Most important information
- Essential actions
- Secondary information that can move or collapse
- Interactions that need a different mobile pattern

## Mobile-First Thinking

Start with the smallest practical layout and progressively enhance it.

Consider:

- Content priority
- Touch targets
- Navigation
- Typography
- Spacing
- Form behavior
- Table strategy
- Image sizing
- Loading performance

## Touch Targets

Interactive controls should be comfortably tappable.

Avoid tiny icon buttons and tightly packed actions. Provide sufficient spacing between adjacent controls to reduce accidental taps.

## Navigation

Mobile navigation should be simple and predictable.

Use appropriate patterns such as:

- Menu drawer
- Bottom navigation for a small set of primary destinations
- Contextual navigation
- Sticky action areas where appropriate

Do not hide essential actions behind multiple layers of menus.

## Header

Mobile headers should prioritize:

- Current context
- Navigation access
- Essential action

Avoid placing too many controls into a narrow header.

## Content Priority

When desktop content does not fit:

1. Keep primary task content.
2. Keep critical actions.
3. Move secondary details below.
4. Collapse optional controls.
5. Remove purely decorative content when necessary.

Do not simply shrink every element until it fits.

## Typography

Maintain readable body text on small screens.

Reduce display typography when needed, but preserve strong hierarchy.

Avoid headings that wrap into awkward shapes or consume the majority of the viewport.

## Spacing

Reduce large desktop spacing where appropriate, but keep enough breathing room for touch interaction and readability.

Do not eliminate spacing merely to fit more content.

## Forms

Mobile forms should:

- Use comfortable inputs.
- Use appropriate input types.
- Avoid unnecessary multi-column layouts.
- Keep labels visible.
- Make validation understandable.
- Keep primary actions reachable.

Long forms should use logical sections and progressive disclosure when appropriate.

## Tables

Do not force a desktop table into a tiny viewport.

Choose among:

- Horizontal scrolling
- Priority columns
- Responsive row/card representation
- Detail page/drawer
- Column visibility controls

The right choice depends on whether users need comparison, scanning, or record-level actions.

## Modals and Drawers

On mobile, large desktop modals often work better as full-screen or near-full-screen surfaces.

Ensure:

- Clear close control
- Keyboard support where applicable
- Safe-area awareness
- Scrollable content
- Accessible focus behavior

## Sticky Actions

Sticky bottom actions can be useful for important workflows, but avoid covering content.

Use them for actions such as:

- Save
- Checkout
- Continue
- Confirm

Provide enough bottom padding so content remains accessible.

## Horizontal Scrolling

Horizontal scrolling can be valid for:

- Data tables
- Carousels
- Wide visualizations

Do not create accidental horizontal scrolling across the entire page.

## Images

Optimize images aggressively for mobile.

- Use responsive sizes.
- Avoid oversized assets.
- Lazy-load below-the-fold imagery.
- Reserve layout space.
- Prioritize only genuinely important above-the-fold images.

## Performance

Mobile devices can have slower CPUs, memory constraints, and variable networks.

Prioritize:

- Small JavaScript payloads
- Optimized images
- Efficient rendering
- Limited animation
- Fast initial content
- Progressive loading

Do not assume desktop hardware performance.

## Motion

Keep mobile motion subtle.

Avoid excessive parallax, large transitions, or continuous effects that consume battery or distract users.

Respect reduced-motion preferences.

## Accessibility

Verify mobile layouts with:

- Zoom
- Text scaling
- Keyboard where relevant
- Screen readers
- Touch interaction
- Focus states
- Contrast

Accessibility should not disappear at mobile breakpoints.

## Safe Areas

When using full-screen mobile UI or fixed controls, account for device safe areas where applicable.

Do not place important controls directly against system UI boundaries.

## Empty and Error States

Mobile error and empty states should remain concise and actionable.

Do not create oversized illustrations that push the actual action below the fold.

## Mobile Review

Before shipping, ask:

- Is this intentionally designed for mobile?
- Can the primary task be completed comfortably with one hand where practical?
- Are touch targets comfortable?
- Is navigation simple?
- Is typography readable?
- Is horizontal overflow controlled?
- Are tables and forms adapted correctly?
- Are sticky controls useful rather than intrusive?
- Are images optimized?
- Is client JavaScript minimized?
- Does the experience remain accessible?
- Does it still feel premium?
- Is this something I'd be proud to ship?
