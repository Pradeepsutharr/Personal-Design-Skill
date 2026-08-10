# Visual Hierarchy Standards

## Purpose

Visual hierarchy determines what users notice first, second, and third. Premium interfaces are not merely attractive; they make the intended reading order obvious.

## Core Principle

Every screen should have a clear visual priority.

Ask:

1. What should the user notice first?
2. What should they understand next?
3. What should they act on?
4. What information can remain secondary?

If everything looks equally important, the hierarchy has failed.

## Hierarchy Tools

Use a combination of:

- Size
- Weight
- Color
- Contrast
- Position
- Spacing
- Alignment
- Density
- Motion
- Surface elevation

Do not rely on one tool alone.

## Primary Focus

Each major section should have one dominant message or action.

Examples:

- Landing page → value proposition and CTA
- Dashboard → key business state
- Form → task completion
- Detail page → record identity and primary action
- Table → important dataset and available actions

## Scale

Larger elements attract attention first, but excessive size quickly reduces sophistication.

Use large typography for genuinely important messages, not as a substitute for strong content.

## Contrast

High contrast should communicate importance.

Use stronger contrast for:

- Primary headings
- Important values
- Primary actions
- Current navigation

Use softer contrast for:

- Supporting metadata
- Secondary descriptions
- Non-critical labels

Do not reduce contrast below accessible levels.

## Spacing as Hierarchy

Elements with small spacing feel related.

Elements with large spacing feel separate.

Use this intentionally instead of applying identical margins everywhere.

## Alignment

Alignment creates invisible structure.

Major elements should share consistent edges when they belong to the same layout system.

Check:

- Page titles
- Cards
- Inputs
- Tables
- Buttons
- Section content

Misalignment makes a design feel unfinished even when individual components look good.

## Visual Weight

Visual weight can come from:

- Size
- Darkness
- Saturation
- Density
- Borders
- Shadows
- Position

Balance these factors so one area does not accidentally dominate the screen.

## Above the Fold

Above-the-fold content should communicate the most important information quickly.

For marketing pages, prioritize:

- Product identity
- Value proposition
- Primary CTA
- Relevant visual proof

For applications, prioritize:

- Page context
- Current state
- Primary workflow action

Do not cram every important feature above the fold.

## Cards and Containers

Containers should support hierarchy rather than fragment the interface.

Avoid putting every small piece of information into a separate card.

Use cards when grouping information improves comprehension.

## CTA Hierarchy

Actions should have clear priority.

Typical order:

1. Primary
2. Secondary
3. Tertiary
4. Destructive/contextual

Avoid multiple competing primary actions in the same visual region.

## Typography Hierarchy

Use typography to establish:

- Page title
- Section title
- Subsection title
- Body
- Metadata
- Labels

A user should be able to scan the hierarchy without reading every sentence.

## Color Hierarchy

Reserve strong accent colors for meaningful actions and states.

If every heading, badge, card, and icon uses a bright accent, the interface loses focus.

## Motion and Hierarchy

Motion can attract attention, so use it carefully.

Do not animate multiple competing elements simultaneously.

Use motion to reinforce the intended focus rather than distract from it.

## Responsive Hierarchy

Hierarchy may need to change on smaller screens.

Examples:

- Secondary content can move below primary content.
- Navigation can collapse.
- Supporting metadata can become less prominent.
- Multi-column layouts can stack.

Do not preserve desktop visual priority blindly on mobile.

## Accessibility

Visual hierarchy must also exist semantically.

Use:

- Proper heading levels
- Semantic landmarks
- Accessible names
- Descriptive controls

Do not create a visual `h1` using a `div` merely because it looks right.

## Common Failures

Avoid:

- Everything bold
- Everything colorful
- Everything inside cards
- Giant headings with weak supporting content
- Too many competing CTAs
- Excessive shadows
- Excessive gradients
- Weak contrast for secondary information
- Random alignment
- Inconsistent spacing

## Hierarchy Review

Before shipping, ask:

- Is the first thing I see the right thing?
- Is the reading order obvious?
- Is the primary action obvious?
- Are secondary elements appropriately quiet?
- Can spacing communicate relationships better?
- Can typography communicate hierarchy better?
- Is contrast used intentionally?
- Is the visual weight balanced?
- Does the hierarchy survive mobile layouts?
- Does the semantic HTML match the visual hierarchy?
- Is the result visually premium?
