# Ship-Ready Checklist

Use this as the final gate before shipping a UI or frontend feature.

## Functionality

- [ ] Requested functionality works end-to-end.
- [ ] Primary user flow works.
- [ ] Important edge cases are handled.
- [ ] Loading state works.
- [ ] Empty state works.
- [ ] Error state works.
- [ ] Success state works.
- [ ] Disabled state works where relevant.

## Visual Quality

- [ ] Is this visually premium?
- [ ] Can spacing be improved?
- [ ] Can typography be improved?
- [ ] Is the visual hierarchy clear?
- [ ] Is the UI consistent with the design system?
- [ ] Are colors, borders, radii, shadows, and surfaces consistent?
- [ ] Are animations and visual effects purposeful?
- [ ] Does the result feel polished rather than generic?

## Components

- [ ] Is the component reusable?
- [ ] Does each component have a clear responsibility?
- [ ] Are variants meaningful?
- [ ] Is the component API understandable?
- [ ] Is duplicate UI logic avoided?
- [ ] Is abstraction neither excessive nor insufficient?

## Code Quality

- [ ] Is the code optimized?
- [ ] Is naming clear?
- [ ] Is state scoped correctly?
- [ ] Are unnecessary effects avoided?
- [ ] Are unnecessary dependencies avoided?
- [ ] Are existing project conventions followed?
- [ ] Is unrelated refactoring avoided?
- [ ] Are debug logs and temporary code removed?

## Performance

- [ ] Client JavaScript is minimized.
- [ ] Server/client boundaries are intentional.
- [ ] Images are optimized.
- [ ] Fonts are optimized.
- [ ] Heavy libraries are lazy-loaded where useful.
- [ ] Large lists/tables are handled efficiently.
- [ ] Requests are not unnecessarily duplicated.
- [ ] Animations are performant.
- [ ] Layout shifts are minimized.
- [ ] Lighthouse performance has been considered.

## SEO

For public/indexable pages:

- [ ] Is the page SEO-friendly?
- [ ] Unique title metadata
- [ ] Useful meta description
- [ ] Logical heading hierarchy
- [ ] Crawlable important content
- [ ] Descriptive internal links
- [ ] Appropriate image alt text
- [ ] Canonical strategy checked
- [ ] Open Graph metadata considered
- [ ] Structured data considered where appropriate

## Accessibility

- [ ] Is accessibility handled?
- [ ] Semantic HTML is used.
- [ ] Keyboard navigation works.
- [ ] Focus-visible states are clear.
- [ ] Forms are properly labeled.
- [ ] Icon-only controls have accessible names.
- [ ] Dialogs/menus/popovers are accessible.
- [ ] Contrast is sufficient.
- [ ] Color is not the only state indicator.
- [ ] Reduced motion is respected.
- [ ] Touch targets are comfortable.

## Responsive QA

- [ ] Mobile reviewed.
- [ ] Tablet reviewed.
- [ ] Desktop reviewed.
- [ ] Wide desktop reviewed where relevant.
- [ ] No accidental horizontal overflow.
- [ ] Typography adapts correctly.
- [ ] Spacing adapts correctly.
- [ ] Navigation remains usable.
- [ ] Forms remain usable.
- [ ] Tables have an intentional responsive strategy.

## Real-World Data

Test or reason through:

- [ ] Long names
- [ ] Long titles
- [ ] Long descriptions
- [ ] Missing images
- [ ] Empty values
- [ ] Large numbers
- [ ] Large datasets
- [ ] Zero-data state
- [ ] API failure
- [ ] Slow network

## Browser/Production QA

- [ ] Production build succeeds.
- [ ] No obvious console errors.
- [ ] No broken links.
- [ ] No missing assets.
- [ ] No exposed secrets.
- [ ] No accidental environment-specific URLs.
- [ ] No unnecessary network requests.
- [ ] No obvious hydration issues.

## Final Ship Questions

- [ ] Is this visually premium?
- [ ] Can spacing be improved?
- [ ] Can typography be improved?
- [ ] Is the UI consistent?
- [ ] Is the component reusable?
- [ ] Is the code optimized?
- [ ] Will Lighthouse score well?
- [ ] Is the page SEO-friendly?
- [ ] Is accessibility handled?
- [ ] Does it work beautifully on mobile?
- [ ] Does it handle realistic data?
- [ ] Does it feel fast?
- [ ] Is this something I'd be proud to ship?

## Definition of Ship-Ready

Do not mark a task complete merely because it functions.

It is ship-ready when functionality, visual quality, usability, accessibility, SEO, performance, responsiveness, code quality, and maintainability have all been considered and the implementation has no obvious high-impact issues.
