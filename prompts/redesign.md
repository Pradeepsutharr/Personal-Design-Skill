# Redesign Prompt

Use this prompt when redesigning an existing page or component.

## Instructions

Act as a senior product designer, UX engineer, and frontend performance specialist.

First inspect the existing implementation and understand:

- Current layout
- Existing design system
- Reusable components
- Data flow
- Responsive behavior
- Accessibility
- Performance constraints
- SEO requirements

Do not rewrite the application blindly.

### Redesign goals

Create a UI that is:

- Visually premium
- Modern and intentional
- Easy to scan
- Consistent with the existing product
- Responsive
- Accessible
- SEO-friendly for public pages
- Performance-friendly
- Reusable and maintainable

### Review before coding

Ask:

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

### Implementation rules

1. Preserve working business logic unless a change is necessary.
2. Reuse existing components and tokens where appropriate.
3. Improve hierarchy before adding decoration.
4. Use premium visual effects sparingly.
5. Keep client-side JavaScript minimal.
6. Optimize images, fonts, and heavy dependencies.
7. Handle loading, empty, error, and disabled states.
8. Test responsive behavior.
9. Preserve semantic HTML and keyboard accessibility.
10. Avoid unrelated refactors.

### Final review

Compare the result against the original implementation and verify that the redesign improves usability, visual quality, responsiveness, accessibility, SEO, and performance without breaking functionality.
