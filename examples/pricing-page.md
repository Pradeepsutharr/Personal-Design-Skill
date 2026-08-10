# Pricing Page Example

Use this example when designing or reviewing SaaS pricing experiences.

## Goal

Help users understand plans, compare value, choose confidently, and start the appropriate conversion flow.

## Recommended Structure

```text
Header

Pricing Hero
  ├─ Clear headline
  ├─ Short value statement
  └─ Billing toggle if applicable

Pricing Cards
  ├─ Plan name
  ├─ Price
  ├─ Billing context
  ├─ Short description
  ├─ Primary CTA
  └─ Included features

Comparison / Feature Details

Trust / Security / Customer Proof

FAQ

Final CTA

Footer
```

## Pricing Hero

Keep the message simple.

Example:

```text
Plans that scale with your team

Choose the capabilities that fit your workflow. Upgrade when you need more.

[Monthly] [Yearly — Save 20%]
```

Avoid vague marketing language when users are actively trying to understand pricing.

## Pricing Cards

Each card should answer:

- What is this plan?
- Who is it for?
- How much does it cost?
- What do I get?
- What should I do next?

Recommended hierarchy:

```text
Plan name
Short description
Price + billing context
Primary CTA
Key features
Secondary details
```

## Recommended Plan

If one plan is genuinely recommended, make it visually distinct.

Use:

- Subtle border emphasis
- Small recommendation label
- Clear value explanation
- Appropriate CTA prominence

Do not make a plan visually dominant without explaining why it is recommended.

## Feature Comparison

For complex products, provide a comparison table below the primary pricing cards.

Prioritize:

- Features that meaningfully differentiate plans
- Limits users care about
- Integrations
- Support levels
- Security/compliance capabilities

Avoid dumping every backend capability into the comparison table.

## Pricing Clarity

Clearly communicate:

- Monthly vs yearly billing
- Currency
- Taxes where relevant
- Usage limits
- Seats/users where relevant
- Setup fees if any
- Trial details
- Cancellation terms where appropriate

Do not hide important pricing conditions.

## CTA Design

Use action-oriented labels:

- `Start free`
- `Start trial`
- `Choose Pro`
- `Contact sales`
- `Book a demo`

The CTA should match the actual next step.

Do not use `Get started` for every plan if the resulting workflows differ.

## Enterprise Plan

Enterprise plans often need a sales-assisted path.

Explain the value and use a clear action such as:

`Talk to sales`

Avoid pretending enterprise pricing is identical to self-serve plans when it is not.

## Billing Toggle

If monthly/yearly billing exists:

- Make the current selection obvious.
- Show savings accurately.
- Update all affected prices consistently.
- Ensure keyboard accessibility.
- Avoid misleading savings claims.

## Responsive Strategy

### Desktop

Use cards in a clear comparison layout.

### Mobile

Stack plans intentionally.

Consider:

- Sticky or easily accessible billing controls
- Clear plan headings
- Short feature lists
- Expandable feature details
- Avoiding extremely long comparison tables

Do not squeeze four pricing cards into a narrow mobile viewport.

## Visual Direction

Premium pricing pages should feel trustworthy and calm.

Use:

- Strong typography
- Clear pricing hierarchy
- Restrained accent colors
- Subtle borders
- Consistent card geometry
- Purposeful recommendation styling

Avoid:

- Excessive gradients
- Fake urgency
- Confetti-like decoration
- Too many badges
- Visually confusing price treatments

## Accessibility

Ensure:

- Plan names are semantic headings.
- Pricing is readable without color.
- Billing controls are keyboard accessible.
- Buttons have clear accessible names.
- Comparison tables have semantic headers.
- Focus states are visible.
- Contrast is sufficient.

## Performance

- Avoid unnecessary client-side state.
- Keep billing toggles lightweight.
- Optimize illustrations and background assets.
- Avoid large animation libraries for simple transitions.
- Server-render static pricing content where appropriate.

## SEO

For public pricing pages:

- Use a unique title.
- Provide a useful description.
- Use logical headings.
- Keep pricing content crawlable.
- Use structured data only when accurate and appropriate.
- Avoid hiding important pricing information behind client-only interactions.

## Review Questions

- Is pricing immediately understandable?
- Is the recommended plan obvious when appropriate?
- Can spacing be improved?
- Can typography be improved?
- Is the UI consistent?
- Are CTAs accurate and clear?
- Is the component reusable?
- Is the code optimized?
- Will Lighthouse score well?
- Is the page SEO-friendly?
- Is accessibility handled?
- Is the mobile comparison usable?
- Is the pricing experience trustworthy?
- Is this something I'd be proud to ship?
