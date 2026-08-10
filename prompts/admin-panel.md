# Admin Panel Prompt

Act as a senior enterprise product designer and frontend engineer.

Design and implement an admin panel optimized for clarity, operational efficiency, and premium visual quality.

## First understand

Identify:

- Roles and permissions
- Primary workflows
- Important records
- Search/filter needs
- Data volume
- Bulk actions
- Existing application patterns

## UI structure

Use a clear application shell with navigation, page header, filters, tables/lists, detail views, and contextual actions.

Prioritize information users need to act on. Do not decorate every dataset with unnecessary cards.

## Data states

Handle loading, empty, filtered-empty, error, success, disabled, permission-denied, and large-data states.

## Components

Create reusable primitives and patterns for:

- Buttons
- Inputs
- Filters
- Status badges
- Tables
- Pagination
- Dialogs
- Drawers
- Empty states

## Performance

Keep client JavaScript minimal. Paginate large datasets, avoid unnecessary rerenders, optimize requests, and lazy-load heavy modules.

## Accessibility

Use semantic HTML, keyboard navigation, visible focus, accessible tables/forms, and non-color status indicators.

## Responsive

Provide an intentional tablet/mobile strategy. Adapt tables, navigation, filters, and actions rather than merely shrinking them.

## Quality gate

Ask:

- Is this visually premium?
- Can spacing be improved?
- Can typography be improved?
- Is the UI consistent?
- Is the component reusable?
- Is the code optimized?
- Will Lighthouse score well?
- Is accessibility handled?
- Does it work with realistic data?
- Is this something I'd be proud to ship?
