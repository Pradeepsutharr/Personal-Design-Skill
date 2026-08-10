# Mobile UI Example

Use this example when adapting a desktop experience for mobile.

## Principle

Mobile is not a scaled-down desktop. Reprioritize the experience around the primary mobile task.

## Recommended Structure

```text
Mobile Header
  ├─ Context
  ├─ Navigation
  └─ Essential action

Primary Content
  ├─ Page title
  ├─ Important information
  └─ Primary action

Secondary Content

Sticky action (only when genuinely useful)
```

## Navigation

Use simple patterns:

- Menu drawer
- Bottom navigation for a small set of primary destinations
- Contextual navigation

Do not hide essential tasks behind deep menus.

## Touch

Controls should be comfortable to tap and have enough separation to prevent accidental activation.

Avoid tightly packed icon-only actions.

## Forms

Prefer a single-column layout for most forms.

Use:

- Visible labels
- Appropriate input types
- Comfortable controls
- Clear validation
- Reachable primary actions

## Tables

Choose intentionally between:

- Horizontal scrolling
- Priority columns
- Stacked record cards
- Detail drawer/page

Do not squeeze a desktop table into a narrow screen.

## Content Priority

Keep:

1. Page context
2. Primary task
3. Primary action
4. Critical information
5. Secondary information

Move or collapse lower-priority content.

## Responsive Typography

Reduce display sizes where necessary while preserving hierarchy and readability.

Check heading wrapping and button labels with realistic content.

## Performance

Mobile performance is especially important.

- Optimize images.
- Minimize JavaScript.
- Lazy-load non-critical media.
- Avoid heavy animation.
- Keep initial rendering lightweight.

## Accessibility

Check:

- Keyboard support where applicable
- Screen readers
- Focus states
- Text scaling
- Contrast
- Touch target comfort
- Reduced motion

## Premium Visual Direction

Premium mobile UI comes from precision rather than decoration:

- Clean spacing
- Strong typography
- Refined surfaces
- Consistent controls
- Clear hierarchy
- Subtle interactions

## Review Questions

- Is the primary task obvious?
- Is the UI intentionally mobile-first?
- Can spacing be improved?
- Can typography be improved?
- Is the UI consistent?
- Are touch targets comfortable?
- Is the component reusable?
- Is the code optimized?
- Will Lighthouse score well?
- Is accessibility handled?
- Is this something I'd be proud to ship?
