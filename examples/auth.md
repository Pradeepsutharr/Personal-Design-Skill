# Authentication UI Example

Use this example for sign-in, sign-up, password reset, verification, and account recovery flows.

## Recommended Structure

```text
Authentication Shell
├── Brand / logo
├── Context heading
├── Supporting copy
├── Form
│   ├── Fields
│   ├── Recovery / secondary links
│   └── Primary action
├── Alternative authentication (optional)
├── Legal / consent copy
└── Help / navigation
```

## Sign-In Example

```text
Welcome back
Sign in to continue to your account.

Email
[ you@example.com ]

Password
[ ••••••••••• ]       Forgot password?

[ Sign in ]

──────── or ────────

[ Continue with Google ]

Don't have an account? Sign up
```

## Sign-Up

Ask only for information needed to create the account.

Avoid long registration forms when the product can collect additional information later through onboarding.

## Password Rules

Make requirements visible when useful.

Do not make users guess why a password failed validation.

## Validation

Errors should:

- Explain the problem.
- Stay close to the relevant field.
- Preserve valid input.
- Avoid revealing sensitive account information.

For account recovery, avoid messages that expose whether an email address exists when that would create a security risk.

## Loading State

Use clear feedback:

```text
[Signing in...]
```

Prevent duplicate submissions without making the form feel frozen.

## Error State

Use calm, actionable messages.

Example:

`We couldn't sign you in. Check your email and password and try again.`

Do not expose stack traces or backend implementation details.

## Success / Redirect

After successful authentication:

- Provide clear feedback when useful.
- Redirect to the expected destination.
- Preserve intended navigation context where appropriate.

## Responsive Strategy

### Desktop

A centered authentication card or split-screen composition can work well.

### Mobile

Prioritize the form and reduce decorative content.

Avoid requiring excessive scrolling for simple authentication.

## Premium Visual Direction

Authentication screens can feel premium through:

- Strong typography
- Clean form hierarchy
- Refined surfaces
- Subtle brand imagery
- Controlled gradients
- Fine borders
- Restrained motion

Do not let decorative visuals compete with the form.

## Accessibility

Ensure:

- Labels are programmatically associated with fields.
- Password controls have appropriate accessible names.
- Errors are announced appropriately.
- Keyboard navigation works.
- Focus is visible.
- Contrast is sufficient.
- Autofill and password-manager behavior is not unnecessarily blocked.

## Performance

Authentication should be lightweight.

- Avoid heavy visual libraries.
- Optimize background imagery.
- Keep client-side JavaScript minimal.
- Do not load application dashboards before authentication is complete.

## SEO

Authentication pages are usually not intended for search indexing. Follow the application's indexing strategy rather than adding unnecessary SEO content.

## Review Questions

- Is the authentication task immediately clear?
- Is the form simple?
- Can spacing be improved?
- Can typography be improved?
- Is the UI consistent?
- Are validation and errors clear?
- Is the component reusable?
- Is the code optimized?
- Is accessibility handled?
- Does it work well on mobile?
- Does the page feel trustworthy and premium?
- Is this something I'd be proud to ship?
