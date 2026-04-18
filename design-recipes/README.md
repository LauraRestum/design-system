# Design Recipes

Task-based guides. When you know what you need to make, start here.

Each recipe walks through the design decisions for a specific deliverable — not just "what" but "why."

---

## Recipe 1: A Commercial Sales Deck

**Audience:** Procurement officers, supply chain managers, enterprise buyers.
**Output:** PowerPoint, 12-18 slides.

### Structure (the 7-slide skeleton)

1. **Cover** — Solid Primary Blue. Headline states the value proposition directly. Green eyebrow = the audience ("Commercial Solutions · Prepared for [Buyer]").
2. **Section divider** — Navy background, large green "01" numeral. Section title: "What you need to know."
3. **Big-stat slide** — One number that earns the meeting. Ex: "410K sq ft," "93% on-time," "$40M in federal contracts."
4. **Three-column capability** — What you actually do. Print, fulfillment, contact center. One green border on the differentiator.
5. **Capability matrix** — Data slide. Contract vehicles, certifications, compliance. This is where procurement officers relax because you've proven you're credible.
6. **Testimonial / quote** — Primary Blue slide. Real client quote with real attribution. Builds trust without needing mission framing.
7. **Closing** — Primary Green slide with Primary Blue contact block. Action-oriented headline ("Let's build something" / "Ready when you are").

### Design rules

- Lead with capability. Mission enters only in Slide 9 or later if the buyer's RFP specifically asks about it.
- No clip art, no stock "handshake" photos, no icons-of-people-holding-hands.
- Photography should show facilities, production lines, or workforce — not clients receiving services.
- Max 3 weights on any slide (Regular, Bold, Black).
- One primary action per deck. "Schedule a conversation" is the default CTA.

### What breaks this recipe

- Opening with "Envision is a nonprofit that provides meaningful employment…" — deficit framing buries the pitch.
- Listing all eight program pillars — commercial buyers don't need Arts Center context.
- More than one green accent per slide — it stops being an accent.
- Generic icons on every slide — makes it look like a template.

---

## Recipe 2: A Landing Page for a Commercial Campaign

**Audience:** Enterprise buyers landing from an ad or email.
**Output:** Single-page HTML, mobile-responsive.

### Section sequence

1. **Hero — type-forward** (Pattern 01). Solid Primary Blue. Eyebrow, headline, short supporting copy, single green CTA.
2. **Stats band** (Pattern 03). 3-4 numbers proving scale. One stat in green as the hero metric.
3. **Capabilities grid** (Pattern 04). 3 feature cards summarizing what you do.
4. **Pull quote** (Pattern 05). Real client testimonial. Primary Blue, centered, plenty of whitespace.
5. **Compliance / data section** (Pattern 08). Navy background for contrast. Contract vehicles + certification chips.
6. **Full-width CTA** (Pattern 07). Primary Green band with Primary Blue headline and CTA.
7. **Footer** (Pattern 10). Navy.

### Spacing rhythm

- Section vertical padding: 128px desktop, 80px mobile (hero and quote); 96px desktop, 64px mobile (everything else).
- Never stack two sections without 48px+ rhythm between them.

### Hierarchy

- Hero h1: 72px Bold/Black, -0.045em tracking.
- Section h2s: 36-44px Bold.
- Card h3s: 20-22px Bold.
- Body: 16-18px Regular, 1.5 line-height.

### What breaks this recipe

- Multiple CTAs at equal weight ("Schedule a conversation" AND "Download the brief" AND "Watch the video" all as filled buttons). Pick one.
- Hero image instead of hero type. If the photo isn't spectacular, go type-only.
- Rounded pill buttons. 4px max radius, always.

---

## Recipe 3: A Mailchimp Email Campaign

**Audience:** Existing contacts, newsletter subscribers, customers.
**Output:** HTML email, 640px wide.

### Must-haves

- **Brand bar at top:** 24-32px padding, Primary Blue background, "ENVISION" wordmark in white.
- **Preheader text:** One sentence that completes the subject line. Hidden in the email but visible in inbox preview.
- **640px container max.** Any wider breaks in Outlook.
- **Table-based layout.** Emails use `<table>` for structure — divs break in many email clients.
- **Inline styles.** Many email clients strip `<style>` blocks. Inline everything critical.
- **Fallback fonts.** Montserrat is not preinstalled on most systems. Use web font loading + `Arial, Helvetica, sans-serif` fallback.

### Structure

1. Brand bar (blue, logo left-aligned)
2. Hero with eyebrow + headline (can be a color band or white with blue type)
3. Divider — 2px Primary Blue, 80px wide
4. Intro paragraph ("Hi {{FNAME}}, ...")
5. Stats block (3 stats max, table-structured)
6. Feature section with CTA button
7. Pull quote (Primary Green left border)
8. CTA band (Primary Green background, Primary Blue button)
9. Footer (Navy background, address, unsubscribe)

