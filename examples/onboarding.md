# Onboarding Example

Use this example for product setup, workspace creation, profile completion, and guided first-use experiences.

## Goal

Help users reach their first meaningful outcome quickly.

## Principles

- Ask only what is necessary.
- Explain why information is needed when useful.
- Show progress for multi-step flows.
- Allow users to skip non-essential steps.
- Preserve entered data.
- Make the next action obvious.

## Recommended Structure

```text
Welcome
  ↓
Essential setup
  ↓
Preferences / configuration
  ↓
Optional personalization
  ↓
First meaningful outcome
```

## Step Design

Each step should have:

- Clear title
- Short explanation
- Focused task
- Primary action
- Secondary/skip action when appropriate

Avoid combining unrelated questions into one step.

## Progress

For multi-step onboarding, communicate progress.

Examples:

```text
Step 2 of 4
```

or

```text
● ● ○ ○
```

Do not use progress indicators that imply precision you cannot provide.

## First Value

Optimize onboarding around the first meaningful outcome, not profile completion.

For example:

- Create first project
- Import first dataset
- Configure first marina
- Invite first teammate

## Forms

Keep onboarding forms short.

If additional information can be collected later without harming the experience, defer it.

## Skip Behavior

Optional steps should be clearly skippable.

Do not disguise `Skip` as a low-contrast link if users genuinely need the choice.

## Loading

When setup triggers server work, communicate the operation:

```text
Setting up your workspace...
```

Do not leave users staring at a disabled button without explanation.

## Error Recovery

If setup fails:

- Preserve entered data.
- Explain what failed.
- Provide a retry action.
- Allow users to continue when safe.

## Responsive Strategy

### Desktop

A centered flow or split-screen composition can work well.

### Mobile

Use a single-column layout, comfortable inputs, and reachable primary actions.

Avoid unnecessary decorative content that pushes the task below the fold.

## Accessibility

Ensure:

- Step headings are semantic.
- Progress is understandable to assistive technologies.
- Focus moves appropriately between steps.
- Form fields are labeled.
- Errors are associated with their fields.
- Keyboard navigation works.

## Performance

- Keep the initial onboarding bundle small.
- Lazy-load optional setup tools.
- Avoid loading the entire application before it is needed.
- Optimize illustrations and media.

## Premium Visual Direction

Premium onboarding should feel welcoming and focused.

Use:

- Strong typography
- Clear progress
- Refined surfaces
- Subtle illustration/product visuals
- Purposeful motion
- Generous but controlled spacing

Avoid excessive confetti, animations, or decorative steps that slow the task.

## Review Questions

- Does the user reach value quickly?
- Is every question necessary?
- Can spacing be improved?
- Can typography be improved?
- Is the UI consistent?
- Is the component reusable?
- Is the code optimized?
- Will Lighthouse score well?
- Is accessibility handled?
- Does the flow work on mobile?
- Are loading and error states polished?
- Is this something I'd be proud to ship?
