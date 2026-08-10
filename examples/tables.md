# Tables Example

Use this example when designing or reviewing admin, SaaS, operations, analytics, or enterprise data tables.

## Recommended Structure

```text
Page Header
  ├─ Title
  ├─ Description
  └─ Primary action

Toolbar
  ├─ Search
  ├─ Common filters
  ├─ Advanced filters
  ├─ Column controls (optional)
  └─ Bulk actions when selected

Table
  ├─ Header
  ├─ Data rows
  └─ Row actions

Footer
  ├─ Result count
  ├─ Page size
  └─ Pagination
```

## Example

```text
Bookings
Manage and monitor marina reservations.

[Search bookings...] [Status] [Date range] [Export] [Create booking]

☐  Customer       Berth       Arrival     Departure    Status       Actions
──────────────────────────────────────────────────────────────────────────
☐  Acme Marine    A-12        Jul 08      Jul 14       Confirmed    View ⋯
☐  Ocean Works    B-04        Jul 10      Jul 18       Pending      View ⋯

Showing 1–20 of 128                         [Previous] 1 2 3 [Next]
```

## Column Priority

Put the most important information first.

Typical order:

1. Identity
2. Primary business information
3. Status
4. Important dates/metrics
5. Secondary metadata
6. Actions

Do not expose every backend field merely because it exists.

## Search

Search should clearly communicate what it searches.

Example:

`Search customer, booking ID, or berth...`

For network-backed search, debounce appropriately and preserve the query when useful.

## Filters

Keep high-value filters immediately accessible.

Use advanced filters for less frequently used criteria.

Example:

```text
[Status] [Date range] [Marina] [More filters]

Active filters:
[Confirmed ×] [This month ×] [Clear all]
```

## Sorting

Sortable headers should clearly communicate:

- Sortable state
- Active column
- Ascending/descending direction

Do not visually imply sorting support if the column is not sortable.

## Row Actions

Use inline actions for frequent operations.

Use a contextual menu for secondary actions.

Example:

```text
View   Edit   ⋯
```

Avoid five or six equally prominent buttons in every row.

## Selection and Bulk Actions

When rows are selected:

```text
3 selected

[Export] [Assign] [Change status] [Delete]
```

Make scope clear, especially when pagination is involved.

## Status

Use semantic badges or labels.

Example:

```text
Confirmed
Pending
Cancelled
Completed
```

Do not rely only on badge color. Include readable text or another meaningful indicator.

## Loading State

Use table-shaped skeletons.

```text
[Header]
[Row skeleton]
[Row skeleton]
[Row skeleton]
[Row skeleton]
```

Avoid replacing the complete page with a spinner.

## Empty State

Differentiate between no records and no filter results.

### No data

```text
No bookings yet

Create your first booking to start managing reservations.

[Create booking]
```

### No search results

```text
No bookings match your search

Try a different search term or clear the filters.

[Clear filters]
```

## Error State

Keep the error localized.

```text
Unable to load bookings

We couldn't retrieve the latest bookings.

[Try again]
```

## Long Content

Handle long values intentionally.

Options:

- Truncation + tooltip
- Wrapping
- Detail drawer
- Detail page

Never silently hide critical information.

## Responsive Strategy

### Desktop

Use full table comparison when practical.

### Tablet

Hide lower-priority columns or allow intentional horizontal scrolling.

### Mobile

Use one of:

- Horizontal table scrolling
- Priority-column table
- Stacked record cards
- Detail drawer/page

Choose based on whether users need comparison or record-level actions.

Do not squeeze every column into a narrow viewport.

## Performance Strategy

For large datasets:

- Paginate server-side when appropriate.
- Fetch only required fields.
- Virtualize when rendering volume genuinely requires it.
- Avoid expensive formatting on every render.
- Keep row components efficient.
- Avoid rendering hidden rows unnecessarily.

## Accessibility

Use semantic table markup when the data represents a table.

Ensure:

- Header relationships are meaningful.
- Sort controls are accessible.
- Row actions have accessible names.
- Selection controls are labeled.
- Focus states are visible.
- Keyboard navigation works.

## Visual Direction

Premium tables should prioritize clarity over decoration.

Use:

- Strong header hierarchy
- Precise row height
- Subtle borders
- Restrained hover states
- Consistent status treatments
- Clear action hierarchy

Avoid:

- Heavy shadows on every row
- Excessive colors
- Oversized rows
- Unnecessary card nesting

## Review Questions

- Can users scan the data immediately?
- Are important columns prioritized?
- Can spacing be improved?
- Can typography be improved?
- Is the UI consistent?
- Are filters and sorting clear?
- Are row actions appropriately prioritized?
- Are loading, empty, and error states polished?
- Is the component reusable?
- Is the code optimized?
- Will it remain performant with realistic datasets?
- Is the table accessible?
- Is the mobile strategy intentional?
- Is this something I'd be proud to ship?
