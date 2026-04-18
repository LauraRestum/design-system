# Claude Instructions — Envision Design System

This file tells AI assistants (Claude Code, Claude in chat, etc.) how to use this design system.

## What this is

The Envision Design System is a design-first reference. It tells you **how to design for Envision**, not just **what Envision's brand values are**. It includes:

- Tokens (colors, type, spacing) you can link to
- Design principles that govern every decision
- Layout and composition rules
- Rendered HTML examples of every section type and component
- Full-page composed examples (landing page, email, slide layouts)
- Task-based recipes

## Your job when designing for Envision

### 1. Read the design principles first

Before you create anything, read `design-principles/README.md`. The twelve principles are the tiebreaker for every design decision. They answer questions like:
- "Should I use Primary Blue or Navy here?"
- "Is this photo on-brand?"
- "Does this hero section feel right?"

Refuse to design without reading these first.

### 2. Use the token files

Colors, typography, spacing — pull from the source:

- **CSS projects:** Link `tokens/envision-tokens.css` in your HTML head:
  ```html
  <link rel="stylesheet" href="path/to/envision-design-system/tokens/envision-tokens.css">
  ```
  Then use CSS variables: `color: var(--color-primary-blue); padding: var(--space-16);`

- **Programmatic work:** Parse the JSON files:
  - `tokens/colors.json`
  - `tokens/typography.json`
  - `tokens/spacing.json`

Never hardcode color hex values or type sizes. Always reference tokens.

### 3. Match the request to a recipe

For common deliverables, check `design-recipes/README.md` first. If the user is asking for:

- A commercial sales deck → Recipe 1
- A landing page (commercial) → Recipe 2
- A Mailchimp email campaign → Recipe 3
- A one-pager capabilities brief → Recipe 4
- A program / pillar landing page → Recipe 5

Recipes give you the section sequence, hierarchy, and specific rules. They exist so you don't have to re-derive the approach each time.

### 4. Compose with section patterns

`layout/section-patterns.html` is the master reference for page-level composition. Ten patterns:

1. Hero — type-forward (commercial, B2B, federal)
2. Hero — split with image (program, mission work)
3. Stat block (3 or 4 column)
4. Feature grid — cards
5. Pull quote / testimonial
6. Pillar / program section
7. Full-width callout
8. Data-forward section (tables, certifications)
9. Image grid / gallery
10. Footer

When building a page, decide the section sequence first, then fill each section using the corresponding pattern.

### 5. Use the component library for small pieces

`components/component-library.html` shows every UI primitive: buttons (3 variants), eyebrows (3 variants), cards, stats, chips, form fields, callouts, dividers, type samples. Don't invent new components — use these.

### 6. Follow the voice rules

`guidelines/voice-and-tone.md` is the authority on language. The most important rules:
- **Person-first language:** "people who are blind or low vision" (BVI acceptable after first mention). Never "the blind" or "handicapped."
- **No deficit framing:** Lead with what someone can do, not what they can't.
- **Commercial work leads with capability.** Mission enters later (if at all) — it's the reason to choose Envision when capability is equal, not a substitute for it.
- **Mission work centers the person,** not Envision.

### 7. Respect the non-negotiables

From `guidelines/brand-rules.md`:

- Primary Blue `#003087` is the anchor. Primary Green `#78BE21` is an accent only (never more than ~10% of a page).
- Max border-radius is 4px. No pills, no rounded shadows.
- No drop shadows, no gradients on text, no decorative effects.
- Typography: Gotham for print (licensed), Montserrat for web, Humanist is **logo-only** (never elsewhere).
- Headlines tracked at -0.045em. Buttons uppercase at 0.25em tracking. Large subheads uppercase at 0.5em tracking.
- Entity naming: "Envision's Dallas Foundation" (with apostrophe). "Envision, Dallas Campus" (with comma) when location matters. Never "Envision Dallas" alone.
- Retired marks to never use: Envision Xpress (now Base Supply Center), old Arts logo, old ECDC circular.
- Madison Neuhaus is **not** a reviewer on Philips Healthcare / Controlled OEM Gateway materials — never list her as a stakeholder on Philips work.

## Typical workflow

When the user asks you to create something for Envision:

1. **Identify the deliverable type.** PowerPoint? Landing page? Email? One-pager?
2. **Match it to a recipe** in `design-recipes/README.md`.
3. **Read the twelve design principles** in `design-principles/README.md`.
4. **Check the relevant pillar profile** in `guidelines/pillar-profiles.md` (if the work is pillar-specific).
5. **Check the voice rules** in `guidelines/voice-and-tone.md`.
6. **Link the CSS tokens** and use CSS variables throughout.
7. **Compose the page** using section patterns from `layout/section-patterns.html`.
8. **Fill in components** from `components/component-library.html`.
9. **Self-check against the design principles** checklist at the bottom of `design-principles/README.md`.

## Common mistakes to avoid

- Using default browser styles (system font, `line-height: normal`, no letter-spacing). Envision typography is always deliberately spec'd.
- Leading commercial work with mission language. Capability first. Always.
- Applying rounded corners above 4px. Never pills. Never rounded hero images.
- Using drop shadows, gradients, glow effects, or glassmorphism.
- Treating Primary Green as a field color. It's an accent only.
- Using generic stock photography. If no real Envision photography is available, go type-only.
- Saying "Envision Dallas" — either "Envision" alone (holistically), "Envision, Dallas Campus" (location-specific), or "Envision's Dallas Foundation" (the foundation entity).

## When in doubt

If you're unsure whether something is on-brand, run it against the checklist at the end of `design-principles/README.md`. If you still can't tell, flag it to the user rather than guessing.
