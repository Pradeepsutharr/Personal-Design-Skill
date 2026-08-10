# Performance Standards

## Purpose

Performance is a product requirement. The skill must produce interfaces that feel fast, respond quickly, minimize unnecessary work, and are built with strong Core Web Vitals and Lighthouse performance in mind.

## Performance Target

Aim for excellent production performance rather than merely avoiding obvious mistakes.

Recommended goals:

- Lighthouse Performance: 95+ where practical
- Fast initial render
- Stable layout
- Low unnecessary JavaScript
- Responsive interaction
- Efficient rendering
- Good Core Web Vitals

Scores are targets, not guarantees. Always measure real applications with realistic data and devices.

## Core Web Vitals

Consider:

- LCP: Largest Contentful Paint
- INP: Interaction to Next Paint
- CLS: Cumulative Layout Shift

Design and implementation decisions should support fast content rendering, responsive interactions, and visual stability.

## Server vs Client

For Next.js applications:

- Prefer Server Components by default.
- Add `use client` only when browser APIs, local interaction state, effects, or client-only libraries are actually required.
- Keep client boundaries as small as practical.
- Avoid turning entire pages into Client Components unnecessarily.

Every client boundary should have a reason.

## JavaScript Budget

Minimize client-side JavaScript.

Avoid:

- Large libraries for simple tasks
- Duplicate dependencies
- Unnecessary polyfills
- Shipping data that is never used
- Hydrating static content unnecessarily
- Client-side computations that can happen on the server

Choose the simplest implementation that satisfies the requirement.

## Code Splitting

Use code splitting for heavy or rarely used functionality.

Consider dynamic imports for:

- Rich editors
- Large charting libraries
- PDF viewers
- Maps
- Complex visualization libraries
- Advanced admin tools
- Heavy modal content

Do not dynamically import tiny components without a measurable or meaningful reason.

## Images

Optimize every image.

- Use framework image optimization where available.
- Provide appropriate dimensions.
- Use responsive image sizing.
- Avoid shipping oversized assets.
- Prefer modern formats when supported.
- Lazy-load below-the-fold images where appropriate.
- Prioritize important above-the-fold imagery correctly.

Avoid layout shifts by reserving image space.

## Fonts

Fonts can significantly affect performance.

- Minimize font families.
- Load only required weights.
- Prefer framework-supported font optimization.
- Avoid unnecessary external font requests.
- Use appropriate display behavior.

Typography must remain beautiful without creating a poor loading experience.

## Rendering

Reduce unnecessary rendering work.

- Keep state close to where it is used.
- Avoid broad context updates for frequently changing state.
- Avoid unnecessary derived state.
- Memoize expensive calculations only when useful.
- Avoid premature memoization of trivial components.

## React Performance

Use:

- Stable keys
- Proper component boundaries
- Lazy loading where justified
- Memoization where it prevents meaningful repeated work
- Virtualization for large collections

Avoid:

- State updates on every keystroke when not required
- Large objects recreated unnecessarily
- Expensive calculations during every render
- Rendering thousands of DOM nodes unnecessarily

## Lists and Tables

For large datasets:

- Paginate when appropriate.
- Virtualize very large lists.
- Avoid rendering hidden rows.
- Avoid expensive formatting in every render.
- Debounce search where appropriate.
- Use server-side filtering for very large datasets when appropriate.

Do not sacrifice usability just to reduce DOM nodes.

## Data Fetching

Fetch only what the UI needs.

- Avoid duplicate requests.
- Cache appropriate data.
- Parallelize independent requests.
- Avoid request waterfalls.
- Stream or progressively render where appropriate.
- Keep loading states localized.

For interactive applications, use an established data-fetching strategy rather than creating ad-hoc request logic throughout components.

## Bundle Optimization

Before adding a dependency, ask:

- Is it necessary?
- Is there a native browser API?
- Is there already a dependency in the project that solves this?
- How large is it?
- Does it force client-side rendering?

Prefer focused imports where the package supports them.

## CSS Performance

Prefer efficient CSS.

- Avoid unnecessarily complex selectors.
- Avoid excessive runtime style generation.
- Prefer transform and opacity for animation.
- Avoid expensive filters over large surfaces.
- Keep repeated styles in reusable abstractions when appropriate.

## Animation Performance

Animations should normally use:

- `transform`
- `opacity`

Avoid animating layout properties continuously.

Respect reduced-motion preferences.

## Layout Stability

Prevent unexpected movement.

Reserve space for:

- Images
- Ads when applicable
- Async content
- Fonts when practical
- Dynamic UI blocks

Do not insert content above the user's current position unexpectedly.

## Loading Experience

A fast-feeling application communicates progress clearly.

Prefer:

- Skeletons for known content structures
- Localized loading indicators
- Optimistic UI where safe
- Progressive rendering
- Immediate feedback for user actions

Avoid blocking the entire application because one secondary request is pending.

## Error Performance

Failed requests should not cause the whole page to become unusable when only one section failed.

Use localized error boundaries or fallbacks where appropriate.

## Lighthouse Review

Before shipping, review:

### Performance

- Is JavaScript minimized?
- Are images optimized?
- Are fonts optimized?
- Are client components necessary?
- Are heavy dependencies lazy-loaded?
- Are rendering costs reasonable?
- Are there request waterfalls?
- Is layout stable?
- Are animations efficient?

### Accessibility

- Is semantic HTML used?
- Are labels and focus states present?
- Is contrast sufficient?

### Best Practices

- Are browser errors avoided?
- Are resources loaded securely?
- Are deprecated patterns avoided?

### SEO

- Is content crawlable?
- Is metadata present?
- Is the heading structure logical?

## Performance Anti-Patterns

Avoid:

- Making everything a Client Component
- Loading entire libraries for one small function
- Huge hero images without optimization
- Rendering large datasets without virtualization or pagination
- Excessive animation libraries for simple transitions
- Repeated API requests from multiple components
- Unnecessary global state
- Giant component files that rerender unrelated UI
- Blocking rendering on non-critical data

## Measurement

Do not claim a specific Lighthouse score without measuring it.

Use the standards in this file as implementation targets. When actual tooling is available, measure performance on realistic devices, network conditions, content, and production builds.

## Final Performance Gate

Before considering implementation complete, ask:

- Is the code optimized?
- Is the client JavaScript minimal?
- Are Server Components used where appropriate?
- Are images and fonts optimized?
- Are heavy components lazy-loaded where useful?
- Are large lists handled efficiently?
- Are interactions responsive?
- Is layout stable?
- Are animations performant?
- Is the implementation likely to achieve excellent Lighthouse and Core Web Vitals results?
- Have performance claims been measured rather than assumed?
