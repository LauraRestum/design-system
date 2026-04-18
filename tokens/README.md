# Tokens

Machine-readable design tokens. **The values in these files are the source of truth.** If a component, template, or example disagrees with a token, the token wins.

## Files

| File | Status | Contents |
| --- | --- | --- |
| `colors.json` | ✅ Populated | Brand palette, semantic colors, data-viz sequence, usage rules |
| `typography.json` | ✅ Populated | Montserrat weights, scales, line-heights, letter-spacing, composed text styles |
| `envision-tokens.css` | ✅ Populated | CSS custom properties generated from the JSON above — ready to drop into any HTML project |
| `spacing.json` | ⏳ To do | 4px-base spacing scale |
| `radii.json` | ⏳ To do | Border-radius values (max 4px) |
| `shadows.json` | ⏳ To do | Shadow tokens (production default: none) |
| `motion.json` | ⏳ To do | Easing and duration tokens |

## Token naming convention

`category.role.variant.state` — e.g., `color.brand.navy.base`, `color.accent.green.base`.

## How to use

### In HTML / CSS projects

Link the generated CSS file and use the custom properties:

```html
<link rel="stylesheet" href="tokens/envision-tokens.css">

<style>
  .hero {
    background: var(--color-brand-navy);
    color: var(--color-text-on-dark);
    font-family: var(--font-family-primary);
    font-size: var(--font-size-display-lg);
    font-weight: var(--font-weight-bold);
  }

  .cta {
    background: var(--color-action-accent);
    color: var(--color-white);
    border-radius: var(--radius-md);
    padding: 12px 24px;
  }
</style>
```

### In Claude Code

Claude Code reads `CLAUDE.md` at the repo root, which points here. Just ask for what you want — e.g. *"build me a one-pager hero section"* — and the tokens will be applied without hex codes being invented.

### In PowerPoint

Use the hex values from `colors.json` directly in the PPT theme editor. Theme colors should map as:

- Text/Background 1 → `#FFFFFF` (white)
- Text/Background 2 → `#1B365D` (navy base)
- Accent 1 → `#1B365D` (navy base)
- Accent 2 → `#78BE21` (green base)
- Accent 3 → `#4A90A4` (blue)
- Accent 4 → `#7CB342` (green PPT)
- Accent 5 → `#2D4A73` (navy soft)
- Accent 6 → `#6B7280` (gray 500)

### In Figma / Adobe

Import the JSON directly via Tokens Studio (Figma) or paste hex values into brand libraries.

## Rules of the system

**Allowed:**
- Use `color.brand.navy.base` as the primary anchor.
- Use `color.brand.green.base` as a controlled accent — CTAs, single data highlights, emphasis.
- Compose text styles from the `styles.*` object in `typography.json` rather than reassembling font properties each time.

**Forbidden:**
- Do not invent new colors. If a color is missing, escalate.
- Do not round or approximate hex values (no `#1B3660`, no `#78BE20`).
- Do not substitute Montserrat for a "similar" font.
- Do not use `border-radius` above 4px.
- Do not ship `box-shadow` in production materials.

## Regenerating the CSS

When `colors.json` or `typography.json` changes, regenerate `envision-tokens.css` so the two stay in sync. A build script will land here once the token set stabilizes.
