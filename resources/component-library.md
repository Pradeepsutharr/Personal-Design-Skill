# Component Library Standards

## Purpose

Build reusable components that create consistency, reduce duplication, preserve accessibility, and allow the product to scale without visual drift.

## Core Principle

A reusable component should represent a meaningful repeated pattern, not merely a few lines of JSX.

Before creating a component, ask:

- Is this pattern reused or likely to be reused?
- Does it have a clear responsibility?
- Are its variants predictable?
- Can it be configured without excessive conditional logic?
- Does abstraction improve consistency?

## Component Hierarchy

A practical hierarchy is:

1. Primitives — buttons, inputs, icons, labels
2. Components — cards, dialogs, dropdowns, form fields
3. Patterns — filter bars, data tables, navigation shells
4. Sections — dashboard panels, hero sections, feature blocks
5. Pages — composed experiences

Avoid making every visual element a primitive.

## Single Responsibility

Components should have focused responsibilities.

Avoid a component that simultaneously manages:

- Data fetching
- Global state
- Complex business logic
- Layout
- Multiple unrelated visual patterns

Separate concerns when doing so improves clarity and testability.

## Component API

Keep public component APIs intentional.

Prefer:

- Clear prop names
- Sensible defaults
- Explicit variants
- Composition through `children` when appropriate
- Predictable event callbacks

Avoid giant prop interfaces containing dozens of rarely used flags.

## Variants

Use variants for meaningful visual or behavioral differences.

Examples:

- Button: primary, secondary, ghost, destructive
- Input: default, error, disabled
- Card: default, interactive, elevated
- Badge: success, warning, error, neutral

Do not create a variant for every tiny visual adjustment.

## Composition

Prefer composition when a component needs flexible content.

Examples:

- Card with header/content/footer regions
- Dialog with title/body/actions
- Table with configurable columns
- Form sections with reusable fields

Composition is often more maintainable than dozens of boolean props.

## Accessibility

Reusable components must preserve accessibility by default.

Every interactive component should account for:

- Semantic HTML
- Keyboard navigation
- Focus states
- Accessible names
- Disabled state
- Loading state
- Error state where relevant
- Reduced motion where relevant

Do not require every consumer to remember basic accessibility behavior.

## State Coverage

Define component states explicitly.

Typical states:

- Default
- Hover
- Focus-visible
- Active
- Selected
- Disabled
- Loading
- Error
- Empty

The component should not look unfinished when a real application state occurs.

## Controlled and Uncontrolled

Support controlled behavior when a component's state needs external coordination.

For simple components, uncontrolled usage can be appropriate.

Do not force a complex controlled API when local state is sufficient.

## Data Components

Reusable data components should support realistic data.

Consider:

- Empty state
- Loading state
- Error state
- Long content
- Large datasets
- Pagination
- Responsive behavior
- Accessibility

## Styling

Components should use the application's design tokens.

Avoid hardcoding independent colors, spacing, typography, and radius values that cause visual drift.

## Tailwind Components

When using Tailwind:

- Keep class names organized.
- Use semantic tokens.
- Extract repeated patterns.
- Use variant utilities where appropriate.
- Avoid uncontrolled arbitrary values.

## Third-Party Components

When using libraries such as shadcn/ui or Ant Design:

- Reuse existing primitives when they meet requirements.
- Customize through supported APIs where possible.
- Preserve accessibility behavior.
- Avoid unnecessary duplicate implementations.
- Keep the visual language consistent with custom components.

## Client Components

In Next.js:

- Keep reusable static components server-compatible when possible.
- Isolate client-only behavior.
- Do not mark an entire component tree as client-side for one interactive child.

## Performance

Reusable components should avoid unnecessary work.

Consider:

- Stable props
- Efficient rendering
- Avoiding expensive calculations during render
- Virtualization for large collections
- Lazy loading heavy components where useful

Do not add memoization automatically. Use it when it provides meaningful benefit.

## Naming

Names should describe the component's purpose.

Prefer:

- `BookingStatusBadge`
- `UserAvatar`
- `FilterBar`
- `DataTable`
- `PageHeader`

Avoid vague names such as:

- `Box2`
- `CustomThing`
- `NewComponent`

## File Organization

Keep component structure predictable.

A project may organize components by:

- Shared UI
- Feature/domain
- Layout
- Page-specific components

Follow the existing project's conventions when they are sound.

## Documentation

Complex reusable components should document:

- Purpose
- Props
- Variants
- Usage constraints
- Accessibility expectations
- Important interaction behavior

Do not document trivial components with unnecessary prose.

## Testing

Reusable components should be tested for important behavior.

Prioritize:

- User interactions
- Keyboard behavior
- Form validation
- Loading/error states
- Variant behavior
- Critical accessibility behavior

## Component Review

Before shipping, ask:

- Is the component genuinely reusable?
- Is its API simple?
- Are variants meaningful?
- Are all important states covered?
- Is accessibility built in?
- Does it follow the design system?
- Is the component performant?
- Does it avoid unnecessary client JavaScript?
- Can another developer understand it quickly?
- Does it reduce duplication rather than add abstraction?
- Is it visually polished?
- Is this something I'd be proud to ship?
