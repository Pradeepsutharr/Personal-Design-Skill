# SEO Standards

## Purpose

Every public-facing page should be designed and implemented so search engines can understand its purpose, content hierarchy, relationships, and important entities.

SEO is part of architecture and content design, not a final metadata patch.

## Core Principle

Create pages for users first while making their meaning explicit to search engines through semantic HTML, metadata, structured data, crawlable content, and strong information architecture.

## Page Purpose

Before building a page, identify:

- Primary search intent
- Primary topic
- Primary keyword or topic phrase when relevant
- Supporting topics
- Intended audience
- Desired conversion or next action

Do not force keywords into copy where they make the content unnatural.

## Title Metadata

Each indexable page should have a unique, descriptive title.

A strong title should:

- Describe the page accurately.
- Put the primary topic near the beginning when natural.
- Be useful to humans, not just search engines.
- Avoid unnecessary repetition.

Do not generate duplicate titles across unrelated pages.

## Meta Description

Provide a concise, useful description that communicates:

- What the page offers.
- Who it is for when relevant.
- Why the user should care.

Do not keyword-stuff descriptions.

## Heading Hierarchy

Use semantic headings.

- One clear primary page heading in normal page structures.
- Use `h2` for major sections.
- Use `h3` for subsections.
- Continue logically.

Do not choose heading levels purely for visual size. Style semantic headings independently when needed.

## Semantic HTML

Prefer meaningful elements:

- `main`
- `header`
- `nav`
- `section`
- `article`
- `footer`
- `aside`
- `button`
- `a`

Semantic structure helps users, assistive technologies, and crawlers understand the page.

## Crawlable Content

Important content should exist in the accessible page structure.

Do not make critical text discoverable only after a client-side interaction when a crawlable alternative is appropriate.

Avoid hiding important content exclusively behind animations, tabs, or client-only rendering without a valid product reason.

## Internal Linking

Use internal links to establish useful relationships between pages.

Good internal links:

- Use descriptive anchor text.
- Lead to genuinely relevant pages.
- Help users discover related content.
- Support the site's information architecture.

Avoid generic anchors such as `click here` when a descriptive label is possible.

## Canonical URLs

Use canonical URLs where duplicate or near-duplicate URLs can occur.

Ensure canonical strategy is consistent with routing and deployment.

Do not generate conflicting canonical values across environments.

## Open Graph

Public pages should be ready for rich sharing.

Consider:

- Open Graph title
- Open Graph description
- Open Graph image
- Open Graph URL
- Site or brand information

Use page-specific social imagery when it materially improves sharing.

## Twitter/X Cards

When the project uses social metadata, provide appropriate Twitter/X card metadata consistent with the page's Open Graph content.

## Structured Data

Use Schema.org structured data when it accurately describes the page.

Potential types include:

- Organization
- WebSite
- WebPage
- BreadcrumbList
- Article
- Product
- FAQPage where genuinely applicable
- LocalBusiness where appropriate
- SoftwareApplication where appropriate

Never invent structured data that does not match visible or valid page information.

## Breadcrumbs

For deep information architectures, breadcrumbs can improve navigation and provide useful structured context.

Use them when they reflect the real hierarchy.

## Images

SEO-friendly images should:

- Have descriptive filenames when practical.
- Use meaningful alt text for informative images.
- Use empty alt text for purely decorative images.
- Have dimensions to reduce layout shift.
- Be optimized for performance.

Do not stuff keywords into alt text.

## URLs

Prefer clean, stable URLs.

Good URLs should be:

- Descriptive
- Predictable
- Short where practical
- Consistent with the information architecture

Avoid unnecessary query parameters for canonical content when path-based routing is appropriate.

## Content Structure

Pages should be easy to scan.

Use:

- Clear headings
- Short paragraphs
- Lists where useful
- Supporting visuals
- Descriptive links
- Clear CTAs

Do not sacrifice readability for keyword density.

## SEO and Performance

SEO implementation must not create unnecessary performance problems.

Avoid:

- Huge hero assets
- Unnecessary client-side rendering
- Excessive third-party scripts
- Heavy animation for above-the-fold content
- Blocking non-critical resources

A search-friendly page should also be fast and accessible.

## SEO and Accessibility

Many SEO-friendly practices overlap with accessibility.

Prioritize:

- Semantic HTML
- Descriptive headings
- Useful link text
- Image alt text
- Form labels
- Good contrast
- Keyboard accessibility

## Next.js SEO

For Next.js applications:

- Use the framework's metadata capabilities appropriately.
- Keep page titles and descriptions route-specific.
- Use static metadata when content is static.
- Use generated metadata when it depends on route data.
- Avoid unnecessary client-side metadata logic.
- Consider sitemap and robots configuration for public sites.
- Keep canonical URLs environment-aware.

## Dynamic Pages

For dynamic content:

- Generate unique metadata where appropriate.
- Handle missing content correctly.
- Avoid indexing invalid or empty pages.
- Provide meaningful fallback behavior.
- Ensure canonical URLs match the final public route.

## SEO Review

Before shipping, ask:

- Is the page SEO-friendly?
- Does it have a unique title?
- Is the description useful?
- Is heading hierarchy logical?
- Is important content crawlable?
- Are semantic elements used?
- Are images optimized and described correctly?
- Are internal links useful?
- Is the canonical strategy correct?
- Are Open Graph tags considered?
- Is structured data appropriate?
- Is the URL clean?
- Is the page fast?
- Is the page accessible?
- Are SEO claims based on actual implementation rather than assumptions?
