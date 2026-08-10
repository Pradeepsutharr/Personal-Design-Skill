# Content Design Standards

## Purpose

Content is part of the interface. Clear copy improves usability, conversion, accessibility, SEO, and perceived product quality.

## Core Principle

Write for the user's task, not for the interface's implementation.

Every important piece of UI copy should answer a useful question or guide a useful action.

## Clarity First

Prefer:

- Short sentences
- Familiar words
- Specific labels
- Active voice
- Concrete actions

Avoid unnecessary jargon, vague marketing language, and technical terminology when the audience does not need it.

## Headlines

Headlines should communicate the main idea quickly.

For product pages, prefer outcome-oriented language over generic claims.

Weak:

`Powerful solutions for modern businesses`

Stronger:

`Manage your marina operations from one platform`

## Supporting Copy

Supporting text should add context rather than repeat the headline.

Use it to explain:

- What the product does
- Who it is for
- Why it matters
- What happens next

## Buttons and CTAs

CTA labels should describe the action or outcome.

Prefer:

- `Start free`
- `Book a demo`
- `Create project`
- `Save changes`
- `View pricing`

Avoid vague labels when a specific action is possible.

## Navigation Labels

Navigation labels should be:

- Short
- Familiar
- Consistent
- Predictable

Use the same term for the same concept throughout the application.

Do not call something `Bookings` in one place and `Reservations` in another unless they intentionally represent different concepts.

## Form Copy

Field labels should tell users exactly what information is required.

Helper text should explain why or how when useful.

Error text should explain:

- What went wrong
- How to fix it

Avoid technical error messages such as raw API or database errors.

## Empty States

An empty state should explain the situation and the next step.

Structure:

**Context → Explanation → Action**

Example:

`No marinas yet`

`Add your first marina to start managing berths and bookings.`

`Add marina`

## Loading Copy

When an operation takes time, communicate what is happening.

Prefer:

- `Loading bookings`
- `Saving changes`
- `Generating report`

Avoid vague messages such as `Please wait` when a more informative message is possible.

## Error Copy

Error messages should be calm, specific, and actionable.

Avoid:

`Something went wrong.`

when the application can explain the actual issue.

Better:

`We couldn't save the booking. Check your connection and try again.`

Do not expose stack traces, internal IDs, database errors, or implementation details to end users.

## Confirmation Copy

For destructive or irreversible actions, communicate the consequence clearly.

Example:

`Delete marina?`

`This will permanently remove the marina and its associated data.`

`Cancel` / `Delete marina`

## Tooltips

Tooltips should explain unfamiliar controls, not repeat visible labels.

Do not hide essential instructions exclusively inside tooltips.

## Accessibility and Content

Accessible content should remain understandable without visual styling.

Avoid:

- Meaning communicated only through color
- Icon-only meaning without labels
- Ambiguous link text
- Overly complex sentences

Use descriptive text for important actions.

## SEO Content

SEO copy should remain useful to humans.

Do not:

- Stuff keywords
- Repeat the same phrase unnaturally
- Create thin sections solely for search engines
- Hide keyword-heavy text from users

Use headings and supporting content to establish real topical relevance.

## Conversion Copy

Conversion-oriented copy should communicate value and reduce uncertainty.

Good conversion copy can answer:

- What do I get?
- How quickly can I start?
- Why should I trust this?
- What happens after I click?

Avoid manipulative urgency or misleading claims.

## Enterprise Product Copy

Enterprise interfaces benefit from precise language.

Use terminology that reflects real business workflows.

Avoid overly playful language when it makes operational tasks less clear.

## Consistency

Create a product vocabulary.

Maintain consistency for:

- Actions
- Statuses
- Roles
- Objects
- Navigation
- Notifications
- Error states

A consistent vocabulary reduces cognitive load.

## Content Density

Do not remove useful information simply to make a design look minimal.

Instead:

- Improve hierarchy.
- Group related information.
- Use progressive disclosure.
- Rewrite unnecessary copy.
- Remove repetition.

## Content Review

Before shipping, ask:

- Is the copy clear?
- Is the action obvious?
- Can the text be shorter without losing meaning?
- Are labels consistent?
- Are errors actionable?
- Are empty states useful?
- Is the copy accessible?
- Is important SEO content natural and useful?
- Does the wording support conversion without being manipulative?
- Does the interface feel professional and premium?
