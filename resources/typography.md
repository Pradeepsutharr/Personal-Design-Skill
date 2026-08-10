# Typography Standards

## Purpose

Typography should establish hierarchy, improve readability, communicate brand character, and make every interface feel intentional.

## Core Rule

Never treat typography as an afterthought. Before finalizing a page, verify that headings, body text, labels, metadata, buttons, and helper text form a clear visual hierarchy.

## Type Scale

Use a predictable scale rather than arbitrary font sizes.

A practical product scale may include:

- Display: 48–72px
- H1: 40–56px
- H2: 32–40px
- H3: 24–32px
- H4: 20–24px
- Body large: 18px
- Body: 16px
- Body small: 14px
- Caption: 12–13px

Adjust responsively. Do not force large desktop typography onto small screens.

## Hierarchy

A user should be able to scan a page and understand:

1. What this page is about.
2. What matters most.
3. What supporting information means.
4. What action is available.

Use size, weight, color, spacing, and position together. Do not rely on font size alone.

## Font Selection

Choose fonts based on product character and readability.

For enterprise SaaS, prefer clean, highly legible sans-serif families. Display fonts may be used selectively for marketing experiences when they improve brand identity.

Do not introduce many font families. One family with a thoughtful weight system is usually stronger than several unrelated fonts.

## Font Weights

Use a limited weight vocabulary.

Recommended roles:

- Regular: body copy
- Medium: labels and supporting emphasis
- Semibold: headings and important controls
- Bold: major display headings when appropriate

Avoid using bold everywhere. Weight loses meaning when every element is emphasized.

## Line Height

Recommended starting points:

- Display headings: 0.95–1.1
- Section headings: 1.1–1.25
- Body text: 1.45–1.7
- Labels and controls: 1.2–1.4

Tune line height to the chosen font. Optical readability is more important than rigid numbers.

## Line Length

Long lines reduce readability.

For prose, target approximately 45–80 characters per line. Marketing copy can be slightly wider when visual composition requires it, but avoid full-width paragraphs.

## Letter Spacing

Use tracking carefully.

- Large display headings can use slightly tighter tracking.
- Uppercase labels often benefit from modest positive tracking.
- Body copy should normally use natural tracking.
- Avoid extreme letter spacing.

## Headings

Headings should communicate structure, not simply make text larger.

Use one clear page title. Descendant headings should follow a logical hierarchy.

Do not skip heading levels merely to achieve a visual size. Style semantic headings independently when needed.

## Body Copy

Body text should be easy to scan.

- Use short paragraphs.
- Avoid unnecessary jargon.
- Keep line lengths comfortable.
- Use adequate contrast.
- Separate paragraphs with intentional spacing.

## Labels

Labels should be concise and descriptive.

For forms, labels must identify the field even when placeholder text disappears.

Avoid using placeholder text as the only label.

## Buttons

Button typography should be clear and confident.

- Use concise verbs.
- Avoid unnecessarily long CTA text.
- Maintain consistent font size across button variants.
- Use weight to establish importance.

Examples:

- `Create project`
- `Save changes`
- `View details`
- `Get started`

## Data-Dense Interfaces

For dashboards, tables, and admin systems:

- Use 14–16px body sizes as appropriate.
- Keep numeric values aligned.
- Use muted text for secondary metadata.
- Make important values visually prominent.
- Avoid shrinking text excessively to fit more information.

Density should be intentional, not cramped.

## Responsive Typography

At smaller widths:

- Reduce display sizes.
- Preserve readable body size.
- Reduce heading line length.
- Rebalance vertical spacing.
- Avoid headings that occupy most of the viewport.

Prefer fluid typography when appropriate, for example with `clamp()`, while keeping accessibility and readability intact.

## Typography and Accessibility

- Maintain adequate contrast.
- Never communicate meaning through font weight alone.
- Do not disable browser text scaling.
- Keep body text readable.
- Preserve visible focus and state indicators.
- Avoid tiny text for essential information.

## Typography and Performance

Performance matters when loading fonts.

- Minimize font families.
- Minimize unnecessary weights.
- Prefer modern font formats.
- Use appropriate font-display behavior.
- Avoid loading large font files when a smaller subset is sufficient.
- Use framework-supported font optimization where available.

## Premium Typography Review

Before shipping, ask:

- Can typography be improved?
- Is the hierarchy immediately obvious?
- Does the heading feel premium rather than oversized for its own sake?
- Is body text comfortable to read?
- Are weights used intentionally?
- Are line lengths controlled?
- Is responsive typography polished?
- Are labels and metadata appropriately subordinate?
- Does the typography match the product personality?
- Is the typography accessible and performant?
