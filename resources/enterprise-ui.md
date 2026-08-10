# Enterprise UI Standards

## Purpose

Enterprise applications must handle complex workflows, dense information, permissions, long sessions, and large datasets without becoming confusing or visually dated.

## Core Principle

Optimize for clarity, efficiency, trust, and repeat usage.

Enterprise UI should feel powerful without feeling complicated.

## Information Architecture

Organize features around user workflows rather than backend entities alone.

Before building a screen, identify:

- Primary task
- Secondary tasks
- Frequently accessed information
- Important decisions
- Destructive operations
- User roles and permissions

## Navigation

Enterprise navigation should remain predictable over time.

Use:

- Clear active states
- Logical grouping
- Consistent labels
- Search when navigation becomes large
- Breadcrumbs where hierarchy is deep

Avoid deeply nested menus unless the information architecture genuinely requires them.

## Application Shell

A consistent shell can include:

- Sidebar/navigation
- Top bar
- Page header
- Main content area
- Contextual actions

Persistent elements should remain stable so users can build muscle memory.

## Dense Information

Density is useful when users process information frequently.

Use:

- Compact but readable controls
- Strong alignment
- Consistent row heights
- Clear hierarchy
- Subtle separators
- Efficient whitespace

Do not make everything oversized in the name of modern design.

## Progressive Disclosure

Do not expose every option immediately.

Reveal secondary actions through:

- Menus
- Drawers
- Detail panels
- Advanced filter sections
- Contextual actions

Keep frequent actions visible.

## Search

Large enterprise systems should provide strong search where users need to locate records, pages, or resources.

Search should:

- Have a clear purpose.
- Communicate what it searches.
- Provide useful empty states.
- Handle loading and errors.
- Preserve useful query state.

## Filters

Complex filters should be grouped logically.

Prefer:

- Common filters near the primary content.
- Advanced filters behind a clear control.
- Visible active filter indicators.
- One-click clearing where practical.

## Permissions

Design for permissions explicitly.

Users should not see confusing actions they cannot perform.

Where permissions require disabled controls, explain why when useful. Do not rely solely on unexplained disabled buttons.

## Forms

Enterprise forms may be complex, but they should remain structured.

Use:

- Sections
- Clear labels
- Helpful descriptions
- Validation
- Save state
- Unsaved-change protection when necessary

## Tables

Tables are often primary enterprise workspaces.

Support appropriate combinations of:

- Sorting
- Filtering
- Search
- Pagination
- Selection
- Bulk actions
- Column visibility
- Row actions
- Export

Do not implement every feature automatically. Add capabilities based on the workflow.

## Bulk Actions

When users manage many records:

- Make selection state obvious.
- Surface available bulk actions.
- Communicate scope.
- Require confirmation for destructive operations.

## Detail Views

Record detail screens should prioritize the user's next action.

A useful structure can include:

- Record identity
- Status
- Primary actions
- Important summary
- Detailed information
- Activity/history
- Related records

## Status Design

Status should be consistent throughout the application.

Use the same label and semantic color for the same concept everywhere.

Avoid inventing different visual meanings for identical states.

## Notifications

Use notifications for meaningful feedback.

Appropriate examples:

- Save succeeded
- Import completed
- Background operation failed
- Permission changed

Avoid noisy notifications for every minor interaction.

## Long-Running Operations

Enterprise workflows can involve imports, exports, processing, or integrations.

Provide:

- Progress where meaningful
- Clear status
- Ability to continue working when possible
- Completion notification
- Error recovery

Do not make users stare at a blocking spinner unnecessarily.

## Unsaved Changes

Protect users from losing meaningful work.

When appropriate:

- Indicate unsaved state.
- Warn before leaving.
- Provide save/discard choices.

Do not interrupt users for trivial changes.

## Audit and History

For systems requiring traceability, make activity understandable.

Show:

- What changed
- Who changed it when appropriate
- When it changed
- Relevant context

Keep audit information readable rather than dumping raw technical logs into the UI.

## Responsive Enterprise UI

Responsive behavior should preserve workflows.

On smaller screens:

- Prioritize essential actions.
- Collapse secondary navigation.
- Move secondary details into drawers or detail pages.
- Use responsive tables intentionally.
- Preserve readable controls.

Do not simply scale the desktop UI down until everything becomes unusable.

## Accessibility

Enterprise users may spend many hours in the application.

Ensure:

- Keyboard navigation
- Visible focus
- High-quality contrast
- Clear labels
- Predictable interaction
- Reduced motion support
- Screen-reader compatibility where relevant

## Performance

Enterprise applications often contain substantial data and complex screens.

Use:

- Server-side data fetching where appropriate
- Pagination
- Virtualization for large datasets
- Lazy loading for heavy features
- Efficient state boundaries
- Request caching where appropriate

Avoid unnecessary client-side JavaScript.

## Visual Quality

Enterprise does not mean boring.

Use:

- Refined typography
- Consistent spacing
- Subtle surfaces
- Clear hierarchy
- Restrained accent colors
- Purposeful micro-interactions

Avoid excessive decorative effects that compete with operational tasks.

## Enterprise UI Review

Before shipping, ask:

- Can a frequent user complete the primary workflow quickly?
- Is navigation predictable?
- Is information density appropriate?
- Are important actions obvious?
- Are permissions understandable?
- Are tables and forms optimized for real workflows?
- Are loading and long-running states handled?
- Is unsaved work protected?
- Is the UI accessible?
- Will it remain performant with realistic data?
- Is the component architecture reusable?
- Is the visual system consistent?
- Is the experience premium without sacrificing efficiency?
- Is this something I'd be proud to ship?
