# Visual Effects Standards

## Purpose

Visual effects should make the product feel polished, modern, and premium without damaging usability, accessibility, performance, or content clarity.

## Core Principle

Use visual effects as supporting layers. Never let effects become the product.

Every effect should answer at least one question:

- Does it improve hierarchy?
- Does it communicate depth?
- Does it reinforce brand identity?
- Does it improve interaction feedback?
- Does it make a key moment more memorable?

If the answer is no, remove it.

## Premium Visual Language

A premium interface usually relies on:

- Strong typography
- Precise spacing
- Refined surfaces
- Consistent radii
- Subtle borders
- Controlled shadows
- Purposeful accent color
- High-quality product visuals
- Restrained motion

Do not attempt to create premium quality by adding more effects.

## Shadows

Use shadows to establish hierarchy and elevation.

Prefer subtle, layered shadows over extremely dark or large shadows.

Use elevation consistently:

- Base surface → little or no shadow
- Raised card → subtle elevation
- Popover/dialog → stronger elevation
- Floating navigation → distinct but controlled elevation

Do not add shadows to every component.

## Border Radius

Use a consistent radius system.

Possible hierarchy:

- Small controls: small radius
- Cards: medium radius
- Large surfaces: larger radius
- Pills: full radius

Do not mix unrelated radii across components without a design reason.

## Gradients

Gradients should be intentional.

Good uses:

- Hero backgrounds
- Brand atmosphere
- Subtle highlights
- Large feature surfaces
- Focused visual accents

Avoid:

- Gradient on every card
- Multiple unrelated gradients on one screen
- Extremely saturated backgrounds behind text
- Generic purple/blue gradients added without brand purpose

## Glow Effects

Glow can create depth and premium atmosphere.

Use it sparingly around:

- Primary product visuals
- Important CTAs
- Hero backgrounds
- Focused accent elements

Keep glow behind or around content rather than reducing text readability.

## Glassmorphism

Glass effects can be useful for selected floating surfaces.

When using glass:

- Ensure sufficient contrast.
- Use a fallback surface.
- Keep blur areas limited.
- Avoid making every card translucent.
- Verify performance on lower-powered devices.

## Blur

Use blur for atmosphere or layered surfaces, not as a substitute for hierarchy.

Avoid large numbers of heavily blurred elements because they can increase rendering cost.

## Background Effects

Background visuals may include:

- Subtle gradients
- Radial glows
- Grid patterns
- Noise textures
- Abstract shapes
- Soft lighting

They should remain subordinate to foreground content.

Do not make background effects so strong that they compete with headings, controls, or product UI.

## Decorative Shapes

Decorative shapes should have a clear visual purpose.

Prefer a small number of intentional elements over dozens of floating objects.

Avoid decorative elements that:

- Distract from CTAs
- Cause layout shifts
- Increase DOM complexity unnecessarily
- Reduce contrast
- Make responsive layouts fragile

## Product Visuals

For SaaS products, authentic product UI is usually more valuable than generic decoration.

Use:

- Realistic data
- Clear hierarchy
- Meaningful charts
- Relevant workflows
- Consistent product styling

Do not fill product mockups with meaningless placeholder content solely for visual appeal.

## Hover Effects

Hover effects should communicate interactivity.

Appropriate effects include:

- Slight elevation
- Border emphasis
- Background change
- Small icon translation
- Subtle scale

Avoid dramatic scaling that causes nearby elements to shift.

## Cursor Effects

Custom cursor effects should be rare and optional.

Never make a cursor effect necessary for navigation or understanding the interface.

Avoid custom cursors in dense enterprise applications unless they provide genuine interaction value.

## Noise and Texture

Subtle noise can reduce overly sterile surfaces.

Use it carefully and ensure it does not reduce text clarity or create unnecessary image payloads.

CSS-generated effects can be preferable to large texture assets when they provide equivalent visual quality at lower cost.

## Decorative Animation

Decorative motion should remain subtle.

Examples:

- Slow background glow movement
- Very subtle gradient movement
- Gentle entrance transitions
- Small hover transformations

Do not use continuous animation across many elements.

## Performance

Visual effects must respect performance budgets.

Be cautious with:

- Large blur regions
- Multiple box shadows
- Heavy filters
- Continuous animations
- Large background images
- Excessive DOM decorations

Prefer efficient CSS and compositing-friendly properties where possible.

## Accessibility

Effects must not reduce accessibility.

Check:

- Text contrast
- Focus visibility
- Reduced motion
- Keyboard usability
- Readability over backgrounds

Decorative effects should disappear or reduce appropriately for users who prefer reduced motion.

## Responsive Effects

Effects that look good on desktop may be excessive on mobile.

Reduce or remove:

- Large decorative shapes
- Heavy blur
- Excessive parallax
- Continuous background animation

on lower-powered or smaller devices when appropriate.

## Visual Consistency

Use a coherent visual language.

Do not combine:

- Heavy glassmorphism
- Strong neumorphism
- Flat design
- Skeuomorphic effects

randomly within the same interface.

Choose a visual direction and apply it consistently.

## Effects Review

Before shipping, ask:

- Is this effect actually improving the experience?
- Does it make the interface more premium or merely busier?
- Does it preserve readability?
- Does it support hierarchy?
- Is it consistent with the design system?
- Does it perform well on mobile and lower-powered devices?
- Does reduced motion work?
- Does it introduce layout instability?
- Could the same result be achieved more simply?
- Is the interface still excellent with decorative effects removed?
- Is this something I'd be proud to ship?
