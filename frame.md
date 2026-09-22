---
version: alpha
name: Warden — Frame (video / frame layer)
description: >
  Frame spec for the Warden launch video. Source of truth is the Figma file
  "Warden", page "01 · Design system" (RFPKLtSSZjQMHy9XaOOSqp): the palette
  frame 155:4 "Color con una función", the typography frame 257:100, and the
  component sections 302:35-302:38. Read through the Figma connector on
  2026-09-20; raw reads cached in .media/figma-cache/. Light Intermedio only:
  the film has no dark register.
unit: the frame — 1920×1080 primary
principle: colour with a function · graphite to act, red/green/yellow to understand · one thing the eye sees first

colors:
  # — Light Intermedio: the whole film is light mode (owner's call, 2026-09-20) —
  canvas: "#F4F5F4"
  ink: "#22282A"
  ink-body: "#444D4F"
  muted: "#656E6F"
  surface-page: "#FFFFFF"
  surface-subtle: "#F4F5F4"
  surface-selected: "#E6E8E6"
  line-hairline: "#E7EAE8"
  line-control: "#DDE2DF"
  graphite: "#22282A"
  graphite-ink: "#FFFFFF"
  # — states. Figma "Color con una función", re-read 2026-09-21: the tinted
  #   ink/bg badge pairs are gone. A state is a signal-coloured bullet beside a
  #   label in ink. Mint was #26B88A and yellow #F5D547 until that date. —
  signal-red-danger: "#FF3B5C"
  signal-green-success: "#34D399"
  signal-yellow-warning: "#FDE047"

typography:
  # — reading ramp: Inter, Figma "Warden v2 / Review", scaled from a 1440 artboard to the frame —
  body:    { fontFamily: "Inter", cqw: 1.5, weight: 400, lineHeight: 1.47 }
  body-strong: { fontFamily: "Inter", cqw: 1.5, weight: 500, lineHeight: 1.47 }
  lead:    { fontFamily: "Inter", cqw: 1.9, weight: 400, lineHeight: 1.45 }
  ui:      { fontFamily: "Inter", cqw: 1.4, weight: 500, lineHeight: 1.38 }
  caption: { fontFamily: "Inter", cqw: 1.4, weight: 400, lineHeight: 1.33 }
  label:   { fontFamily: "Inter", cqw: 1.0, weight: 500, lineHeight: 1.27 }
  mono:    { fontFamily: "Geist Mono", cqw: 1.5, weight: 400, lineHeight: 1.55 }
  mono-lg: { fontFamily: "Geist Mono", cqw: 2.2, weight: 400, lineHeight: 1.45 }
  # — display ramp: Manrope SemiBold, Figma "Display / Page" (600, tracking -5%) —
  h3:      { fontFamily: "Manrope", cqw: 2.8, weight: 600, lineHeight: 1.2, tracking: "-0.03em" }
  h2:      { fontFamily: "Manrope", cqw: 4.2, weight: 600, lineHeight: 1.12, tracking: "-0.04em" }
  h1:      { fontFamily: "Manrope", cqw: 5.8, weight: 600, lineHeight: 1.05, tracking: "-0.05em" }
  display: { fontFamily: "Manrope", cqw: 7.6, weight: 600, lineHeight: 1.0, tracking: "-0.05em" }

spacing:
  pad-x: "7cqw"
  pad-y: "6cqw"
  gap-lg: "3.5cqw"
  gap-md: "2cqw"
  gap-sm: "1cqw"
  radius: "0.55cqw"
  radius-composer: "1.5cqw"

components:
  ground:
    backgroundColor: "{colors.canvas}"
    description: "Light Intermedio subtle grey (#F4F5F4), the console's own sidebar and hover grey — so a white product card still reads as a surface on it. Flat: no gradient, no vignette, no glow. Its own full-duration clip layer, never the composition root."
  statement:
    typography: "{typography.h1} / {typography.display}, {colors.ink}"
    description: "One declarative sentence with a full stop. Sentence case. Never 'you'. Lines reveal one at a time from a clipped mask."
  product-card:
    backgroundColor: "{colors.surface-page}"
    border: "1px solid {colors.line-hairline}"
    borderRadius: "{spacing.radius}"
    description: "The product as it ships: a white surface on the subtle-grey ground, separated by a hairline only. Rebuilt from the Figma components, not screen-recorded. No drop shadow, no drawn browser window."
  row-rule:
    figma: "264:163 Row / Rule"
    layout: "rule sentence in {typography.body-strong} {colors.ink}; scope as an outlined role label; effect as coloured text with no box (table-row law)"
    description: "One per rule the compiler produced."
  rule-proposal:
    figma: "263:91 Rule proposal / Activation status, 291:2027 Menu actions"
    description: "A drafted rule before activation — the card a broad instruction splits into."
  composer:
    figma: "263:479 Composer"
    borderRadius: "{spacing.radius-composer}"
    description: "Where the administrator types the policy sentence. The one rounded thing in the system (22px at source), because it nests attach and send."
  badge-verdict:
    figma: "229:11 Badge / Verdict (Blocked · Held · Allowed), 210:393 Badge / Effect (Block · Escalate · Warn · Active)"
    typography: "{typography.ui}, {colors.ink}"
    layout: "a round bullet in the signal colour, then the label in ink. No fill, no border — in table rows, cards and detail alike."
    variants: "Block / Blocked {colors.signal-red-danger} · Active / Allowed {colors.signal-green-success} · Escalate / Warn / Held {colors.signal-yellow-warning}"
    description: "Colour never carries a state alone: mint and yellow are unreadable as text on white, so the word is always ink. At statement scale the same pattern holds — a big bullet, then the word. Its arrival is the event of the frame."
  tint:
    backgroundColor: "signal colour at ~10%"
    description: "Figma allows a 10% signal fill only for feedback messages and confirmation containers, never for a badge. The film uses it twice: the full-frame ground under the block, and under the allow."
  label-role:
    figma: "210:404 Label / Role"
    description: "Outlined hairline, no fill, text in the role's colour. Identity, never severity; Everyone is neutral."
  button:
    figma: "258:119 Button, 378:1962 Button / Compact"
    description: "Primary is graphite filled, one per view; secondary is quiet with a border."
  term:
    backgroundColor: "{colors.surface-page}"
    border: "1px solid {colors.line-hairline}"
    borderRadius: "{spacing.radius}"
    header: "one-line bar, hairline below, mono label left ('claude code'). No traffic-light dots, no fake buttons."
    body: "{typography.mono} in {colors.ink-body}; the ⛔ line in {colors.ink} bold, the rule line in {colors.ink-body}; the ⛔ glyph is the only colour"
    description: "Not a Figma component — the employee's own terminal, drawn light like everything else, where the block is seen. Built from the same hairline/radius atoms. The label exists so the viewer knows the block happens inside their tool, not a Warden app."
  mask:
    typography: "{typography.mono}"
    description: "A masked secret as the product renders it, [API_KEY], {colors.muted} inside a 1px {colors.line-control} box."
