# Charts Example

Use this example when designing dashboards, analytics, reports, and operational data visualizations.

## Core Principle

A chart should answer a real question. Do not add charts simply because a dashboard looks more sophisticated with them.

## Choose the Right Visualization

Use:

- Line charts → trends over time
- Bar charts → category comparison
- Stacked bars → composition across categories
- Area charts → volume/trend when appropriate
- Scatter plots → relationships between variables
- Tables → exact values and detailed comparison
- KPI cards → single high-value metrics

## Chart Structure

```text
Chart title
Short explanation / context

[ Visualization ]

Legend / controls
Source / time context when needed
```

## Titles

Chart titles should communicate the metric or question.

Weak:

`Revenue`

Better:

`Revenue by month`

When useful, add a short explanation of the comparison or period.

## Color

Use color semantically and consistently.

- Do not use a rainbow palette without meaning.
- Keep related series visually related.
- Ensure sufficient contrast.
- Do not rely only on color to distinguish states.

## Tooltips

Tooltips can expose exact values while keeping the chart visually clean.

Ensure tooltip content is readable and does not become the only way to understand the visualization.

## Empty State

Do not render an empty chart frame with no explanation.

Example:

```text
No revenue data yet

Revenue trends will appear once transactions are recorded.
```

## Loading State

Use a chart-shaped skeleton or reserved visual area to minimize layout shift.

## Error State

Keep errors localized:

```text
Unable to load revenue data
[Try again]
```

## Accessibility

Charts should have an accessible summary or an equivalent data representation when the visualization contains important information.

Provide:

- Meaningful title
- Text alternative where needed
- Accessible controls
- Keyboard access for interactive controls
- Non-color indicators when color communicates state

## Responsive Strategy

### Desktop

Use enough width to support comparison without unnecessary whitespace.

### Mobile

Consider:

- Simplified visualization
- Horizontal scrolling for inherently wide charts
- Summary metrics above the chart
- Table/detail alternative

Do not make labels unreadably small just to keep the desktop chart dimensions.

## Performance

- Avoid loading a large charting library for a simple visualization.
- Lazy-load complex charts when below the fold.
- Limit unnecessary animations.
- Avoid rendering thousands of points when aggregation is sufficient.
- Memoize or precompute expensive transformations only when measurement justifies it.

## Animation

Use animation to communicate change, not decoration.

Respect reduced-motion preferences.

Avoid continuously animated charts unless there is a genuine real-time use case.

## Visual Direction

Premium data visualization comes from:

- Strong hierarchy
- Accurate data
- Restrained colors
- Clean axes
- Clear labels
- Consistent spacing
- Subtle interaction feedback

Do not sacrifice data clarity for visual spectacle.

## Review Questions

- Does the chart answer a useful question?
- Is the data accurate and understandable?
- Can spacing be improved?
- Can typography be improved?
- Is the UI consistent?
- Is the component reusable?
- Is the chart performant with realistic data?
- Is accessibility handled?
- Does it work on mobile?
- Does the visualization remain understandable without color alone?
- Is this something I'd be proud to ship?
