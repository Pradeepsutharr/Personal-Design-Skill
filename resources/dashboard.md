# Dashboard UX Standards

## Purpose

Dashboards should help users understand status, identify important changes, and take action quickly. A premium dashboard is optimized for decisions, not decoration.

## Core Principle

Design around the user's questions.

Before building a dashboard, identify:

- What does the user need to know immediately?
- What decisions do they make here?
- What actions happen most frequently?
- Which metrics are critical?
- Which information is secondary?

Do not begin with a grid of cards. Begin with the user's workflow.

## Information Hierarchy

A strong dashboard usually follows a hierarchy such as:

1. Page context and primary action
2. Key health/status indicators
3. Important trends or changes
4. Primary operational data
5. Secondary details

Not every dashboard needs every layer.

## Page Header

The header should communicate:

- Where the user is.
- What the page represents.
- What important global context applies.
- What primary action is available.

Keep the header concise.

## KPI Cards

Use KPI cards for genuinely important metrics.

A good KPI card can include:

- Metric name
- Current value
- Comparison or trend
- Time period
- Relevant status

Avoid creating ten cards merely because there are ten metrics.

## Metric Hierarchy

Use typography to distinguish:

- Primary number
- Metric label
- Supporting comparison
- Context or timestamp

Do not make every value visually dominant.

## Charts

Charts should answer a question.

Before adding a chart, ask:

- What decision does this visualization support?
- Is a chart better than a simple number or table?
- What comparison matters?
- What time period matters?

Avoid decorative charts with no actionable meaning.

## Chart Design

Charts should:

- Have clear labels.
- Use consistent scales.
- Avoid unnecessary grid lines.
- Highlight meaningful values.
- Provide accessible legends or labels.
- Work reasonably on mobile.

Do not rely on color alone to distinguish series.

## Filters

Place important filters where users expect them.

Common filters include:

- Date range
- Status
- Location
- Owner
- Category
- Search

Make active filters visible and easy to clear.

## Date Context

When metrics depend on time, communicate the period clearly.

Avoid ambiguous labels such as `Revenue` without indicating whether it means today, this month, or another period.

## Tables

Use tables when users need exact values, comparison, or record-level action.

Keep dashboards from becoming tables surrounded by decorative cards. Each visual should have a purpose.

## Navigation

Dashboard navigation should remain predictable.

- Highlight current location.
- Group related sections.
- Avoid excessive nesting.
- Keep frequently used destinations accessible.

## Empty Dashboards

A new account may have no data.

Design useful empty states that explain:

- What will appear here.
- Why it matters.
- How to create the first relevant record.

Avoid presenting an empty grid of blank cards.

## Loading Dashboards

Use skeleton structures that resemble the eventual content.

Avoid large spinners when multiple independent dashboard sections can load progressively.

## Error Handling

If one dashboard widget fails, avoid taking down the entire dashboard.

Provide a localized error and retry action when appropriate.

## Responsive Behavior

On mobile:

- Prioritize key metrics.
- Stack or horizontally scroll complex content intentionally.
- Simplify chart controls.
- Avoid unreadable dense tables.
- Keep primary actions reachable.

Do not simply compress a desktop dashboard into a narrow screen.

## Density

Enterprise dashboards can be information-dense, but density must remain structured.

Use:

- Clear grouping
- Strong typography hierarchy
- Consistent spacing
- Subtle dividers
- Predictable alignment

Avoid visual clutter.

## Interaction Design

Important dashboard interactions should have clear feedback.

Examples:

- Filter changes update visible data.
- Export shows progress and completion.
- Save actions confirm success.
- Destructive actions require appropriate confirmation.

## Performance

Dashboards often contain many data sources.

Optimize by:

- Fetching independent data concurrently where possible.
- Loading secondary widgets progressively.
- Lazy-loading heavy visualizations.
- Avoiding unnecessary client-side rendering.
- Paginating or virtualizing large tables.
- Caching stable data where appropriate.

## Accessibility

Ensure:

- Semantic headings establish page structure.
- Charts have accessible summaries or alternative representations where needed.
- Filters are keyboard accessible.
- Icon-only actions have accessible labels.
- Color is not the only state indicator.
- Focus states are visible.

## Premium Dashboard Aesthetic

Premium does not mean adding gradients to every card.

Use:

- Strong hierarchy
- Restrained surfaces
- Consistent spacing
- Refined typography
- Subtle borders
- Purposeful accent color
- Carefully selected visualization
- Polished micro-interactions

## Dashboard Review

Before shipping, ask:

- Can the user understand the dashboard in seconds?
- Is the most important information obvious?
- Are KPI cards actually necessary?
- Does every chart answer a useful question?
- Are filters understandable?
- Are loading, empty, and error states designed?
- Does it work with realistic data?
- Is the mobile experience intentional?
- Is the dashboard accessible?
- Is client-side JavaScript minimized?
- Are expensive charts and tables optimized?
- Is the UI consistent with the rest of the product?
- Is it visually premium?
- Is this something I'd be proud to ship?
