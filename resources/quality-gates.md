# UI Quality Gates

## Purpose

Every implementation must pass a deliberate quality review before it is considered complete.

The goal is not simply to make the code work. The goal is to produce an interface that is visually premium, usable, accessible, SEO-friendly, performant, reusable, and maintainable.

## Gate 1 — Visual Quality

Ask:

- Is this visually premium?
- Does the interface feel intentional rather than generic?
- Is the visual hierarchy obvious?
- Is the primary action clear?
- Are colors restrained and consistent?
- Are borders, radii, shadows, and surfaces consistent?
- Are decorative effects purposeful?

Fix visual issues before considering the task complete.

## Gate 2 — Spacing

Ask:

- Can spacing be improved?
- Are related elements grouped correctly?
- Are major sections sufficiently separated?
- Are page gutters aligned?
- Is card padding balanced?
- Is mobile spacing comfortable?
- Are arbitrary spacing values introducing inconsistency?

## Gate 3 — Typography

Ask:

- Can typography be improved?
- Is the heading hierarchy clear?
- Are font sizes appropriate for the viewport?
- Are weights used intentionally?
- Are line lengths readable?
- Are labels and metadata appropriately subordinate?
- Does typography feel premium rather than oversized?

## Gate 4 — Consistency

Ask:

- Is the UI consistent with the existing design system?
- Are the same patterns implemented the same way?
- Are colors semantic?
- Are spacing and radius tokens reused?
- Are component states consistent?
- Is terminology consistent?

Do not create one-off visual patterns when an existing system already solves the problem.

## Gate 5 — Component Quality

Ask:

- Is the component reusable?
- Does it have one clear responsibility?
- Is its API understandable?
- Are variants meaningful?
- Are important states covered?
- Does it reduce duplication?
- Is abstraction justified?

Avoid both extremes:

- Giant monolithic components
- Excessive micro-components with no meaningful responsibility

## Gate 6 — Code Quality

Ask:

- Is the code readable?
- Is the implementation appropriately simple?
- Are names descriptive?
- Is business logic separated where appropriate?
- Are unnecessary effects avoided?
- Is state scoped correctly?
- Are duplicate patterns extracted when appropriate?
- Does the implementation follow existing project conventions?

Do not perform unrelated refactors during focused tasks.

## Gate 7 — Performance

Ask:

- Is the code optimized?
- Is unnecessary client-side JavaScript avoided?
- Are Server Components used where appropriate?
- Are images optimized?
- Are fonts optimized?
- Are heavy libraries lazy-loaded where useful?
- Are large lists handled efficiently?
- Are requests duplicated or unnecessarily sequential?
- Are animations performant?
- Is layout stable?

Aim for excellent Lighthouse and Core Web Vitals results, but never claim a score without measurement.

## Gate 8 — SEO

For public/indexable pages, ask:

- Is the page SEO-friendly?
- Is the title unique and useful?
- Is the meta description present and meaningful?
- Is heading hierarchy logical?
- Is important content crawlable?
- Are internal links useful?
- Are images optimized and described appropriately?
- Is canonical handling correct?
- Is structured data appropriate?
- Is the URL clean and stable?

## Gate 9 — Accessibility

Ask:

- Is accessibility handled?
- Can the interface be used by keyboard?
- Are focus states visible?
- Are semantic HTML elements used?
- Are forms correctly labeled?
- Are icon-only controls named?
- Is color ever the only state indicator?
- Is contrast sufficient?
- Are dialogs and menus accessible?
- Is reduced motion respected?
- Are touch targets comfortable?

## Gate 10 — Responsive Quality

Check at minimum:

- Mobile
- Tablet
- Desktop
- Wide desktop where relevant

Ask:

- Does hierarchy remain clear?
- Does navigation work?
- Do forms remain usable?
- Are tables handled intentionally?
- Is there accidental horizontal overflow?
- Are images sized correctly?
- Does spacing adapt?
- Does typography adapt?

## Gate 11 — Real-Data Resilience

Do not validate only with ideal mock content.

Test mentally or actually with:

- Long names
- Long titles
- Empty values
- Missing images
- Large numbers
- Long descriptions
- Error states
- Loading states
- Large datasets
- Very small datasets

The UI should not fall apart when content becomes realistic.

## Gate 12 — Interaction Quality

Verify:

- Hover
- Focus
- Active
- Selected
- Disabled
- Loading
- Success
- Error
- Empty

Every interactive action should provide appropriate feedback.

## Gate 13 — Production Safety

Before shipping, check:

- No secrets exposed to the client
- No debug logging left unnecessarily
- No broken links
- No missing assets
- No obvious console errors
- No invalid HTML patterns
- No unnecessary dependencies
- No accidental destructive changes

## Gate 14 — Ship Test

Ask the final questions:

- Is this visually premium?
- Can spacing be improved?
- Can typography be improved?
- Is the UI consistent?
- Is the component reusable?
- Is the code optimized?
- Will Lighthouse score well?
- Is the page SEO-friendly?
- Is accessibility handled?
- Does it work on mobile?
- Does it handle real data?
- Is the interaction polished?
- Is the implementation maintainable?
- Is this something I'd be proud to ship?

If any answer is clearly `no`, improve the implementation before declaring the task complete.

## Definition of Done

A UI task is complete only when:

1. The requested functionality works.
2. The visual design is polished.
3. The design system is followed.
4. Components are appropriately reusable.
5. Responsive behavior is intentional.
6. Accessibility is handled.
7. Performance has been considered.
8. SEO has been handled for public pages.
9. Loading, empty, error, and interaction states are covered where relevant.
10. The code is clean and maintainable.
11. No unnecessary unrelated changes were introduced.
12. The result passes the final ship test.
