# Conspiracy Party — Website

Self-contained, themed site for the conspiracy-theory party (Knives Out / murder-mystery vibe). Companion to the Obsidian project at `Vaults/Me/Projects/Conspiracy Party/`.

Multiple design directions live side by side so they can be compared before picking one.

## Live
Published on GitHub Pages: **https://joshuaangulo.github.io/conspiracy-party-site/** (repo: `joshuaangulo/conspiracy-party-site`). Pushing to `main` redeploys within ~30–60s.

## Structure
```
index.html                  ← chooser: links to each version
v1-dossier/index.html       ← Version 1 — "Declassified Dossier" (grungy, redaction bars, red stamps)
v2-twilight-zone/index.html ← Version 2 — "Twilight Zone" (B&W retro-TV, spiral, scanlines)
v3-red-velvet/index.html    ← Version 3 — "Red Velvet & Gold" (opulent gala, velvet crimson + gold)
v4-wes-anderson/index.html  ← Version 4 — "Wes Anderson" (symmetrical, color-blocked, Futura)
v5-knives-out/index.html    ← Version 5 — "Sleuthed" (vintage detective, Abril Fatface gold-on-espresso)
```

## View it locally
No build step, no dependencies — just open the chooser:

```bash
open index.html        # macOS — then click into a version
```

## Edit the event details
Each version keeps its details as plain text, flagged with HTML comments:
- **Date / Location / Dress** — the "Particulars" section (`<!-- EDIT THE EVENT DETAILS … -->`).
- **Presentation time limit** — Rule III (`<!-- EDIT THE TIME LIMIT … -->`). Replace `⟨ X ⟩ minutes`.
- **Event name** — search and replace `⟨ Event Name ⟩`.

## The game (current rules)
Theories are **assigned in advance** so guests can prepare a real, quality presentation. Each presentation has a **strict time limit** and may use **any medium** (slides, film, props, performance). The room votes; the most convincing wins a valuable prize. (Source of truth: the Obsidian "Game Design and Rules" note.)

## Collect real RSVPs
Each version's form runs in **demo mode** by default (shows a confirmation, stores nothing). To collect responses, get a free [Formspree](https://formspree.io) endpoint and paste it into the config near the top of that page's `<script>`:

```js
const RSVP_ENDPOINT = "https://formspree.io/f/xxxxxxx";
```

## Design notes
- **v1 — Declassified Dossier:** Special Elite (typewriter) + Courier Prime — now styled as an authentic typed/declassified document (Oswald dropped); film grain, red-string draw-in, tap-to-declassify redactions, red CLASSIFIED stamp.
- **v2 — Twilight Zone:** Anton (stark condensed caps) + Jost; black-and-white retro-TV — a spinning generated spiral, starfield, CRT scanlines + flicker, vignette; Rod-Serling-cadence copy; RSVP framed like a TV screen. (Replaced the earlier "Glass Onion" v2.)
- **v3 — Red Velvet & Gold:** Playfair Display (gold-gradient serif) + EB Garamond; deep velvet-crimson background (drape + grain), metallic gold, rotating knife-wheel sunburst, gilded double-line frames, gold-diamond (◆) dividers. Inspired by the Knives Out Collection poster.
- **v4 — Wes Anderson:** Jost (Futura-style geometric caps) + Lora; symmetrical, color-blocked panels in muted Knives-Out pastels (hunter green, oxblood, mustard, dusty rose, cream); chapter cards (I–IV), thin double-line frames, crossed-knives crest, deadpan-whimsical copy.
- **v5 — Sleuthed (actual Knives Out / Agatha Christie):** Abril Fatface (high-contrast Victorian fat-face, modeled on the "Sleuthed AF" reference) + EB Garamond; gold/amber on dark espresso brown, magnifying-glass crest, gold-diamond dividers, vintage-detective copy.
- All: responsive, `prefers-reduced-motion` fallback, demo-mode RSVP.

## History
Earlier explorations that were replaced: a Spectral "Knives Out" v3, a blackletter "Wake Up Dead Man" v3, a "Cheeky Gothic" v4, and a "Glass Onion" v2. Current lineup is v1–v4 (contiguous). A v5 "actual Knives Out / Agatha Christie font" is planned.
