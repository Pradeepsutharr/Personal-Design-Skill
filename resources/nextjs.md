# Next.js Standards

## Purpose

Use modern Next.js architecture to build fast, maintainable, SEO-friendly, and scalable applications. The skill should prefer framework capabilities over unnecessary client-side work.

## App Router First

For modern projects, prefer the App Router unless the existing project explicitly uses the Pages Router or migration is outside the requested scope.

Respect the architecture already present in the repository. Do not rewrite routing structure unnecessarily.

## Server Components by Default

Prefer Server Components for:

- Static content
- Data fetching that does not require browser APIs
- SEO-critical page content
- Layouts
- Navigation structures that do not require client state
- Content rendering

Use Client Components when the UI genuinely requires:

- Browser APIs
- Event handlers
- Local interactive state
- Effects
- Client-only libraries
- Real-time browser interactions

Keep client boundaries as small as practical.

## Avoid Client Component Creep

Do not add `"use client"` to an entire page merely because one small section is interactive.

Instead:

1. Keep the page/server structure on the server.
2. Extract the interactive portion into a Client Component.
3. Pass serializable data into it where appropriate.

## Data Fetching

Prefer server-side data fetching when the data does not need to be fetched in the browser.

Avoid unnecessary request waterfalls.

When requests are independent, structure the implementation so they can execute concurrently where practical.

Do not fetch data on the client merely because it is familiar if server rendering provides a better architecture.

## Loading UI

Use route and component loading patterns intentionally.

Provide useful loading states for operations that can take noticeable time.

Avoid replacing an entire page with a spinner when only one section is loading.

Use skeleton layouts when the final structure is predictable.

## Error Handling

Design error boundaries and fallbacks intentionally.

- Keep errors localized where possible.
- Provide actionable recovery.
- Avoid exposing internal implementation details.
- Preserve unaffected page functionality.

## Metadata

Use Next.js metadata capabilities for public pages.

Prefer server-side metadata generation rather than client-side document manipulation.

For dynamic routes, generate metadata from the same source of truth used by the page when appropriate.

Ensure:

- Unique titles
- Useful descriptions
- Appropriate Open Graph metadata
- Canonical strategy where relevant

## Images

Use Next.js image capabilities when appropriate.

- Provide meaningful dimensions or layout information.
- Avoid oversized images.
- Use responsive sizing.
- Prioritize important above-the-fold imagery carefully.
- Lazy-load non-critical imagery when appropriate.

Do not blindly mark every image as priority.

## Fonts

Use the project's font optimization strategy.

Avoid loading many font families or weights unnecessarily.

Typography decisions must balance visual quality and performance.

## Dynamic Imports

Use dynamic imports for heavy functionality when it materially reduces initial client cost.

Good candidates can include:

- Maps
- Editors
- PDF viewers
- Advanced charts
- Large visualization libraries
- Rarely used admin tools

Do not use dynamic imports everywhere. Extra complexity without performance benefit is harmful.

## Suspense

Use Suspense when progressive rendering or isolated asynchronous UI provides a meaningful user experience improvement.

Do not wrap every component in Suspense without a clear reason.

## Routing

Keep route structures predictable.

Use route groups, layouts, loading, error, and not-found conventions where they improve architecture.

Avoid deep nesting solely for organizational convenience when a simpler route structure is clearer.

## Layouts

Use shared layouts for persistent UI such as:

- Navigation
- Sidebars
- Application shells
- Shared headers

Avoid duplicating persistent layout code across pages.

## API and Server Logic

Keep server-only logic on the server.

Do not expose secrets or private configuration to the browser.

Use environment variables appropriately and expose only intentionally public variables.

## Caching and Revalidation

Choose caching and revalidation behavior based on data freshness requirements.

Ask:

- Can this data be cached?
- How frequently does it change?
- Can stale data be acceptable?
- Does the user need immediate consistency?

Do not disable caching globally without understanding the consequences.

## SEO Architecture

Public pages should remain crawlable and semantically structured.

Do not move important SEO content into unnecessary client-only rendering.

Consider:

- Metadata
- Sitemap
- Robots configuration
- Canonicals
- Structured data
- Semantic headings
- Internal linking

## Accessibility

Use semantic HTML and preserve accessibility through server/client boundaries.

Client-side interaction must not remove keyboard access, focus behavior, labels, or meaningful structure.

## State Management

Do not introduce global state for data that can remain local.

Choose state based on scope:

- Component state for local UI behavior
- URL state for shareable filters and navigation state
- Server data/cache for remote resources
- Global state only for genuinely cross-cutting client state

## Performance

For every page ask:

- Does this need to be a Client Component?
- Can this data be fetched on the server?
- Can this library be lazy-loaded?
- Are images optimized?
- Are fonts optimized?
- Is the initial JavaScript bundle reasonable?
- Are request waterfalls avoided?
- Is layout stable?

## Avoid Unnecessary Rewrites

When modifying an existing application:

- Preserve working architecture.
- Follow existing conventions when they are sound.
- Change only what the task requires.
- Avoid replacing libraries without a clear benefit.
- Avoid broad refactors during focused UI tasks.

## Production Review

Before shipping a Next.js implementation, verify:

- Server/client boundaries are intentional.
- SEO content is crawlable.
- Metadata is complete.
- Images are optimized.
- Fonts are optimized.
- Heavy code is split when useful.
- Loading and error states exist where needed.
- Accessibility works across responsive layouts.
- Secrets remain server-side.
- Performance decisions are evidence-based.
- The code is maintainable and consistent with the project architecture.
