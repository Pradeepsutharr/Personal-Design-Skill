# Forms Example

Use this example when designing or reviewing authentication, onboarding, settings, checkout, admin, or data-entry forms.

## Recommended Structure

```text
Form Container
  ├─ Context / Breadcrumb (optional)
  ├─ Title
  ├─ Short explanation
  ├─ Field Group
  │   ├─ Label
  │   ├─ Input
  │   ├─ Helper text (optional)
  │   └─ Error (when needed)
  ├─ Additional Field Groups
  ├─ Supporting / Consent Content
  └─ Primary Action
```

## Example

```text
Create marina

Add the basic information needed to start managing this marina.

Marina name *
[ Marina name                         ]

Location *
[ Search location                    ]

Contact email *
[ name@company.com                   ]

Description
[ Describe the marina...             ]
[                                     ]

                         [Cancel] [Create marina]
```

## Field Design

Every field should answer:

- What information is required?
- Why is it required?
- What format should be used?

Use visible labels rather than relying on placeholders.

## Form Layout

Use grouping to reduce cognitive load.

For longer forms:

```text
Basic information
-----------------
Name
Location
Contact

Operational information
----------------------
Capacity
Operating hours
Berth configuration

Actions
-------
[Cancel] [Save changes]
```

Do not create unnecessary multi-step forms for short tasks.

## Validation

Validation should be helpful rather than hostile.

Example:

```text
Email address *
[ hello@                    ]

Enter a valid work email address.
```

Avoid showing errors before the user has meaningfully interacted with the field unless immediate validation is genuinely useful.

## Submission State

Example:

```text
[Saving...]
```

The application should:

- Prevent accidental duplicate submission.
- Preserve entered data.
- Communicate progress.
- Restore an actionable state after completion or failure.

## Success State

Example:

```text
Marina created successfully.

You can now configure berths and start accepting bookings.

[View marina]
```

## Error State

Example:

```text
We couldn't create the marina.

Check your connection and try again.

[Try again]
```

Do not expose raw API, database, or stack-trace errors.

## Destructive Form Actions

For destructive actions:

```text
Delete marina?

This permanently removes the marina and its associated data.

[Cancel] [Delete marina]
```

Make consequences clear before irreversible actions.

## Mobile Strategy

On mobile:

- Use a single-column layout for most forms.
- Keep touch targets comfortable.
- Use correct mobile input types.
- Keep the primary action accessible.
- Avoid tiny inline controls.
- Preserve clear section hierarchy.

## Accessibility

Ensure:

- Every input has a programmatic label.
- Required fields are communicated.
- Errors are associated with the relevant fields.
- Keyboard navigation works.
- Focus states are visible.
- Buttons have meaningful names.
- Validation is understandable by assistive technologies.

## Performance

- Avoid expensive validation on every keystroke unless necessary.
- Keep rerenders localized.
- Do not load large libraries for simple fields.
- Lazy-load heavy widgets such as rich editors or maps when appropriate.

## Visual Direction

Premium forms should feel calm and precise.

Use:

- Strong label hierarchy
- Consistent input heights
- Refined borders
- Clear focus states
- Balanced whitespace
- Subtle surfaces
- Clear primary CTA

Avoid:

- Excessive card nesting
- Heavy shadows around every field
- Giant input controls without reason
- Unnecessary decorative elements

## Review Questions

- Is every field necessary?
- Is the form easy to scan?
- Can spacing be improved?
- Can typography be improved?
- Is validation clear?
- Are loading, success, and error states polished?
- Is the UI consistent?
- Is the component reusable?
- Is the code optimized?
- Is accessibility handled?
- Is the form mobile-friendly?
- Does the experience feel premium?
- Is this something I'd be proud to ship?
