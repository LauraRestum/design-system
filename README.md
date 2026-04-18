# Envision Design System

**The single source of truth for how Envision looks, sounds, and designs.**

A design-first system — principles, grids, components, section patterns, and recipes — with rendered HTML references you can open in a browser. Built from the 2026 Edition of the Envision Brand Book.

---

## Start here

Open `index.html` in your browser. That's the visual entry point to everything below.

Or, if you prefer to browse directly:

| If you want to… | Open this |
| --- | --- |
| See every section type rendered | `layout/section-patterns.html` |
| See buttons, cards, stats, form fields | `components/component-library.html` |
| See a full composed landing page | `patterns/landing-page-commercial.html` |
| See a Mailchimp-safe email template | `patterns/email-template.html` |
| See PowerPoint slide layouts | `patterns/slide-layouts.html` |
| See all colors and type | `examples/token-preview.html` |
| Know **how to design** | `design-principles/README.md` |
| Know **how to compose a page** | `layout/README.md` |
| Get a **step-by-step recipe** | `design-recipes/README.md` |

---

## Repo structure

```
envision-design-system/
├── index.html                      # Start here — visual entry point
├── README.md                       # This file
├── CLAUDE.md                       # Instructions for AI assistants
│
├── tokens/                         # Machine-readable source of truth
│   ├── colors.json                 # Primary, extended, WCAG pairs
│   ├── typography.json             # Gotham / Montserrat / Humanist
│   ├── spacing.json                # 4px scale + aliases
│   └── envision-tokens.css         # CSS custom properties + utility classes
│
├── design-principles/              # How Envision designs (the twelve rules)
│   └── README.md
│
├── layout/                         # Grids, rhythm, composition
│   ├── README.md                   # Grid system, breakpoints, section rhythm
│   └── section-patterns.html       # 10 rendered section patterns
│
├── components/                     # UI building blocks
│   └── component-library.html      # All components rendered
│
├── patterns/                       # Full compositions
│   ├── landing-page-commercial.html   # Complete landing page
│   ├── email-template.html            # Mailchimp-safe email
│   └── slide-layouts.html             # 8 PowerPoint layouts at 16:9
│
├── design-recipes/                 # Task-based how-tos
│   └── README.md                   # Deck, landing page, email, one-pager, pillar page
│
├── guidelines/                     # Voice, brand, audiences
│   ├── our-story.md
│   ├── brand-rules.md
│   ├── voice-and-tone.md
│   ├── brand-architecture.md
│   ├── pillar-profiles.md
│   └── audience-personas.md
│
├── examples/                       # Spec preview pages
│   └── token-preview.html
│
└── assets/                         # Placeholder — logos, fonts, images
    ├── logos/
    ├── fonts/
    ├── images/
    └── icons/
```

---

## How to use this with Claude Code

In any Envision project, clone this repo alongside your work:

```bash
# In the parent directory of your project
git clone https://github.com/LauraRestum/envision-design-system.git
```

Then in your project's `CLAUDE.md`:

```
Design system: ../envision-design-system

Always:
1. Read ../envision-design-system/design-principles/README.md before designing
2. Use tokens from ../envision-design-system/tokens/envision-tokens.css
3. Reference section patterns from ../envision-design-system/layout/section-patterns.html
4. Follow recipes from ../envision-design-system/design-recipes/README.md
```

Then in prompts you can say:

> "Build a commercial landing page using Recipe 2 for the SEWP VI fulfillment launch."

Claude Code will pull section sequence, tokens, components, and voice rules automatically.

---

## The twelve design principles

The shortest version:

1. Navy anchors. Green accents. Everything else supports.
2. Lead with type. Not imagery.
3. Hierarchy before decoration.
4. Whitespace is a feature, not a leftover.
5. Restraint wins. Always.
6. Geometry is sharp, not soft.
7. Color-block, don't gradient-blend.
8. Type treatment is the brand.
9. Photography is candid, not staged.
10. Commercial work leads with capability.
11. Mission work centers the person.
12. The design serves the through-line (Thriving).

Full version with examples: `design-principles/README.md`.

---

## Versioning

- Tokens — v1.2.0 (Primary Blue #003087, Primary Green #78BE21, verified against 2026 brand book)
- Design system — v1.0.0 (initial release)

Changelog lives at the top of each token JSON file.

---

## Credits

- Source — Envision Brand Book 2026 Edition (brand-guidelines-nine.vercel.app)
- Owner — Laura Restum, Marketing Manager, Envision Inc.
- Reviewed by — Madison Neuhaus, Sr. Director of Marketing & Communications
- Built with assistance from Claude (Anthropic)

© 2026 Envision Inc. All rights reserved. Proprietary — internal Envision use only.
