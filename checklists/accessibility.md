# Accessibility Checklist

Use this checklist for every UI implementation.

## Semantic Structure

- [ ] Semantic HTML is used.
- [ ] Heading levels reflect document structure.
- [ ] Landmarks are meaningful.
- [ ] Buttons are buttons.
- [ ] Links are links.
- [ ] Lists, tables, and forms use appropriate semantics.

## Keyboard

- [ ] All interactive controls are keyboard accessible.
- [ ] Focus order is logical.
- [ ] Focus-visible states are clearly visible.
- [ ] No keyboard trap exists.
- [ ] Menus and dialogs support expected keyboard behavior.

## Forms

- [ ] Every field has an accessible label.
- [ ] Required fields are communicated.
- [ ] Errors are associated with the correct fields.
- [ ] Error messages explain how to recover.
- [ ] Input purpose/types are appropriate.

## Interactive Controls

- [ ] Icon-only controls have accessible names.
- [ ] Buttons communicate disabled/loading states.
- [ ] Toggle/switch state is exposed semantically.
- [ ] Tooltips do not contain essential information exclusively.

## Color and Contrast

- [ ] Text contrast is sufficient.
- [ ] UI control contrast is sufficient.
- [ ] Color is not the only way to communicate state.
- [ ] Error/success/warning states include text, icons, or other cues.

## Images and Media

- [ ] Informative images have meaningful alt text.
- [ ] Decorative images have appropriate empty alt text.
- [ ] Complex visuals have an equivalent explanation when necessary.
- [ ] Autoplay media does not create accessibility problems.

## Motion

- [ ] `prefers-reduced-motion` is respected.
- [ ] Motion is not required to understand state.
- [ ] No problematic flashing animation exists.
- [ ] Transitions do not prevent interaction.

## Responsive Accessibility

- [ ] Text scaling does not break the layout.
- [ ] Zoom remains usable.
- [ ] Touch targets are comfortable.
- [ ] Mobile controls remain accessible.
- [ ] Responsive navigation preserves keyboard and screen-reader behavior.

## Dialogs and Overlays

- [ ] Dialogs have accessible names.
- [ ] Focus moves appropriately into dialogs.
- [ ] Focus returns appropriately after closing.
- [ ] Background content is appropriately inert when required.

## Tables

- [ ] Tables use semantic headers.
- [ ] Header relationships are meaningful.
- [ ] Sort controls are accessible.
- [ ] Row actions have clear names.

## Final Review

- [ ] Tested with keyboard.
- [ ] Tested with browser zoom/text scaling.
- [ ] Reviewed focus states.
- [ ] Reviewed contrast.
- [ ] Reviewed form errors.
- [ ] Reviewed reduced motion.
- [ ] Is accessibility handled without compromising visual quality?
- [ ] Is this something I'd be proud to ship?
