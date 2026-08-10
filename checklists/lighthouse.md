# Lighthouse Checklist

Use this checklist to prepare a frontend implementation for Lighthouse and real-world performance testing.

## Performance

- [ ] Production build is used for measurement.
- [ ] Initial JavaScript is minimized.
- [ ] Unnecessary Client Components are removed.
- [ ] Heavy dependencies are avoided or lazy-loaded.
- [ ] Images are optimized and correctly sized.
- [ ] Hero/LCP image is intentionally prioritized when appropriate.
- [ ] Below-the-fold images are lazy-loaded where appropriate.
- [ ] Fonts are optimized and unnecessary weights are removed.
- [ ] Third-party scripts are minimized.
- [ ] Request waterfalls are avoided where practical.
- [ ] Large datasets are paginated or virtualized where appropriate.
- [ ] Expensive rendering work is controlled.
- [ ] Animations use performant properties.
- [ ] Layout shifts are minimized.

## Core Web Vitals

### LCP

- [ ] Largest content is identified.
- [ ] Critical content is server-rendered where appropriate.
- [ ] Hero imagery is optimized.
- [ ] Critical fonts/resources are not unnecessarily delayed.
- [ ] No heavy client-side initialization blocks the main content.

### INP

- [ ] Click handlers are lightweight.
- [ ] Expensive synchronous work is avoided during interactions.
- [ ] Large state updates are localized.
- [ ] Heavy UI is not unnecessarily rendered after small interactions.
- [ ] Long JavaScript tasks are minimized.

### CLS

- [ ] Images have reserved dimensions/aspect ratios.
- [ ] Async content does not unexpectedly push existing content.
- [ ] Fonts do not create obvious layout instability.
- [ ] Dynamic banners and notices reserve appropriate space.
- [ ] Animations do not cause unexpected layout shifts.

## Accessibility

- [ ] Semantic HTML is used.
- [ ] Heading hierarchy is logical.
- [ ] Interactive elements have accessible names.
- [ ] Keyboard navigation works.
- [ ] Focus indicators are visible.
- [ ] Color contrast is sufficient.
- [ ] Color is not the only state indicator.
- [ ] Form controls are labeled.
- [ ] Images have appropriate alt text.
- [ ] Reduced motion is respected.

## Best Practices

- [ ] No obvious console errors.
- [ ] No broken resource requests.
- [ ] No insecure resource loading.
- [ ] No unnecessary deprecated APIs.
- [ ] Production environment behavior is tested.
- [ ] Browser compatibility is considered.

## SEO

- [ ] Title is unique and meaningful.
- [ ] Meta description is present where appropriate.
- [ ] Search-engine-relevant content is crawlable.
- [ ] Heading hierarchy is logical.
- [ ] Links have descriptive text.
- [ ] Images have meaningful alt text when informative.
- [ ] Canonical URL strategy is correct.
- [ ] Sitemap/robots configuration is appropriate for the project.

## Lighthouse Discipline

Do not optimize exclusively for a synthetic score.

Also consider:

- Real mobile devices
- Real network conditions
- Production data sizes
- Long user sessions
- Interaction responsiveness
- Accessibility
- User-perceived speed

A high Lighthouse score does not automatically mean a good product.

## Final Questions

- [ ] Is the code optimized?
- [ ] Will Lighthouse score well?
- [ ] Are Core Web Vitals likely to be healthy?
- [ ] Is the page accessible?
- [ ] Is the page SEO-friendly?
- [ ] Does the interface still feel visually premium after performance optimizations?
- [ ] Have actual measurements been taken before making performance claims?
