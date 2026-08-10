# Landing Page Example

Use this example when designing or reviewing a premium SaaS, product, or service landing page.

## Recommended Structure

```text
Header
  ├─ Logo
  ├─ Navigation
  └─ Primary CTA

Hero
  ├─ Eyebrow (optional)
  ├─ Outcome-focused headline
  ├─ Supporting value proposition
  ├─ Primary CTA
  ├─ Secondary CTA (optional)
  └─ Product visual / proof

Trust
  ├─ Customer logos
  ├─ Metrics
  └─ Credibility indicators

Problem / Opportunity
  └─ Explain the user's pain clearly

Product / Solution
  ├─ Product visual
  ├─ Capability
  └─ Outcome

Key Benefits
  ├─ Benefit 1
  ├─ Benefit 2
  └─ Benefit 3

Workflow / How It Works
  ├─ Step 1
  ├─ Step 2
  └─ Step 3

Proof
  ├─ Testimonial
  ├─ Case study
  └─ Metrics

Integrations / Ecosystem (optional)

Pricing (optional)

FAQ

Final CTA

Footer
```

## Hero Example

### Goal

Communicate value within seconds without overwhelming the visitor.

### Recommended hierarchy

```text
Small eyebrow
Strong outcome-focused headline
Short supporting paragraph
Primary CTA + optional secondary CTA
Product visualization
Trust signal
```

Example copy pattern:

```text
MANAGE YOUR OPERATIONS WITH CONFIDENCE

One platform for your team's most important workflows.

Bring data, automation, and collaboration together so your team can move faster with less operational overhead.

[Start free] [Book a demo]
```

The exact copy should be adapted to the actual product and audience.

## Visual Direction

A premium SaaS landing page can use:

- Strong display typography
- Generous but controlled whitespace
- Dark or light surfaces depending on brand
- Subtle gradients
- Product UI mockups
- Fine borders
- Layered surfaces
- Restrained glow
- High-quality micro-interactions

Do not stack every effect together.

## Product Visual

Prefer authentic product UI over generic decoration.

Show realistic examples such as:

- Dashboard data
- Tables
- Workflow states
- Maps
- Reports
- Analytics
- User actions

Make the visual legible at the actual rendered size.

## Responsive Strategy

### Mobile

- Simplify navigation.
- Stack hero content intentionally.
- Keep the main CTA easy to tap.
- Reduce decorative effects.
- Optimize product screenshots.
- Preserve typography hierarchy.

### Desktop

- Use a readable maximum content width.
- Give the hero visual enough breathing room.
- Avoid unnecessarily wide text blocks.
- Use grid composition intentionally.

## Performance Strategy

- Server-render static content where appropriate.
- Keep interactive client components isolated.
- Optimize hero imagery.
- Lazy-load below-the-fold media.
- Avoid heavy animation libraries for simple effects.
- Avoid shipping large JavaScript bundles for decorative visuals.

## SEO Strategy

Ensure:

- Unique title
- Useful meta description
- One clear primary heading
- Logical section headings
- Crawlable page content
- Descriptive internal links
- Appropriate Open Graph metadata
- Optimized image alt text
- Canonical URL strategy
- Structured data only when accurate and useful

## Accessibility Strategy

Ensure:

- Semantic landmarks
- Logical heading hierarchy
- Keyboard-accessible navigation
- Visible focus states
- Accessible CTA names
- Sufficient contrast
- Meaningful alt text
- Reduced-motion support

## Review Questions

Before shipping, ask:

- Is the value proposition obvious within seconds?
- Is the hero visually premium?
- Is the primary CTA obvious?
- Does the product visual explain something useful?
- Is spacing balanced?
- Can typography be improved?
- Are sections visually varied without becoming inconsistent?
- Is the UI consistent?
- Is the page SEO-friendly?
- Is accessibility handled?
- Will Lighthouse score well?
- Is the code optimized and reusable?
- Is this something I'd be proud to ship?
