# Spacing and Layout Standards

## Purpose

Spacing creates hierarchy, rhythm, readability, and perceived quality. Premium interfaces use spacing deliberately rather than filling every available area.

## Core Principle

Use spacing to communicate relationships.

- Small gap = strong relationship
- Medium gap = related group
- Large gap = separate concept
- Extra-large gap = major section transition

If two elements belong together, their spacing should make that relationship obvious.

## Base Scale

Use an 8px-oriented scale by default:

`4, 8, 12, 16, 20, 24, 32, 40, 48, 64, 80, 96, 128`

4px can be used for fine adjustments. Larger values should be reserved for meaningful separation.

Do not use the scale mechanically when optical alignment requires a small adjustment, but avoid arbitrary values becoming the norm.

## Component Internal Spacing

Typical starting points:

- Compact control padding: 8–12px
- Standard control padding: 12–16px
- Card padding: 20–24px
- Large panel padding: 24–32px
- Major feature surface: 32–48px

Tune based on density, content length, and viewport.

## Vertical Rhythm

Vertical spacing should establish hierarchy.

A useful pattern is:

- Label → field: small
- Field → helper/error: small
- Field group → field group: medium
- Form group → section: large
- Section → section: extra-large

Do not use identical spacing between every element. Uniform spacing without hierarchy makes interfaces feel flat.

## Page Sections

Major sections should have intentional breathing room.

Marketing pages may use larger vertical spacing than dense enterprise dashboards.

Use responsive section spacing rather than a single fixed value.

Example approach:

- Mobile: 48–72px
- Tablet: 64–88px
- Desktop: 80–120px

These are starting points, not rigid requirements.

## Containers

Use a consistent page container.

- Keep horizontal padding comfortable on mobile.
- Increase gutters on larger screens.
- Use a max width to prevent excessive line length.
- Keep major sections aligned to the same content grid.

Avoid having each section invent its own left and right edges unless the visual design intentionally calls for it.

## Grid

Use grids to create structure.

Common patterns:

- 12-column desktop grid
- 8-column tablet grid
- 4-column mobile grid

The exact implementation may vary by framework, but alignment should remain consistent.

## Gaps

Prefer `gap` in flex and grid layouts when elements form a collection. This usually creates cleaner responsive behavior than scattered margins.

Use margins when spacing expresses a semantic relationship to surrounding content.

## Alignment

Check alignment across:

- Headings
- Body copy
- Cards
- Inputs
- Buttons
- Tables
- Navigation
- Section boundaries

Misalignment is one of the fastest ways to make otherwise good UI look unfinished.

## Density

Density should match the task.

### Marketing UI

Use generous spacing and strong visual hierarchy.

### Enterprise dashboard

Use tighter spacing while preserving readability.

### Data-heavy tables

Optimize for scanning and comparison rather than decoration.

Do not confuse compactness with cramping.

## Responsive Spacing

Spacing should adapt across breakpoints.

Reduce:

- Page gutters
- Section spacing
- Large card padding
- Display heading margins

on smaller screens when necessary.

Do not simply scale every spacing value proportionally. Preserve the relationships that matter most.

## Optical Spacing

Mathematical equality does not always look equal.

For example:

- Icons may need slight visual adjustment relative to text.
- Rounded buttons can require different vertical padding than square controls.
- Large headings may need tighter spacing than body copy.

Use optical judgment while maintaining system consistency.

## Avoid

- Random margin values everywhere
- Huge empty spaces without purpose
- Cramped cards
- Inconsistent page gutters
- Different spacing for identical components
- Excessive padding that reduces usable content area
- Using whitespace to compensate for weak hierarchy

## Spacing Review

Before shipping, ask:

- Can spacing be improved?
- Is the hierarchy clear without reading every word?
- Are related elements grouped tightly enough?
- Are unrelated sections separated enough?
- Are page gutters consistent?
- Do cards have balanced internal padding?
- Is mobile spacing comfortable?
- Does the interface feel spacious rather than empty?
- Does the interface feel dense rather than cramped?
- Is the spacing system consistent across the product?
