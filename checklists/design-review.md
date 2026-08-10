# Design Review Checklist

Use this checklist after implementing or redesigning a UI.

## Visual

- [ ] Is this visually premium?
- [ ] Is the visual hierarchy immediately clear?
- [ ] Is the primary action obvious?
- [ ] Are colors consistent and restrained?
- [ ] Are borders, radii, and shadows consistent?
- [ ] Are visual effects purposeful rather than decorative noise?
- [ ] Does the page feel intentional rather than template-like?

## Spacing

- [ ] Can spacing be improved?
- [ ] Are related elements grouped correctly?
- [ ] Are section gaps intentional?
- [ ] Are page gutters aligned?
- [ ] Is card padding balanced?
- [ ] Is mobile spacing comfortable?

## Typography

- [ ] Can typography be improved?
- [ ] Is heading hierarchy clear?
- [ ] Are font sizes appropriate?
- [ ] Are weights used intentionally?
- [ ] Are line lengths readable?
- [ ] Are labels and metadata appropriately subordinate?

## Consistency

- [ ] Is the UI consistent with the existing design system?
- [ ] Are repeated patterns implemented consistently?
- [ ] Are semantic color tokens used?
- [ ] Are spacing and radius tokens reused?
- [ ] Is terminology consistent?

## Components

- [ ] Is the component reusable?
- [ ] Does it have a clear responsibility?
- [ ] Is the API understandable?
- [ ] Are variants meaningful?
- [ ] Are loading, empty, error, disabled, and success states covered where relevant?

## Responsive

- [ ] Mobile layout reviewed
- [ ] Tablet layout reviewed
- [ ] Desktop layout reviewed
- [ ] Wide desktop considered where relevant
- [ ] No accidental horizontal overflow
- [ ] Navigation works at all breakpoints
- [ ] Forms remain usable
- [ ] Tables have an intentional mobile strategy

## Accessibility

- [ ] Semantic HTML used
- [ ] Keyboard navigation works
- [ ] Focus states are visible
- [ ] Forms have proper labels
- [ ] Icon-only controls have accessible names
- [ ] Color is not the only state indicator
- [ ] Contrast is sufficient
- [ ] Reduced motion is respected
- [ ] Touch targets are comfortable

## Performance

- [ ] Is the code optimized?
- [ ] Client-side JavaScript is minimized
- [ ] Images are optimized
- [ ] Fonts are optimized
- [ ] Heavy components are lazy-loaded where useful
- [ ] Large lists/tables are handled efficiently
- [ ] Animations use efficient properties
- [ ] Layout shifts are minimized
- [ ] Request waterfalls are avoided where practical

## SEO

For public pages:

- [ ] Is the page SEO-friendly?
- [ ] Unique title
- [ ] Useful meta description
- [ ] Logical heading hierarchy
- [ ] Crawlable important content
- [ ] Useful internal links
- [ ] Optimized images and alt text
- [ ] Canonical strategy checked
- [ ] Structured data considered where appropriate

## Content

- [ ] Copy is clear
- [ ] CTAs are action-oriented
- [ ] Error messages are actionable
- [ ] Empty states explain what to do next
- [ ] Terminology is consistent
- [ ] No unnecessary jargon

## Final

- [ ] Realistic content tested
- [ ] Long content tested
- [ ] Empty state tested
- [ ] Loading state tested
- [ ] Error state tested
- [ ] No obvious console errors
- [ ] No broken links/assets
- [ ] No unnecessary unrelated refactors
- [ ] This is something I'd be proud to ship
