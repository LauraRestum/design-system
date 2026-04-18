# Envision Design System

The single source of truth for Envision Inc.'s brand, visual, and component standards.

**Maintained by:** Marketing & Communications — Envision Inc.
**Primary contact:** Laura Restum, Marketing Manager
**Status:** Internal — Envision team use only

---

## What this repo is

This is the canonical design system for everything Envision produces externally: commercial sales materials, B2B collateral, event marketing, web, print, and executive decks. It exists so that:

1. **Everything Envision ships looks like Envision** — no AI-generated defaults, no rogue template aesthetics, no off-brand gradients or rounded pills.
2. **AI tools can build on-brand work without re-briefing.** This repo is the ground truth Claude Code, Claude.ai, and other AI assistants reference when producing Envision work.
3. **New hires, contractors, and external agencies can get aligned in one place** instead of chasing PDFs across email threads.

## What lives here

| Folder | What's in it |
| --- | --- |
| `tokens/` | Machine-readable design tokens — colors, typography, spacing, radii, shadows. The source values. |
| `components/` | Reusable component patterns (HTML/CSS and PowerPoint). Buttons, cards, headers, data blocks. |
| `guidelines/` | Written brand guidance — voice, tone, content hierarchy, banned patterns, photography direction. |
| `assets/` | Logos, fonts, brand imagery, iconography. |
| `templates/` | Starting-point files: pitch decks, one-pagers, email shells, print layouts. |
| `examples/` | Real, shipped work that exemplifies the system. Reference material, not a component library. |
| `CLAUDE.md` | Instructions for Claude Code and other AI assistants working in this repo. |

## Quick start

**For humans:** Start with `guidelines/README.md` for the brand philosophy, then browse `tokens/` and `components/` for the "how."

**For Claude Code / AI assistants:** Read `CLAUDE.md` first. It points to the AI Brand Directive and tells you how to use the tokens and components without guessing.

**For a new project:** Copy from `templates/` rather than starting from a blank file.

## Core brand rules (the short version)

- **Business first. Mission second.** All commercial and B2B work leads with enterprise credibility. Deficit language is banned.
- **Colors:** Dark navy `#1B365D` anchors. Green `#78BE21` is a controlled accent, never a field color.
- **Type:** Montserrat throughout. No secondary families without approval.
- **Geometry:** No rounded corners above 4px. No drop shadows. No gradients outside approved callout/chart usage.
- **Entity naming:** "Envision" holistically. "Envision, Dallas Campus" or "Envision, Wichita Campus" when location matters. "Envision's Dallas Foundation" (with apostrophe) for the foundation entity.

Full rules: `guidelines/brand-rules.md`.

## Contributing

This is a private internal repo. Changes require review from Marketing & Communications leadership. See `.github/CONTRIBUTING.md` (add when ready).

## License

Proprietary — Envision Inc. All rights reserved. Not for external distribution without written approval.
