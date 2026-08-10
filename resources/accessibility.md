# Accessibility Standards

## Purpose

Accessibility is a core product-quality requirement. Every interface should be usable by people with different abilities, input methods, screen sizes, and assistive technologies.

Target WCAG 2.2 AA principles where applicable.

## Core Principle

Use semantic HTML first. Add ARIA only when native HTML cannot express the required meaning or behavior.

Accessibility must be designed into components from the beginning, not added after the visual implementation is complete.

## Semantic HTML

Prefer the correct element for the job:

- `button` for actions
- `a` for navigation
- `input` for text input
- `label` for form labels
- `nav` for navigation
- `main` for primary content
- `header` and `footer` for page regions
- `section` and `article` when they communicate structure
- Proper heading elements for hierarchy

Do not use clickable `div` elements when a native interactive element exists.

## Keyboard Navigation

Every interactive feature must be usable without a mouse.

Verify:

- Tab order is logical.
- Interactive controls can receive focus.
- Enter/Space activates appropriate controls.
- Escape closes dismissible overlays where expected.
- Arrow keys are used only when the interaction pattern calls for them.
- Focus is not trapped unexpectedly.

## Focus States

Every keyboard-focusable element should have a visible focus indicator.

Do not remove browser focus styles without replacing them with an equally visible or better indicator.

Use `:focus-visible` where appropriate so keyboard users receive strong feedback without creating unnecessary visual noise for pointer users.

## Color Contrast

Do not rely on subtle gray-on-gray styling merely for aesthetics.

Verify contrast for:

- Body text
- Headings
- Labels
- Buttons
- Links
- Form controls
- Placeholder or supporting text where it conveys information
- Icons that communicate meaning

Large text and UI components have different contrast considerations; evaluate each according to its role.

## Do Not Use Color Alone

Never communicate an important state using color alone.

For example, an error should combine:

- Color
- Text
- Icon or other visual cue when appropriate

The same principle applies to success, warning, selected, and required states.

## Forms

Every form control needs an accessible name.

Use:

- Visible labels
- Proper `for`/`id` relationships
- Helpful descriptions when needed
- Programmatically associated errors

Do not use placeholder text as the only label.

Errors should identify:

1. Which field has a problem.
2. What is wrong.
3. How to fix it.

Preserve entered values when possible.

## Buttons and Links

Button labels should describe the action.

Prefer:

- `Save changes`
- `Delete account`
- `View booking`

Avoid ambiguous labels such as:

- `Click here`
- `Submit`
- `More`

unless the surrounding context makes the action unambiguous.

Links should navigate. Buttons should perform actions.

## Images

Provide meaningful alternative text for informative images.

Decorative images should use empty alt text or an equivalent mechanism so screen readers do not announce irrelevant content.

Do not repeat nearby text in alt text unnecessarily.

## Icons

Icons used alone must have an accessible name when they are interactive or communicate meaning.

For icon-only buttons:

- Provide an accessible label.
- Provide a visible tooltip when useful.
- Ensure the hit target is large enough.

Do not assume users understand an icon without context.

## Modals and Dialogs

Dialogs should:

- Have an accessible name.
- Move focus into the dialog appropriately.
- Keep focus contained while open when required by the interaction pattern.
- Return focus to the triggering element when closed where practical.
- Close predictably.

Do not make dialogs impossible to escape with a keyboard.

## Navigation

Navigation should have clear structure and current-location indication.

For complex applications:

- Group related destinations.
- Provide clear active state.
- Avoid excessive nested navigation.
- Keep important destinations discoverable.

## Tables

Tables should have:

- Clear headers
- Logical reading order
- Sufficient contrast
- Accessible actions

Do not use tables for layout.

For complex data tables, consider appropriate header associations and responsive strategies.

## Dynamic Content

When content updates without a page navigation, make important changes understandable to assistive technologies.

Use appropriate live-region techniques carefully. Do not announce every minor UI change.

Examples where announcements may help:

- Save succeeded
- Important error occurred
- Search result count changed
- Background operation completed

## Loading States

Loading states should communicate progress without creating accessibility barriers.

Do not make a spinner the only indication of a long-running operation.

Where appropriate, provide text such as `Loading bookings` or `Saving changes`.

## Motion

Respect `prefers-reduced-motion`.

For users requesting reduced motion:

- Remove decorative movement.
- Reduce transition distance.
- Avoid unnecessary parallax.
- Keep state changes understandable.

## Touch Targets

Interactive controls should have comfortable touch targets on mobile devices.

Do not pack tiny icon buttons tightly together.

Spacing between controls is also important because it reduces accidental activation.

## Responsive Accessibility

Accessibility must remain intact across breakpoints.

Check:

- Text scaling
- Zoom behavior
- Keyboard navigation
- Touch targets
- Reflow
- Horizontal scrolling
- Form usability
- Navigation access

Do not hide important functionality solely because the viewport is small.

## Content Accessibility

Use clear language.

- Avoid unnecessary jargon.
- Use descriptive headings.
- Break dense content into scannable sections.
- Explain unfamiliar terms when needed.
- Keep error messages actionable.

## Accessibility Review

Before shipping, ask:

- Is accessibility handled from the component design stage?
- Can the entire interface be operated by keyboard?
- Are focus states visible?
- Are semantic elements used correctly?
- Are forms properly labeled?
- Are errors understandable?
- Do icons have accessible names when needed?
- Is color ever the only state indicator?
- Is contrast sufficient?
- Does reduced motion work?
- Are touch targets comfortable?
- Can screen-reader users understand the page structure?
- Does accessibility remain intact on mobile and zoomed layouts?