### Email-safe design rules

- No `background-image` on buttons — use colored cells.
- No SVG (support is spotty). Use PNG or text for logos.
- No CSS Grid or Flexbox (use tables).
- Buttons: padded `<a>` tags with inline styles.
- Images: always include `alt` text, always set dimensions explicitly.

### What breaks this recipe

- Using div-based layout (breaks in Outlook).
- Relying on webfont — always have Arial fallback.
- Three or more CTAs competing in one email.
- Multiple hero images — email is for quick scanning.

---

## Recipe 4: A One-Pager Capabilities Brief

**Audience:** Procurement officers, leave-behind after a sales meeting.
**Output:** Single-page PDF (8.5×11 letter) from HTML-to-PDF pipeline.

### Layout

**Top third** (header zone):
- Small "ENVISION" wordmark top-left.
- Eyebrow: "CAPABILITIES BRIEF · [DATE]" top-right in charcoal.
- Horizontal rule (2px Primary Blue).
- Headline statement (24-28px Primary Blue, Bold, title case).
- Subhead (14-16px charcoal, 2 lines).

**Middle third** (proof zone):
- 4-column stat block (big number in Primary Blue, small label in charcoal uppercase).
- Below that: 2- or 3-column capability breakdown with small icons or no icons.

**Bottom third** (validation + CTA):
- Certification chips (bordered Primary Blue pills — remember, chips can use 4px radius).
- Short case study callout (1 sentence quote + attribution).
- Contact block: email, phone, address.

### Print specifics

- CMYK color values from `tokens/colors.json`, not RGB hex.
- Minimum 11px type for any copy that must be readable in print.
- 0.5" margins at a minimum; 0.75" is better.
- Never bleed color blocks off the edge unless you're printing with bleed (add 0.125" bleed area).

### What breaks this recipe

- Cramming a full page of body copy. One-pagers are scanned, not read.
- Using web colors on a PDF (RGB will shift in print).
- Stock icon sets — they look templated.

---

## Recipe 5: A Program / Pillar Landing Page

**Audience:** BVI clients, families, referring professionals, donors.
**Output:** HTML landing page focused on one Envision pillar.

### Section sequence

1. **Hero — split** (Pattern 02). 7/5 split. Pillar eyebrow at 0.5em tracking. Headline centers the person's experience, not the organization's role.
2. **Intro narrative** — 600-720px max-width centered block. One paragraph establishing what the pillar is and who it's for.
3. **What we do** — Feature grid (Pattern 04). 3 cards summarizing the primary programs/services.
4. **Pull quote** — Real person, ideally a client or family member, not a staff member.
5. **Pillar-specific section** — This is where extended palette comes in. Arts Center might use Goldenrod. Mission Services might use Terracotta. Research Institute stays navy+green (more formal).
6. **Pre-footer CTA** (Pattern 07). Full-width callout with a pillar-appropriate action ("Explore what's possible," "Request an evaluation," "Apply to Level-Up").
7. **Footer** (Pattern 10).

### Differences from commercial work

- Photography is people, not facilities.
- Language centers the person's agency, not Envision's service delivery.
- Extended palette (Goldenrod, Terracotta, Violet, Forest Green) is welcome here — commercial work stays more restricted to blue+green.
- CTAs invite, rather than qualify ("Start the conversation" vs. "Schedule a capability review").

### Pillar-to-color shortlist

- Arts Center → Goldenrod accents
- Mission Services → Terracotta accents
- Research Institute → Navy + Green (clinical formality)
- Workforce Innovation → Primary Green accents, dominant
- Vision Rehabilitation Center → Bright Blue accents
- ECDC → Goldenrod + Terracotta (warmth for parents)
- Base Supply Center → Navy dominant (military formality)
- Continuing Education → Primary Blue + Violet (authoritative)

### What breaks this recipe

- Leading with what Envision does, instead of what thriving looks like for the person.
- Generic "we help people overcome..." language. (Use the voice rules in `guidelines/voice-and-tone.md`.)
- Stock photography. Pillar pages live or die by photography — use real program photos.
- Forcing commercial hierarchy onto mission work. Capability-first is wrong here.

---

## Using these recipes with Claude Code

When you start a new project, tell Claude Code which recipe applies:

> "Build me a landing page using Recipe 2 (commercial campaign landing page). The product is our new Federal IT fulfillment capability under SEWP VI."

That one sentence lets Claude Code pull:
- Section sequence from Recipe 2
- Hero pattern from `layout/section-patterns.html` Pattern 01
- Components from `components/component-library.html`
- Colors from `tokens/colors.json`
- Voice rules from `guidelines/voice-and-tone.md`

No more re-briefing the basics.
