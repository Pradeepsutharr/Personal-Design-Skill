# Design System Standards

## Purpose

Use this document as the reference for creating cohesive, premium interfaces. A design system is not a collection of decoration; it is a repeatable set of decisions that makes an entire product feel intentional.

## 1. Design System First

Before implementing a substantial UI, identify:

- Primary user goal
- Information hierarchy
- Page structure
- Layout primitives
- Typography hierarchy
- Color roles
- Spacing scale
- Component variants
- Interaction states
- Responsive behavior
- Accessibility requirements

Do not invent each component independently. Reuse the same visual language throughout the product.

## 2. Design Tokens

Prefer semantic tokens over arbitrary values.

Recommended token categories:

- Background
- Surface
- Surface elevated
- Foreground
- Muted foreground
- Border
- Primary
- Primary foreground
- Secondary
- Success
- Warning
- Destructive
- Focus ring
- Radius
- Shadow
- Spacing
- Typography

Semantic naming is preferred over names such as `blue-500` when the value represents a product role.

## 3. Layout System

Use a predictable layout grid.

Recommended principles:

- Use a consistent content container.
- Align major sections to the same grid.
- Use predictable horizontal gutters.
- Avoid arbitrary widths that break at intermediate sizes.
- Keep reading content at comfortable line lengths.
- Use full-width sections intentionally.
- Let visual hierarchy determine vertical rhythm.

Typical container strategy:

- Mobile: fluid with comfortable edge padding
- Tablet: fluid with larger gutters
- Desktop: centered max-width container
- Wide desktop: preserve readable content width rather than stretching everything

## 4. Spacing

Use an 8px-based scale by default.

Suggested values:

`4, 8, 12, 16, 20, 24, 32, 40, 48, 64, 80, 96, 128`

Use smaller values for tightly related elements and larger values between conceptual sections.

Do not use spacing merely because a design tool makes it easy. Spacing should communicate relationships.

## 5. Surface Hierarchy

Create hierarchy through a restrained combination of:

- Background changes
- Borders
- Elevation
- Typography
- Spacing
- Accent color

Avoid placing heavy shadows on every card. A premium interface often uses subtle borders and tonal separation instead.

## 6. Border Radius

Use a limited radius vocabulary.

Example roles:

- Small: controls, badges, compact elements
- Medium: inputs, buttons, cards
- Large: major panels and feature surfaces
- Pill: status chips and intentionally pill-shaped controls

Do not round every element excessively. Radius should reinforce component hierarchy.

## 7. Shadows

Use shadows sparingly.

Preferred hierarchy:

- No shadow for flat surfaces
- Very subtle shadow for raised cards
- Medium shadow for menus and popovers
- Stronger shadow only for dialogs or floating surfaces

Avoid dramatic shadows that make enterprise UI look inexpensive.

## 8. Color Roles

Define colors by purpose.

Primary accent should be used for:

- Primary actions
- Selected navigation
- Important links
- Key highlights

Success should communicate completed or healthy states.

Warning should communicate attention without implying failure.

Destructive should communicate irreversible or dangerous actions.

Muted colors should reduce emphasis, not reduce readability below accessible contrast.

## 9. Component States

Interactive components should account for:

- Default
- Hover
- Focus-visible
- Active
- Selected
- Disabled
- Loading
- Success
- Error
- Empty

Do not rely only on color to communicate state.

## 10. Buttons

Button hierarchy should be obvious.

Typical hierarchy:

1. Primary action
2. Secondary action
3. Tertiary/ghost action
4. Destructive action

Keep labels concise and action-oriented.

Buttons need visible keyboard focus and should provide clear disabled/loading feedback.

## 11. Forms

Forms should use consistent:

- Label placement
- Input height
- Border treatment
- Focus ring
- Error messaging
- Helper text
- Required-field treatment
- Button placement

Avoid unnecessary fields. Group related information and make validation understandable.

## 12. Navigation

Navigation should communicate where the user is and what they can do.

For dashboards:

- Keep primary navigation stable.
- Highlight the current location clearly.
- Group related destinations.
- Avoid excessive nesting.
- Preserve important actions where users expect them.

## 13. Cards

Cards should have a purpose.

A card should group information or actions that belong together. Do not turn every piece of content into a card.

Premium cards usually rely on:

- Strong internal hierarchy
- Consistent padding
- Subtle border or surface contrast
- Clear title and supporting content
- Purposeful actions

## 14. Tables

Tables should optimize scanning.

- Align numeric values consistently.
- Keep headers visually distinct.
- Use adequate row height.
- Avoid excessive borders.
- Make row actions predictable.
- Keep important columns visible on smaller screens.
- Use pagination or virtualization for large data sets.

## 15. Empty States

An empty state should explain:

1. What is empty.
2. Why it matters.
3. What the user can do next.

Use a clear action when one exists. Avoid decorative illustrations that do not help the user proceed.

## 16. Loading States

Prefer skeletons when the structure is known and stable.

Use spinners for short, localized operations.

Avoid blocking the entire application for small requests.

Loading states should prevent layout shifts where practical.

## 17. Error States

Errors should be:

- Clear
- Specific
- Actionable
- Calmly presented

Explain what happened and what the user can do next. Preserve user input when possible.

## 18. Responsive Design

Design mobile behavior intentionally rather than simply shrinking desktop layouts.

At each breakpoint evaluate:

- Navigation
- Content order
- Grid columns
- Table behavior
- Form layout
- Button placement
- Typography
- Spacing
- Touch target size

## 19. Accessibility Integration

Accessibility belongs inside the design system, not as a final patch.

Every interactive component should have:

- Keyboard behavior
- Visible focus
- Accessible name
- Appropriate semantic element
- Adequate contrast
- Clear state communication

## 20. Premium Quality Test

Before considering a component complete, ask:

- Is this visually premium?
- Is the hierarchy immediately understandable?
- Can spacing be improved?
- Can typography be improved?
- Is the component reusable?
- Are all states handled?
- Is the component accessible?
- Does it work responsively?
- Does it feel consistent with the rest of the product?
- Is this something I'd be proud to ship?
