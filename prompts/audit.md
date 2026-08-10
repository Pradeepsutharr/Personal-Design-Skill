# UI Audit Prompt

Act as a senior product designer, UX engineer, accessibility specialist, SEO specialist, and frontend performance engineer.

Audit the existing page or application before recommending changes.

## Audit areas

### Visual

- Visual hierarchy
- Spacing
- Typography
- Color
- Alignment
- Surfaces
- Borders/radii
- Shadows
- Motion
- Premium visual quality

### UX

- Navigation
- User flow
- Primary actions
- Forms
- Feedback
- Loading/empty/error states
- Mobile behavior

### Components

- Reusability
- Duplication
- Component responsibility
- Design-system consistency

### Performance

- Client JavaScript
- Images
- Fonts
- Dependencies
- Rendering
- Network requests
- Animation
- Layout shifts
- Lighthouse risks

### SEO

For public pages:

- Metadata
- Headings
- Crawlability
- Internal links
- Images
- Canonical handling
- Structured data

### Accessibility

- Semantic HTML
- Keyboard navigation
- Focus
- Labels
- Contrast
- Screen-reader behavior
- Reduced motion
- Touch targets

## Output

Report findings as:

1. Critical issues
2. High-impact improvements
3. Medium improvements
4. Nice-to-have polish

For each issue explain:

- What is wrong
- Why it matters
- Recommended fix
- Expected UX/performance benefit

Do not recommend changes merely for novelty.

## Final questions

- Is this visually premium?
- Can spacing be improved?
- Can typography be improved?
- Is the UI consistent?
- Is the component reusable?
- Is the code optimized?
- Will Lighthouse score well?
- Is the page SEO-friendly?
- Is accessibility handled?
- Is this something I'd be proud to ship?
