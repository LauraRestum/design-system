# Envision Design Principles

These are the twelve principles that define how Envision designs. They answer the question *"what makes something look like Envision?"* beyond just colors and fonts.

Every component, layout, and pattern in this system descends from these principles. If you're unsure whether a design decision is on-brand, check it against these principles first.

---

## 1. Navy anchors. Green accents. Everything else supports.

**Primary Blue `#003087`** is the gravitational center of every Envision design. It's what the eye lands on first. It carries the headlines, the primary CTAs, the section markers, the footer, the hero.

**Primary Green `#78BE21`** shows up in small, deliberate doses. A CTA. A single stat that matters. An eyebrow label above a headline. A highlight on one word. **Never more than 10% of a page.**

**The extended palette** (Bright Blue, Goldenrod, Terracotta, Violet, Forest Green) adds warmth and differentiation — but only when there's a reason. Program pages, events, human-story callouts. Never decorative.

**What this looks like in practice:** A page with primary blue headlines, charcoal body copy, a green CTA, and a single terracotta accent on a testimonial card. Not a rainbow.

**The test:** Could someone describe your design in one sentence as "blue with a green accent"? If yes, you're on-brand. If they'd say "blue, green, orange, yellow, and purple," you're off.

---

## 2. Lead with type. Not imagery.

Envision's headlines do the heavy lifting. A 56-72px headline in Bold or Black, tracked tight at -0.045em, set in Primary Blue or on a Primary Blue background, is the most on-brand thing you can put on a page.

Photography supports the headline. It doesn't replace it. A hero section without a strong type-first headline is weak, regardless of how good the photo is.

**What this looks like in practice:** Headlines dominate hero sections. Photography sits to the side, below, or as a secondary element. In type-only sections, typography is treated as the design itself.

**The test:** If you removed the photography from a hero, would the design still communicate its message? It should.

---

## 3. Hierarchy before decoration.

Every block of content has one thing that matters most. Make that thing bigger, bolder, or more saturated than everything around it. Decoration comes after hierarchy is established.

**What this looks like in practice:**
- One hero headline per section. Not competing h1s.
- One primary CTA per screen. Secondary CTAs are ghosted or smaller.
- One stat that matters per stat-block. Others supporting.
- One accent color at a time. Multiple accents mean no accent.

**The test:** Squint at a design. Does one element still stand out? If everything blurs to the same visual weight, hierarchy is broken.

---

## 4. Whitespace is a feature, not a leftover.

Envision designs breathe. Section padding is generous (64-96px vertical on desktop). Cards have room inside them (24-40px internal padding). Headlines have space around them.

Cramped design reads as cheap and charity-coded. Spacious design reads as enterprise-grade.

**What this looks like in practice:**
- Minimum 64px vertical section padding on desktop (48px on mobile).
- Card padding at least 24px.
- 40-80px margin between a headline and its body copy.
- Generous gaps between grid items (24-40px).

**The test:** Could you remove more content and the page would feel better? If yes, remove it. Whitespace over density.

---

## 5. Restraint wins. Always.

Envision is not a design-forward consumer brand. We're not trying to be Figma or Stripe. We're enterprise-credible, mission-driven, and calm.

That means: no gradients on text. No drop shadows. No glow effects. No rounded pills. No "glassmorphism." No animated hero backgrounds. No confetti illustrations. No hand-drawn arrows. No "fun" emoji in corporate work.

**What this looks like in practice:** Flat color. Sharp edges (max 4px radius). Solid backgrounds. Real photography. Clean type. No decorative effects.

**The test:** Could this design exist in 2010? If yes, it's probably Envision-appropriate. If it needs a GPU to render its effects, it's off-brand.

---

## 6. Geometry is sharp, not soft.

Borders are sharp (max 4px radius). Dividers are hairline (1-2px). Grids are aligned. Section edges are crisp.

Envision does not use soft, rounded, "friendly" shapes. We use rectangles, straight lines, and clean type. The warmth comes from color choice (goldenrod, terracotta) and human photography — not from rounded corners or bubble shapes.

**What this looks like in practice:**
- Cards: `border-radius: 4px` max.
- Buttons: `border-radius: 4px` max. Never pills (`border-radius: 999px`).
- Images: Sharp rectangles. Never circular crops except for approved portrait use.
- Dividers: 1-2px solid lines.

**The test:** Is there a single rounded corner above 4px in the design? Fix it.

---

## 7. Color-block, don't gradient-blend.

