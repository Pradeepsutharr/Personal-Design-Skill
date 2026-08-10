# Frontend Review Checklist

Use this checklist before considering a frontend implementation production-ready.

## Architecture

- [ ] Existing project architecture was understood before changes.
- [ ] No unnecessary framework or library rewrites were introduced.
- [ ] Server/client boundaries are intentional.
- [ ] Client components are limited to areas that actually need them.
- [ ] Shared logic is placed in appropriate reusable modules.
- [ ] No unnecessary global state was introduced.

## React

- [ ] Components have clear responsibilities.
- [ ] State is scoped appropriately.
- [ ] Derived state is not unnecessarily stored.
- [ ] Effects are used only for external synchronization.
- [ ] List keys are stable.
- [ ] Expensive calculations are controlled where necessary.
- [ ] Reusable patterns are abstracted appropriately.
- [ ] No giant monolithic component was created.

## Next.js

- [ ] App Router conventions are followed where applicable.
- [ ] Server Components are used by default.
- [ ] Dynamic imports are used for genuinely heavy or rarely needed code.
- [ ] Metadata is implemented through Next.js mechanisms.
- [ ] Images use appropriate optimization.
- [ ] Fonts are optimized.
- [ ] Loading and error states are handled.
- [ ] Server-only secrets remain on the server.

## Styling

- [ ] Existing design tokens are reused.
- [ ] Tailwind classes follow project conventions.
- [ ] Arbitrary values are limited to justified one-off cases.
- [ ] Responsive breakpoints are intentional.
- [ ] Focus, hover, active, disabled, and selected states are designed.
- [ ] Dark mode is consistent if supported.
- [ ] No unnecessary global CSS overrides were introduced.

## Performance

- [ ] Is the code optimized?
- [ ] Client JavaScript is minimized.
- [ ] Heavy dependencies are not loaded unnecessarily.
- [ ] Large lists use pagination or virtualization where appropriate.
- [ ] Images are correctly sized and optimized.
- [ ] Below-the-fold media is lazy-loaded where appropriate.
- [ ] Animations use performant properties.
- [ ] Layout shifts are minimized.
- [ ] Request waterfalls are avoided where practical.
- [ ] No obvious unnecessary rerender loops exist.

## Accessibility

- [ ] Semantic HTML is used.
- [ ] All interactive elements are keyboard accessible.
- [ ] Focus-visible states are present.
- [ ] Forms have accessible labels.
- [ ] Icon-only controls have accessible names.
- [ ] Dialogs, menus, and popovers have appropriate focus behavior.
- [ ] Color is not the only way to communicate state.
- [ ] Contrast is sufficient.
- [ ] Reduced motion is respected.

## SEO

For public pages:

- [ ] Unique title metadata exists.
- [ ] Meta description exists.
- [ ] Heading hierarchy is logical.
- [ ] Important content is crawlable.
- [ ] Internal links use descriptive anchor text.
- [ ] Images have appropriate alt text.
- [ ] Canonical handling is correct where relevant.
- [ ] Open Graph metadata is considered.
- [ ] Structured data is used only when appropriate and accurate.

## UX States

- [ ] Loading state
- [ ] Empty state
- [ ] Error state
- [ ] Success state
- [ ] Disabled state
- [ ] Validation state
- [ ] Long-content state
- [ ] Large-data state

## Responsive QA

- [ ] Mobile reviewed.
- [ ] Tablet reviewed.
- [ ] Desktop reviewed.
- [ ] Wide desktop reviewed where relevant.
- [ ] No accidental horizontal scrolling.
- [ ] Touch targets are comfortable.
- [ ] Navigation remains usable.
- [ ] Forms remain usable.
- [ ] Tables use an intentional responsive strategy.

## Code Quality

- [ ] Naming is descriptive.
- [ ] Functions are appropriately small and focused.
- [ ] Duplicate logic is avoided.
- [ ] Comments explain why, not obvious what.
- [ ] No dead code remains.
- [ ] No unnecessary dependencies were added.
- [ ] No debug code remains.
- [ ] No unrelated files were changed.

## Visual Quality

- [ ] Is this visually premium?
- [ ] Can spacing be improved?
- [ ] Can typography be improved?
- [ ] Is the UI consistent?
- [ ] Are visual effects restrained and purposeful?
- [ ] Does the implementation match the intended design?
- [ ] Does the result feel polished at every breakpoint?

## Final Ship Gate

- [ ] Is the component reusable?
- [ ] Is the code optimized?
- [ ] Will Lighthouse score well?
- [ ] Is the page SEO-friendly?
- [ ] Is accessibility handled?
- [ ] Does it work with realistic data?
- [ ] Are production errors absent?
- [ ] Is this something I'd be proud to ship?
