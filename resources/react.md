# React Standards

## Purpose

Use React to build interfaces that are reusable, predictable, accessible, performant, and easy to maintain.

## Component Design

A component should have a clear responsibility.

Prefer components that:

- Do one meaningful job.
- Have predictable inputs.
- Are easy to compose.
- Keep implementation details local.
- Can be reused without hidden dependencies.

Avoid enormous components containing unrelated UI, data fetching, state management, and formatting logic when those responsibilities can be separated cleanly.

## Component Boundaries

Split components when:

- A section has independent state.
- A section is reused.
- A component has multiple unrelated responsibilities.
- A large render tree is difficult to reason about.
- A client-only section can be isolated from server-rendered content.

Do not split every small element into a separate file. Abstraction should improve clarity, not create ceremony.

## Props

Keep props intentional and understandable.

Prefer:

- Explicit props for important behavior.
- Composition for flexible content.
- Sensible defaults.
- Stable APIs for reusable components.

Avoid passing large objects when a component only needs a few fields.

## State

Choose the smallest state scope that solves the problem.

Use local state for local UI behavior.

Use shared state only when multiple areas genuinely need the same changing value.

Do not create global state merely to avoid passing one or two props.

## Derived State

Avoid storing values that can be calculated from existing state or props.

Prefer deriving values during render when the calculation is inexpensive.

Use memoization only when there is meaningful computational or rendering benefit.

## Effects

Effects should synchronize React with an external system, such as:

- Browser APIs
- Subscriptions
- Timers
- External widgets
- Non-React systems

Do not use effects as a default mechanism for deriving ordinary UI state.

## Event Handlers

Keep event handlers focused on user actions.

Avoid putting large business workflows directly inside JSX event attributes. Extract meaningful logic when it improves readability and testing.

## Rendering

Keep render logic predictable.

Avoid:

- Side effects during render
- Expensive calculations repeated unnecessarily
- Creating unnecessary large objects or arrays
- Deeply nested conditional JSX that becomes difficult to understand

## Keys

Use stable, unique keys for lists.

Do not use array indexes as keys when items can be reordered, inserted, removed, or otherwise change identity.

## Conditional Rendering

Make important states explicit.

Prefer clear branches for:

- Loading
- Error
- Empty
- Success
- Data available

Do not hide important behavior inside clever one-line expressions when clarity suffers.

## Forms

Controlled and uncontrolled patterns should be chosen based on the application's needs.

For complex production forms, use established form libraries when they reduce complexity and improve validation, accessibility, and maintainability.

Do not introduce a form library for a tiny form that can be cleanly handled with native React patterns.

## Lists

For large lists:

- Paginate or virtualize where appropriate.
- Avoid rendering unnecessary items.
- Keep row components efficient.
- Avoid expensive work for every row on every render.

## Memoization

Do not use `useMemo` and `useCallback` everywhere by default.

Use memoization when it:

- Prevents meaningful expensive recalculation.
- Stabilizes a value required by a dependency relationship.
- Prevents meaningful child rerenders.

Measure or reason about the benefit rather than adding memoization automatically.

## Context

Use Context for values that are genuinely shared across a subtree.

Avoid placing rapidly changing, high-frequency state into broad Context providers when it causes unnecessary rerenders.

Keep providers close to where their data is needed.

## Custom Hooks

Create a custom hook when logic is:

- Reused.
- Stateful and conceptually grouped.
- Complex enough to obscure a component.
- Useful as a domain-specific abstraction.

Do not create hooks solely to wrap one trivial expression.

## Accessibility

React components must preserve semantic HTML and keyboard behavior.

Prefer native controls before implementing custom interaction patterns.

Custom controls require careful handling of:

- Keyboard interaction
- Focus
- Accessible names
- States
- Screen readers

## Client Boundaries

In Next.js applications, keep interactive React components isolated when possible.

Do not turn a complete page into a Client Component simply because a small child needs client state.

## Performance

Ask:

- Does this component need client-side JavaScript?
- Can state be localized?
- Are renders unnecessarily broad?
- Are large lists optimized?
- Are expensive calculations controlled?
- Can heavy UI be lazy-loaded?

## Error and Loading States

Production components should account for asynchronous states where applicable.

Design:

- Loading
- Error
- Empty
- Success
- Disabled

Do not leave users staring at blank regions while data loads.

## Maintainability

Prefer boring, understandable code over clever abstractions.

A senior engineer should be able to understand the component quickly.

Avoid:

- Unnecessary indirection
- Giant conditional expressions
- Hidden side effects
- Duplicate state sources
- Premature abstraction

## React Review

Before shipping, ask:

- Is the component reusable where appropriate?
- Does it have one clear responsibility?
- Is state scoped correctly?
- Are effects actually necessary?
- Are keys stable?
- Are expensive renders controlled?
- Is accessibility preserved?
- Is the client boundary as small as possible?
- Is the code readable?
- Is this something I'd be proud to ship?
