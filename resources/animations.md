# Animation and Motion Standards

## Purpose

Motion should make interfaces feel responsive, understandable, and premium. Animation is a communication tool, not decoration.

## Core Principle

Every animation should have a reason.

Use motion to:

- Explain a state change
- Establish spatial relationships
- Confirm an action
- Guide attention
- Reduce perceived waiting time
- Add subtle product personality

Do not animate simply because an element can move.

## Motion Hierarchy

Use different levels of motion based on importance.

### Micro motion

For:

- Button hover
- Icon transitions
- Input focus
- Toggle changes
- Small state changes

These should be fast and subtle.

### Component motion

For:

- Dropdowns
- Tooltips
- Modals
- Drawers
- Tabs
- Expanding panels

The motion should communicate where the component came from and where it is going.

### Page motion

For:

- Page transitions
- Hero entrances
- Section reveals
- Large layout changes

Use sparingly. The content should remain usable without animation.

## Timing

Use short durations for interaction feedback.

Suggested starting points:

- Instant feedback: 100–150ms
- Standard interaction: 150–250ms
- Larger surface transition: 250–400ms
- Complex entrance: 400–600ms only when justified

Avoid slow animations for basic interactions.

## Easing

Use easing that feels natural.

- Entering: ease-out
- Exiting: ease-in
- Reversible movement: ease-in-out
- Spring motion: use carefully for physical or playful interactions

Avoid excessive bouncing in enterprise applications.

## Performance

Prefer animations using:

- `transform`
- `opacity`

Avoid animating expensive layout properties when possible, including frequent changes to:

- `width`
- `height`
- `top`
- `left`
- large `box-shadow` changes

Use GPU-friendly transforms where appropriate.

Do not create animations that cause continuous expensive rendering.

## Framer Motion

When Framer Motion is available:

- Keep motion components focused.
- Avoid making the entire page a client component unnecessarily.
- Keep animation logic close to the interactive component.
- Prefer variants for reusable animation states.
- Avoid deeply nested animated trees when unnecessary.
- Respect reduced-motion preferences.

## CSS Animation

Prefer CSS transitions for simple state changes.

Examples:

- Hover color
- Opacity
- Transform
- Border color
- Background transition

Use JavaScript-driven animation only when state or sequencing actually requires it.

## Hover States

Hover should provide subtle feedback.

Good examples:

- Slight elevation
- Small translation
- Border emphasis
- Background shift
- Icon movement

Avoid large scaling that makes layouts jump.

## Button Motion

Buttons should respond quickly.

Appropriate effects include:

- Background transition
- Slight elevation
- Icon translation
- Press feedback

Avoid exaggerated bounce or large transforms.

## Modal and Drawer Motion

Dialogs and drawers should communicate their spatial origin.

- Dialogs can fade and slightly scale.
- Side drawers can slide from their edge.
- Backdrops can fade smoothly.

Keep transitions short enough that users never feel blocked by animation.

## List Animation

Use staggered entry only when it improves comprehension.

Avoid animating dozens or hundreds of rows individually. For large datasets, prioritize performance over visual effects.

## Skeletons

Skeleton loading can use subtle opacity or shimmer, but avoid aggressive animated gradients.

Prefer a calm loading state that does not distract from the content.

## Scroll Motion

Scroll-triggered effects should be subtle.

Do not hide essential information behind animation.

Avoid excessive parallax, especially on mobile devices.

## Reduced Motion

Respect the user's reduced-motion preference.

Where appropriate:

- Disable decorative movement.
- Reduce transition distance.
- Keep state changes understandable without animation.

## Motion and Accessibility

Animation must never prevent users from completing a task.

Do not:

- Flash content rapidly
- Trap focus during animated transitions
- Hide important state changes
- Require animation to understand content

## Motion and SEO

Motion should not prevent important content from being present in the initial document or accessible rendering path.

Do not hide meaningful SEO content solely because an animation has not completed.

## Motion and Performance Review

Before shipping, ask:

- Does this animation improve UX?
- Can it be implemented with transform and opacity?
- Does it cause layout shift?
- Is it smooth on lower-powered devices?
- Is the amount of motion appropriate?
- Does reduced motion work?
- Is JavaScript required for this animation?
- Could CSS handle it more efficiently?
- Is the interface still excellent with motion disabled?
