---
workflow: product-launch-video
flow: automation
storyboard: yes
message: "Write the policy in one sentence. It is enforced on every prompt, on the machine."
destination: x-and-youtube-launch-post
aspect: 1920x1080
language: en
audience: "team lead / PM / CEO evaluating; the technical person it gets forwarded to"
length: 60s
angle: problem-to-mechanism
narration: no
---

## Intent

Launch video for Warden, a local AI gateway: an administrator writes policy in
plain language and every employee prompt is checked against it before it
reaches Claude Code or ChatGPT, on the employee's own laptop. YC-launch-style
motion piece: kinetic type plus the product's real components, no voice-over,
music bed. Sell, not tour. Calm, exact, a little severe — the landing's tone:
declarative sentences with a full stop, no praise adjectives.

Six beats, agreed with the owner:

1. Problem — a prompt carrying customer data and an API key gets sent.
2. Bad options — ban AI, or trust everyone. Both struck through.
3. The mechanism — the admin types "make sure no one leaks data" and the sentence
   splits into five rule cards (customer contacts, credentials, unreleased
   financials, source code, internal documents). This is the hero shot.
4. The block — the same prompt from beat 1 is stopped in the terminal with the
   rule id. (The brief also had a secret masked and an honest request allowed
   here; both were cut later — see STORYBOARD.md, v7 and v23.)
5. Why believe it — judging never leaves the machine; no model is ever asked
   for an ALLOW; the audit keeps hashes, never prompt text.
6. CTA — download the installer. Lockup.

## Assets

- ../operations-aleph-landing/brand/warden-lockup-light.svg (#141414, for light grounds), warden-mark.svg, warden-wordmark.svg — logo, CTA and opening.
- ../operations-aleph/web/assets/fonts/Manrope-Variable.ttf — the console's typeface (OFL), bundled locally so renders are deterministic.
- ../operations-aleph/web/styles/*.css and ../operations-aleph-landing/landing/styles.css — token and component source (rule card, verdict chip, `.term` block). Components are rebuilt in HTML from these, not screen-recorded.

## Customizations

- No website capture: the product is a desktop app and the design system is local. Tokens come from the Figma file RFPKLtSSZjQMHy9XaOOSqp, page 01 · Design system.
- Build order: storyboard, then frame 3 alone as the style proof, then the rest.
- Deliver a 4K render as well as 1080p once approved.

## Notes

- Saturation only on a real verdict (Figma: signal red, cool green, clear yellow); everything else greyscale. Mono is the machine, sans is us. Hairlines and flat sunken surfaces; no shadows, no gradients, no drawn browser windows, no traffic-light dots on the terminal.
- All copy in English, prompts and the admin sentence included (owner, 2026-09-20). The five rules were measured on the Spanish sentence "hacé que no leakeen datos"; the English sentence on screen is its translation.
- Light mode throughout: Figma Light Intermedio, ground #F4F5F4, white surfaces. No dark register (owner, 2026-09-20).
- Do not show accuracy numbers (one run behind them). Do not claim the hooks are verified end to end. Never say "sandbox" or "blocks everything".
- What may leave the machine is compilation, only if the admin chooses it; judging never does. Say "judging", not "everything".
- Music: not resolved. HeyGen not signed in and local MusicGen deps are missing; owner to sign in or supply a track. Frames are built silent-safe until then.
