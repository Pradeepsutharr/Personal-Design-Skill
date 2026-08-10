# Dashboard Example

Use this example when designing or reviewing a SaaS, admin, analytics, or enterprise dashboard.

## Recommended Structure

```text
Application Shell
  ├─ Sidebar / Navigation
  ├─ Top Bar
  └─ Main Content

Page Header
  ├─ Breadcrumb / Context
  ├─ Page Title
  ├─ Supporting description
  └─ Primary action

Context / Filters
  ├─ Date range
  ├─ Search
  ├─ Status
  └─ Other relevant filters

Key Metrics
  ├─ KPI 1
  ├─ KPI 2
  ├─ KPI 3
  └─ KPI 4

Primary Visualization
  └─ Chart answering a real business question

Operational Data
  └─ Table / List

Secondary Insights
  ├─ Supporting chart
  └─ Activity / status panel

Final / Secondary Actions
```

## Design Principle

Do not start by creating a grid of cards.

Start with the user's questions:

- What is happening?
- What changed?
- What needs attention?
- What action should I take?

Then select the UI pattern that best answers each question.

## Page Header Example

```text
Dashboard
A quick overview of your marina operations.

[Date range] [Export report] [Add booking]
```

The actual content should reflect the product's domain.

## KPI Cards

Use KPI cards for high-value information only.

Example:

```text
Occupancy
82%
+6.4% vs last month
```

A KPI should communicate:

- What is being measured
- Current value
- Useful comparison or trend
- Relevant time context

Avoid decorative metrics that do not support a decision.

## Charts

Every chart should answer a question.

Examples:

- How is revenue changing?
- How full is capacity over time?
- Which locations are busiest?
- Where are operational bottlenecks?

If a chart cannot answer a useful question, consider a number, table, or status indicator instead.

## Table Example

```text
Bookings

Search bookings...     Status     Date range

Customer       Berth       Arrival      Departure     Status       Action
---------------------------------------------------------------
Acme Marine    A-12        Jul 08       Jul 14        Confirmed    View
...
```

Support realistic workflows such as sorting, filtering, pagination, row actions, and bulk operations only when needed.

## Loading State

Prefer skeleton structures that match the eventual content.

Example:

```text
[ KPI skeleton ] [ KPI skeleton ] [ KPI skeleton ]

[        chart skeleton                     ]

[        table row skeleton                 ]
[        table row skeleton                 ]
```

Avoid a single page-wide spinner when independent sections can load separately.

## Empty State

Example:

```text
No bookings yet

Create your first booking to start tracking marina activity.

[Create booking]
```

Do not show empty charts and blank cards without context.

## Error State

Keep errors localized.

Example:

```text
Unable to load occupancy data

We couldn't retrieve the latest occupancy information.

[Try again]
```

Do not destroy the rest of the dashboard when one widget fails.

## Responsive Strategy

### Desktop

Use a structured grid with clear alignment and appropriate information density.

### Tablet

Reduce columns and allow important sections to occupy more width.

### Mobile

Prioritize:

1. Page context
2. Primary action
3. Most important metrics
4. Critical operational data
5. Secondary insights

Do not simply shrink a desktop dashboard.

## Performance Strategy

- Fetch independent dashboard data concurrently where appropriate.
- Server-render content when possible.
- Isolate interactive charts into client components.
- Lazy-load heavy visualizations when useful.
- Paginate large tables.
- Avoid rendering unnecessary rows.
- Optimize chart libraries and dependencies.
- Avoid excessive animation.

## Accessibility Strategy

- Use semantic headings.
- Give charts meaningful accessible summaries or alternatives.
- Ensure filters are keyboard accessible.
- Provide accessible names for icon buttons.
- Use color plus text/icons for status.
- Preserve visible focus states.

## Visual Direction

Premium dashboard design should emphasize:

- Strong typography hierarchy
- Precise spacing
- Restrained surfaces
- Subtle borders
- Consistent card geometry
- Purposeful accent colors
- High-quality data visualization
- Subtle micro-interactions

Avoid turning every widget into a floating card with a heavy shadow.

## Review Questions

- Is the most important information obvious immediately?
- Does every widget have a purpose?
- Can spacing be improved?
- Can typography be improved?
- Is the UI consistent?
- Is the component reusable?
- Is the code optimized?
- Will Lighthouse score well?
- Is the page accessible?
- Is the dashboard responsive?
- Does it work with realistic data sizes?
- Are loading, empty, and error states polished?
- Is this something I'd be proud to ship?