When Envision uses color, it uses full, flat color blocks. A primary blue hero is solid primary blue. A green callout is solid green. The transition between colors happens at a hard edge — a section boundary, a card border — not through a gradient.

**What this looks like in practice:**
- Hero sections: solid primary blue or navy background.
- Callout cards: solid accent color (green, goldenrod, terracotta).
- Stat blocks: solid fill with contrasting type.
- No gradient backgrounds. No gradient overlays on photos (except for text legibility — dark-to-transparent only, never color-to-color).

**The test:** Are any two colors blending into each other? Stop.

---

## 8. Type treatment is the brand.

The specific type treatment — Bold/Black headlines, tracked at -0.045em, title case, set against a lot of whitespace — is how Envision looks different from other nonprofits or enterprise brands.

Buttons are uppercase Bold at 0.25em tracking. Large subheads are uppercase Bold at 0.5em tracking — wide, airy, confident. Body copy is Regular at 140-160% line-height and -0.02em tracking.

**Never:**
- Default CSS type (font-weight: normal, tracking 0, line-height: normal). It looks generic.
- Italics for emphasis — use weight instead.
- All-caps for headlines or body.
- Mixing 4+ weights on a page.

**The test:** Does the type feel deliberately spec'd, or does it feel like a browser default?

---

## 9. Photography is candid, not staged.

Envision photography shows real people in real moments — working, creating, learning, connecting. Natural light. Authentic expressions. Depth of field that draws the eye to the person, not the surroundings.

**Never:**
- Stock "diverse hands on a laptop."
- Handshakes in suits.
- Model-posed portraits against white backgrounds.
- Inspirational silhouettes against sunsets.
- Pity framing — isolated, looking down, empty rooms.
- Staged "disability performance" — a cane prominently centered, guide dog as the focus.

**What this looks like in practice:** An artist at their easel. A child in a classroom. A worker on a production line. A clinician and client in a real moment. The person is the subject. Their disability is incidental to the frame.

**The test:** Does the person look like they're doing something real, or performing for the camera?

---

## 10. Commercial work leads with capability.

When designing for commercial, B2B, or federal audiences (Commercial Solutions, Base Supply Center contracting, APS, Philips, Streamlight, Under Armour), the visual design must carry enterprise credibility first.

**What this looks like in practice:**
- Stats, certifications, and proof points are visually prominent.
- Navy/primary blue dominates. Mission framing is absent or minimal.
- Photography shows operations: production lines, facilities, workforce, not clients receiving services.
- Typography is confident and dense. Not "mission-soft."
- CTAs are direct: "Schedule a conversation," "Request capabilities," not "Learn about our mission."

**The test:** Would a procurement officer take this seriously as a vendor presentation? If it reads as a nonprofit appeal, redesign.

---

## 11. Mission work centers the person.

When designing for BVI audiences, caregivers, referring professionals, or donors, the person is the subject — not the organization.

**What this looks like in practice:**
- Photography features BVI individuals in moments of agency — working, creating, teaching, moving through the world.
- Stories are told in the person's voice or from their perspective.
- Typography warms slightly — still on-system, but with more air, more warmth in color combinations.
- Extended palette (goldenrod, terracotta) shows up more here than in commercial work.
- CTAs frame the person's agency: "Explore what's possible," "See what thriving looks like."

**The test:** Is Envision the hero of this page, or is the person? The person should be.

---

## 12. The design serves the through-line.

Everything Envision designs serves one idea: **Thriving.** With the right tools, the right support, and the right opportunities — at every stage of life.

This means:
- Design should feel forward-looking, not nostalgic.
- Design should feel capable, not needy.
- Design should feel inclusive by default, not performatively accessible.
- Design should feel like it respects its audience's intelligence.

**The test:** Does this design help communicate that people are thriving because of the right tools and support? Or does it undermine that — by feeling charity-coded, dated, pitying, or generic?

---

## Quick decision checklist

Before you ship anything, ask:

1. Is Primary Blue the visual anchor?
2. Is Primary Green used sparingly (one or two moments)?
3. Is there a single, clear hierarchy?
4. Is there enough whitespace?
5. Are all radii ≤ 4px?
6. Are all colors flat (no gradients)?
7. Are headlines set to Bold/Black, tight tracking, title case?
8. Is photography candid and authentic?
9. Does commercial work lead with capability?
10. Does mission work center the person?
11. Could you remove 20% of the content and the page would be better?
12. Does it feel like Envision — or like a generic AI-generated template?

If you answered "no" to any of these, keep iterating.