---

# Warden — Frame

## Overview

"Color con una función." Graphite to act; Light Intermedio for surfaces; red,
green and yellow to understand. The whole film is light: a subtle-grey ground
(#F4F5F4) with white product surfaces on it, graphite ink, hairlines. It looks
like the product because it is the product's own palette. Saturation exists
only where a verdict does: never for emphasis, a logo, or a button — on a page
this quiet, the first red is loud.

Manrope SemiBold is the display voice (Figma "Display / Page": 600, −5%
tracking). Inter is everything read at UI scale. Geist Mono is the machine:
prompts, rule ids, terminal output, hashes.

## The Frame

- **Squint** — one thing the eye sees first, decided on purpose. On a verdict frame it is the colour.
- **Silence** — statement frames read 50% empty or more.
- **Restraint** — a frame with no verdict on it has no saturated colour at all (role labels excepted, and only inside a product card).
- **Reference** — Linear and Vercel launch films; the Figma file itself, Stripe and Linear light-mode films. Failure looks like a cybersecurity ad: shields, locks, red scanlines, glitch.

**The container law.** Every frame ground sets `container-type: size`; all
frame-relative units are `cqw`/`cqh`. Hairlines stay 1px.

**Scale.** Figma components are drawn for a 1440-wide console at 13-15px. In the
frame they are shown large: a product card is scaled so its body text lands at
≥ 1.5cqw (about 2× source). Scale the whole component; never restyle it.

**Legibility floor.** Load-bearing sans ≥ 1.4cqw; mono that must be read ≥ 1.5cqw.
A prompt the viewer has under two seconds for is `mono-lg`.

## Copy law

- English, all of it — statements, prompts, the admin's sentence, rule text. No Spanish on screen (owner's call, 2026-09-20; this departs from the landing, which keeps prompts in Spanish).
- Every statement is one declarative sentence with a full stop. None says "you".
- No praise adjectives. No accuracy figures. No "sandbox". No "blocks everything".
- Judging stays on the machine; say "judging", not "everything".

## Shapes

8px corners (0.55cqw) on everything with a box. **No pills.** The composer is
the single exception at 22px. No drop shadows on the frame; the Figma Menu
shadow is the only elevation in the system and no frame uses a menu.

## Composition rules

### Do

- Left-align to one rail at `pad-x` on statement and component frames; centre only the opening line and the closing lockup.
- Carry an element across a cut when the story says it is the same thing (the prompt in frame 1 is the prompt blocked in frame 4).
- Reveal lines from a clipped mask, upward, one at a time.
- Verdicts are symbol plus word, as in Figma. Never colour alone.

### Don't

- No colour without a verdict. No glow, bloom, particles, glitch, scanlines, grid floors.
- No icons standing in for ideas (no shield, no lock). The mark appears only in the lockup.
- No decorative mono. No uppercase sans. No two display moments in one frame.

## Numerals & Claims (hard rule)

Never invent a figure. This video shows no percentages at all.

## Font loading

Local files only, never the network. Paste into every frame:

```html
<style>
@font-face{font-family:"Manrope";font-weight:200 800;font-style:normal;font-display:block;src:url("assets/fonts/Manrope-Variable.ttf") format("truetype");}
@font-face{font-family:"Inter";font-weight:100 900;font-style:normal;font-display:block;src:url("assets/fonts/Inter-Variable.ttf") format("truetype");}
@font-face{font-family:"Geist Mono";font-weight:100 900;font-style:normal;font-display:block;src:url("assets/fonts/GeistMono-Variable.ttf") format("truetype");}
</style>
```
