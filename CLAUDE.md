# CLAUDE.md — Instructions for AI Assistants

You are working inside the **Envision Design System** repo. This file is your orientation. Read it before doing anything else in this repo.

## What this repo is for

This is the ground-truth design system for Envision Inc. Any output you produce from this repo — HTML, CSS, PowerPoint, print, email, deck, copy — must conform to the standards defined here. This repo exists specifically so you do not have to guess.

## How to use this repo

1. **Always read `tokens/` before writing CSS or inline styles.** Never invent color values. Never round a hex code. Never swap Montserrat for a "similar" font.
2. **Always check `guidelines/brand-rules.md` before writing copy.** Envision has specific language rules (no deficit language, business-first framing, specific entity naming) that are non-negotiable.
3. **Start from `templates/` when producing a new deliverable.** Do not scaffold a new HTML page, deck, or document from a blank file if a template exists.
4. **Reference `examples/` for tone and aesthetic calibration**, not for copy-paste.
5. **If a user's request conflicts with the system, flag it.** Do not silently override brand rules to accommodate a prompt.

## Non-negotiable rules

These apply to every output without exception:

- **Colors come from `tokens/colors.json`.** Do not introduce new colors. The primary anchor is `#1B365D` (navy). The primary accent is `#78BE21` (green), used sparingly.
- **Typography is Montserrat.** See `tokens/typography.json` for weights and scales.
- **Geometry:** `border-radius` max 4px. No `box-shadow` in production output. No gradient backgrounds except on approved callout/chart patterns.
- **Language:** Business first, mission second. No deficit framing ("helps the disabled," "people with limitations," etc.). See `guidelines/voice-and-tone.md`.
- **Entity naming:**
  - "Envision" — the company holistically
  - "Envision, Dallas Campus" or "Envision, Wichita Campus" — when location matters
  - "Envision's Dallas Foundation" — always with the apostrophe; never "Envision Dallas Foundation"
- **Madison Neuhaus is not a reviewer on Philips Healthcare / Controlled OEM Gateway materials.** Do not list her as a stakeholder on those.

## File priority when you're uncertain

1. `tokens/` — the numbers win
2. `guidelines/brand-rules.md` — the language rules win
3. `components/` — the patterns win over improvised layouts
4. `examples/` — aesthetic calibration, lowest priority of the four

## Things to never do

- Never use rounded pill buttons.
- Never use drop shadows to create depth.
- Never use emoji in corporate or commercial deliverables.
- Never use stock-photo "diverse hands on a laptop" imagery.
- Never use the word "empower" or "empowerment" in commercial/B2B copy.
- Never produce a deliverable without checking `tokens/` and `guidelines/` first.

## When in doubt

Ask. Surface the ambiguity in your response rather than picking a direction that might violate the system.
