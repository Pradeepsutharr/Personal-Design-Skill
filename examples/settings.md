# Settings Page Example

Use this example for account, profile, workspace, application, billing, notification, and preference settings.

## Recommended Structure

```text
Settings
├── Settings navigation
│   ├── Profile
│   ├── Security
│   ├── Notifications
│   ├── Preferences
│   └── Billing / Workspace (when relevant)
│
└── Content panel
    ├── Section heading
    ├── Explanation
    ├── Form fields
    └── Actions
```

## Organization

Group settings by user intent rather than implementation details.

Prefer:

- Profile
- Security
- Notifications
- Preferences
- Billing
- Team/workspace

Avoid a single page containing every setting unless the product is genuinely small.

## Page Header

Provide clear context:

```text
Profile
Manage your personal information and account details.
```

## Sections

Each section should have:

- Clear title
- Short explanation when useful
- Related controls
- Clear save behavior

Avoid excessive card nesting.

## Save Behavior

Choose a consistent pattern:

### Explicit save

Useful for grouped forms with multiple related changes.

```text
[Cancel] [Save changes]
```

### Immediate save

Useful for simple preferences such as toggles when the result is obvious.

If using immediate save, communicate success or failure without unnecessary interruption.

## Destructive Settings

Keep destructive actions separate from normal settings.

Example:

```text
Danger zone

Delete workspace
Permanently remove this workspace and its data.

[Delete workspace]
```

Use clear confirmation for irreversible operations.

## Security

Security-related actions should communicate consequences.

Examples:

- Change password
- Enable two-factor authentication
- Manage active sessions
- Revoke access

Do not hide security controls behind confusing navigation.

## Loading and Saving

Communicate state clearly:

```text
[Saving...]
```

Prevent accidental duplicate submissions while preserving the user's input.

## Error Handling

Keep errors close to the relevant setting.

Example:

```text
Unable to save notification preferences.
Please try again.

[Try again]
```

Avoid exposing raw server errors.

## Responsive Strategy

### Desktop

Use a settings navigation rail/sidebar with the active section clearly indicated.

### Mobile

Move settings navigation into a compact selector or stacked navigation before the active content.

Keep important save actions reachable.

## Accessibility

Ensure:

- Navigation has an accessible structure.
- Active settings section is communicated semantically.
- Inputs have labels.
- Switches have clear accessible names.
- Destructive actions are clearly identified.
- Keyboard navigation works.
- Focus states are visible.

## Performance

Settings pages generally should remain lightweight.

- Avoid loading unrelated application data.
- Lazy-load heavy settings such as rich editors or advanced visualizations.
- Keep interactive state localized.

## Visual Direction

Premium settings interfaces should feel calm, organized, and trustworthy.

Use:

- Strong section hierarchy
- Consistent form controls
- Subtle separators
- Restrained surfaces
- Clear action hierarchy
- Consistent spacing

Avoid excessive decoration because settings are task-oriented screens.

## Review Questions

- Can users find settings quickly?
- Is the information architecture clear?
- Can spacing be improved?
- Can typography be improved?
- Is the UI consistent?
- Are save behaviors understandable?
- Are destructive actions safe?
- Is the component reusable?
- Is the code optimized?
- Is accessibility handled?
- Does the layout work on mobile?
- Does the page feel premium without becoming distracting?
- Is this something I'd be proud to ship?
