# Layout System

How Envision pages, decks, and emails are composed. The underlying grid, spacing rhythm, and section patterns that make everything feel consistent.

---

## The Grid

### 12-column grid (web)

Web pages and landing pages use a **12-column grid** at desktop (1024px+). This is the most flexible system:

- Full width: 12 columns
- Two-column: 6 + 6
- Three-column: 4 + 4 + 4
- Asymmetric hero: 7 + 5 (content + image)
- Sidebar layout: 8 + 4 (content + sidebar)
- Four-column stat grid: 3 + 3 + 3 + 3

**Gutter:** 24px between columns at desktop, 16px at tablet, collapses to single column at mobile (<768px).

### Container widths

Content never stretches edge-to-edge on wide screens. Maximum container widths:

| Context | Width | Use |
| --- | --- | --- |
| Email | 640px | All email templates |
| Narrow content | 640-720px | Long-form articles, focused reading |
| Default | 1200px | Landing pages, marketing pages, sales content |
| Wide | 1440px | Dashboards, data tables, image-heavy galleries |

**Always include horizontal padding** inside containers: 24px at mobile, 32px at tablet, 40-48px at desktop.

### PowerPoint grid (16:9)

Decks use a **16:9 ratio at 1920×1080px**. Treat each slide as a 12-column grid with:

- Safe area: 80px padding from all edges
- Title zone: top 160-200px
- Content zone: everything else
- Gutter between columns: 40px

## Section Rhythm

Every page is a stack of sections. Sections have consistent vertical padding so the page has a predictable rhythm.

| Rhythm | Vertical padding | Use |
| --- | --- | --- |
| Tight | 48px (mobile) / 64px (desktop) | Utility sections, related content blocks |
| Default | 64px (mobile) / 96px (desktop) | Most content sections |
| Spacious | 80px (mobile) / 128px (desktop) | Marquee sections, testimonials |
| Hero | 96px (mobile) / 160px (desktop) | Page heroes, major CTAs |

**Rule:** Never stack sections with less than 48px vertical rhythm between them. Cramped sections read as AI-generated defaults.

## Spacing Rhythm Inside Content

Within a section, content follows a tight vertical rhythm based on the 4px scale:

- **Eyebrow → Headline:** 16px
- **Headline → Body copy:** 24-32px
- **Body paragraph → Body paragraph:** 16px
- **Body copy → CTA:** 32-40px
- **CTA → End of section:** 0 (section padding takes over)

Inside cards:

- **Card internal padding:** 24px (default) or 40px (large/featured)
- **Card internal vertical rhythm:** Same as above, compressed

## Section Patterns

These are the most common section layouts across Envision web and email work. Each has a rendered preview in `layout/previews/`.

### 1. Hero — type-forward

Solid Primary Blue background. Left-aligned or centered headline in white, set at 56-72px, Bold/Black, tracking -0.045em. Supporting body copy in secondary-on-dark color. Single primary CTA, green accent.

**Proportions:** Headline dominates. Body copy max 2-3 lines. CTA sits at natural stopping point.

### 2. Hero — split (type + image)

7/5 or 6/6 split. Headline + body + CTA on the left, photography on the right. Photography should show a person in action (see Principle 9). Image never has rounded corners above 4px.

### 3. Stat block — 3 or 4 column

Grid of 3-4 stats. Each stat: large number (48-72px, Bold, Primary Blue), short label beneath (14-16px, Charcoal, uppercase eyebrow style optional). Minimal other content. Let the numbers breathe.

### 4. Feature grid — cards

3-column grid of feature cards. Each card: icon or small image, headline (18-22px, Bold, Primary Blue), body copy (14-16px, Charcoal, 2-3 lines). Card border: 1px subtle gray or no border with elevated surface color. 24px internal padding, 24-32px gap between cards.

### 5. Pull quote / testimonial

Single centered quote, 28-36px, Bold or Regular, Primary Blue or Charcoal. Attribution beneath at 14px. Optional small photo of the person at 64-80px. Plenty of whitespace around the quote (80-128px vertical).

### 6. Pillar / program section

Split layout. Eyebrow label (green, uppercase, 0.5em tracking), headline, body copy, CTA on one side. Supporting image or illustration on the other. Used to introduce one of the eight program pillars.

### 7. Full-width callout

Solid color band (Primary Blue, Navy, or an approved accent). Single headline + CTA. Used as a separator between major page sections or as a pre-footer CTA. Vertical padding: 96-128px.

### 8. Data-forward section

Dense with information. Stats, charts, certifications, proof points. Used in commercial/B2B work. Lives on a white or off-white background. Type-dominant. Navy headlines, green data highlights on 1-2 key stats.

### 9. Image grid / gallery

2-4 column grid of photography. Sharp rectangles, no rounded corners. 24-32px gap. Used sparingly for program showcase or event recap.

### 10. Footer

Navy background. 4-column layout (logo+mission, pillars, resources, contact). Type-heavy. Fine divider lines in subtle gray. Copyright line at the very bottom in caption size.

## Breakpoints

Mobile-first. Design for 375px width, then scale up.

| Name | Width | What changes |
| --- | --- | --- |
| Mobile | 375-639px | Single column, 24px horizontal padding, smaller type scale |
| Tablet | 640-1023px | 2-column grids, 32px horizontal padding |
| Desktop | 1024px+ | Full 12-column grid, 40-48px horizontal padding, max 1200px container |
| Wide | 1440px+ | Same as desktop, 1440px container for dashboards only |

## Responsive type scale

At mobile, reduce display/headline sizes by ~25-35%:

| Desktop | Mobile |
| --- | --- |
| 72px (display-xl) | 44px |
| 56px (display-lg) | 36px |
| 44px (display-md) | 30px |
| 36px (heading-xl) | 26px |
| 28px (heading-lg) | 22px |
| Body sizes | Unchanged |

## Composition Rules

### One primary action per screen

A page can have many secondary links, but only **one** visually dominant CTA per viewport. If you have two equally weighted CTAs side by side, you've got a problem — users freeze.

### Edges align

Every element's left edge should align to the grid. Don't arbitrarily nudge things. If you need to break the grid, break it dramatically (a photo that bleeds off the edge) — not subtly.

### Photography goes to the edge

When using photography in a section, it should either:
- Sit on the grid with the same padding as other content, OR
- Bleed fully to the edge of the viewport (full-bleed)

Never in between. Never 80% of the way to the edge with a random gap.

### Group related content

Use whitespace to signal relationships. An eyebrow, a headline, and body copy that go together should sit close (16-32px apart). The gap to the *next* content group should be noticeably larger (64-96px).

### Asymmetry is fine. Randomness isn't.

Envision layouts can be asymmetric (7/5 splits, offset content, imagery that extends past a column). But asymmetry is deliberate. Random placement with "artistic" offsets reads as amateur.
