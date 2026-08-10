# Form UX Standards

## Purpose

Forms should feel simple, predictable, accessible, and trustworthy. A good form minimizes cognitive load while collecting exactly the information required.

## Core Principle

Every field should have a clear reason to exist.

Before adding a field, ask:

- Is it necessary?
- Can the value be inferred?
- Can it be collected later?
- Can multiple fields be combined without reducing clarity?

## Form Structure

Organize fields into logical groups.

Typical structure:

1. Section heading
2. Short explanation when needed
3. Related fields
4. Supporting information
5. Primary action

Avoid presenting a long wall of unrelated inputs.

## Labels

Every input must have a clear label.

Labels should:

- Describe what the user should enter.
- Remain visible when the field contains a value.
- Use consistent terminology across the product.

Do not rely on placeholders as labels.

## Placeholder Text

Use placeholders only as examples or formatting guidance.

Good:

`name@company.com`

Avoid:

`Enter your email`

when the field already has a visible label.

## Required Fields

Clearly communicate required and optional fields.

If most fields are required, consider marking only optional fields to reduce visual noise.

Do not make users guess which fields are mandatory.

## Input Types

Use the correct input type where appropriate.

Examples:

- Email → `type="email"`
- Password → `type="password"`
- Telephone → appropriate telephone input
- Number → appropriate numeric input
- Date → suitable date control

Correct input types improve mobile keyboards and accessibility.

## Input Width

Input width should communicate expected content length.

Examples:

- Short code → narrow field
- Email → medium/wide field
- Address → wider field
- Long description → textarea

Do not make every input full width by default if it harms scanning.

## Field Grouping

Group fields that belong together.

Examples:

- First name + last name
- City + state + postal code
- Billing details
- Account security

Use spacing and headings to establish relationships.

## Validation

Validate at the appropriate time.

Prefer:

- Immediate validation for simple local constraints when helpful.
- Validation on blur for many field-level errors.
- Submission validation as the final safeguard.

Do not aggressively display errors before the user has had a reasonable chance to complete the field.

## Error Messages

An error message should answer:

1. What went wrong?
2. Where did it happen?
3. How can the user fix it?

Bad:

`Invalid input.`

Better:

`Enter a valid work email address.`

Avoid blaming the user.

## Error Placement

Keep errors close to the affected field.

For large forms, also provide a summary when multiple fields fail, with links to the relevant fields when appropriate.

## Success Feedback

After successful submission:

- Confirm the action.
- Explain what happened.
- Tell the user what they can do next when relevant.

Do not rely only on a disappearing toast for important state changes.

## Loading States

During submission:

- Prevent accidental duplicate submissions.
- Show clear progress.
- Preserve entered values.
- Keep the user informed.

Button labels can communicate state, such as `Saving...`.

Do not disable the entire page unless the operation truly blocks further interaction.

## Buttons

The primary action should be obvious.

Examples:

- `Create account`
- `Save changes`
- `Create marina`
- `Send invitation`

Avoid vague labels such as `Continue` when a more descriptive action is possible.

## Destructive Actions

For destructive operations:

- Make the consequence clear.
- Use destructive styling appropriately.
- Require confirmation when the action is irreversible or high impact.
- Do not hide the destructive action so deeply that users cannot understand the workflow.

## Multi-Step Forms

Use multi-step forms when the complete form is genuinely complex.

Each step should have:

- Clear title
- Clear progress indication
- Focused task
- Back/next controls
- Validation appropriate to the step

Avoid splitting a simple form into many steps merely to make it look sophisticated.

## Accessibility

Forms must support:

- Keyboard navigation
- Visible focus
- Programmatic labels
- Accessible errors
- Appropriate descriptions
- Screen-reader understanding

Use native form elements whenever practical.

## Mobile Forms

On small screens:

- Use comfortable touch targets.
- Avoid overly dense two-column layouts.
- Use appropriate mobile input types.
- Keep important actions reachable.
- Avoid excessive scrolling caused by unnecessary sections.

## Autofill

Use appropriate autocomplete attributes where they improve speed and accuracy.

Examples include:

- `email`
- `name`
- `given-name`
- `family-name`
- `street-address`
- `postal-code`

## Performance

Forms should remain responsive.

Avoid:

- Heavy validation on every keystroke without need.
- Unnecessary global rerenders.
- Expensive formatting for simple inputs.
- Large client libraries for tiny forms.

## Form Review

Before shipping, ask:

- Is every field necessary?
- Is the purpose of each field obvious?
- Are labels clear?
- Can the form be completed quickly?
- Is validation helpful rather than frustrating?
- Are errors actionable?
- Are loading and success states clear?
- Is the primary action obvious?
- Is keyboard navigation correct?
- Are focus states visible?
- Is the form responsive?
- Is the implementation reusable and maintainable?
- Is the form visually premium?
