# Table UX Standards

## Purpose

Tables should make structured information easy to scan, compare, filter, sort, and act on. They should remain usable with realistic datasets, not only a handful of sample rows.

## Core Principle

Optimize tables for the user's task.

Before designing a table, identify:

- What users need to compare.
- Which columns are most important.
- Which actions users perform most often.
- How large the dataset can become.
- Which filters and sorting capabilities are necessary.

Do not add columns merely because the backend exposes them.

## Column Priority

Place the most important information toward the left where possible.

Use progressive disclosure for secondary information when showing everything at once would make the table difficult to scan.

## Headers

Headers should:

- Clearly describe the column.
- Use consistent terminology.
- Remain visually distinct from data rows.
- Communicate sort state when sorting is available.

Avoid unnecessarily long header labels.

## Alignment

Use alignment that supports scanning.

Typically:

- Text → left aligned
- Numbers → right aligned when comparison benefits from it
- Statuses → visually grouped or centered where appropriate
- Actions → consistent alignment, often right aligned

Consistency matters more than rigid rules.

## Row Density

Choose row height based on the task.

Dense tables are appropriate for professional workflows where users need to process many records. Less dense tables are appropriate when rows contain richer content.

Do not make rows so compact that text and controls become difficult to use.

## Zebra Striping

Use row striping only when it improves scanning.

Subtle borders or hover states may be enough. Avoid strong alternating backgrounds that create visual noise.

## Row Hover

Hover states should provide useful feedback without overpowering the data.

For interactive rows, make the interaction discoverable and ensure keyboard users receive an equivalent focus state.

## Sorting

Sorting should:

- Clearly indicate the active column.
- Clearly indicate ascending or descending order.
- Preserve user expectations.
- Work consistently across data types.

Do not make a header look sortable unless it actually is.

## Filtering

Filters should help users narrow large datasets.

Use appropriate controls such as:

- Search
- Select
- Multi-select
- Date range
- Status filters
- Numeric ranges

Keep commonly used filters easy to access.

## Search

For large tables, provide search when users need to find specific records.

- Debounce network-backed search where appropriate.
- Clearly communicate what fields are searched.
- Preserve the query when navigating or refreshing where useful.

## Pagination

Pagination is useful when datasets are large and users work page-by-page.

Show:

- Current page
- Total pages or meaningful range information
- Page size where useful
- Previous/next controls

Do not make users lose their filters when changing pages.

## Virtualization

Consider virtualization for very large datasets where rendering every row creates performance problems.

Virtualization should not be introduced merely because it sounds performant. Use it when the dataset and interaction model justify the complexity.

## Selection

If rows can be selected:

- Provide clear selected state.
- Support select-all when appropriate.
- Explain what select-all means across paginated datasets.
- Provide bulk actions near the selected state.

Do not hide important bulk actions after selection.

## Row Actions

Keep common actions discoverable.

Use:

- Inline actions for frequent operations.
- A contextual menu for secondary actions.
- Confirmation for destructive or irreversible operations.

Avoid filling every row with many competing buttons.

## Status Cells

Statuses should be easy to scan.

Use consistent badges or labels and semantic colors.

Do not rely on color alone.

Examples:

- Active
- Pending
- Completed
- Failed
- Draft
- Archived

## Long Content

Handle long values intentionally.

Options include:

- Truncation with tooltip
- Wrapping
- Expandable details
- Dedicated detail page

Never silently truncate critical information without a way to access the full value.

## Responsive Tables

Do not automatically squeeze every column into a narrow mobile viewport.

Possible strategies:

- Horizontal scrolling
- Priority columns
- Stacked cards for small datasets
- Responsive column visibility
- Detail drawer/page for secondary information

Choose based on the user's task.

## Loading States

Prefer table skeletons that match the approximate table structure when the data is loading.

Avoid replacing the entire application with a spinner because table data is pending.

## Empty States

Differentiate between:

- No data exists yet.
- Filters returned no results.
- Search returned no results.
- Data failed to load.

Each state should provide appropriate next actions.

## Error States

Keep table errors localized.

Provide:

- Clear explanation
- Retry action
- Context about what failed

Do not erase unrelated page content when a table request fails.

## Accessibility

Tables should have:

- Semantic table structure when appropriate.
- Clear headers.
- Keyboard-accessible controls.
- Visible focus states.
- Accessible sort and filter controls.
- Meaningful labels for icon-only actions.

Do not use a visual grid of `div`s as a table when semantic table behavior is required.

## Performance

For large datasets:

- Fetch only required fields.
- Paginate or virtualize appropriately.
- Avoid expensive formatting on every render.
- Memoize expensive calculations only when useful.
- Keep row components efficient.
- Avoid rendering hidden rows unnecessarily.

## Premium Table Quality

A premium table is not defined by decoration. It is defined by clarity and efficiency.

Use restrained:

- Borders
- Background changes
- Hover states
- Typography hierarchy
- Status treatments

Avoid excessive shadows, gradients, and visual noise.

## Table Review

Before shipping, ask:

- Can users understand the table immediately?
- Are the most important columns prioritized?
- Is scanning easy?
- Are alignment and spacing consistent?
- Are sorting and filtering understandable?
- Are row actions appropriately prioritized?
- Are loading, empty, and error states handled?
- Does it work on mobile?
- Is it accessible by keyboard and assistive technology?
- Will it remain performant with realistic data?
- Is the component reusable?
- Is this something I'd be proud to ship?
