# Conspiracy Party — Website

Self-contained, themed site for the conspiracy-theory party (Knives Out / murder-mystery vibe). Companion to the Obsidian project at `Vaults/Me/Projects/Conspiracy Party/`.

Multiple design directions live side by side so they can be compared before picking one.

## Structure
```
index.html              ← chooser: links to each version
v1-dossier/index.html     ← Version 1 — "Declassified Dossier" (grungy, redaction bars, red stamps)
v2-glass-onion/index.html ← Version 2 — "Glass Onion" (minimal, gold-on-black, refined serif)
v4-red-velvet/index.html    ← Version 4 — "Red Velvet & Gold" (opulent gala, velvet crimson + gold)
v5-wes-anderson/index.html  ← Version 5 — "Wes Anderson" (symmetrical, color-blocked, Futura)
```

## View it
No build step, no dependencies — just open the chooser:

```bash
open index.html        # macOS — then click into a version
# or open one directly:
open v2-glass-onion/index.html
```

## Edit the event details
Each version keeps its details as plain text, flagged with HTML comments:
- **Date / Location / Dress** — the "Particulars" section (`<!-- EDIT THE EVENT DETAILS … -->`).
- **Presentation time limit** (v2) — Rule III (`<!-- EDIT THE TIME LIMIT … -->`). Replace `⟨ X ⟩ minutes`.
- **Event / operation name** — search and replace `⟨ Event Name ⟩` / `TRUST NO ONE`.

## The game (current rules)
Theories are **assigned in advance** so guests can prepare a real, quality presentation. Each presentation has a **strict time limit** and may use **any medium** (slides, film, props, performance). The room votes; the most convincing wins a valuable prize. (Source of truth: the Obsidian "Game Design and Rules" note.)

## Collect real RSVPs
Each version's form runs in **demo mode** by default (shows a confirmation, stores nothing). To collect responses, get a free [Formspree](https://formspree.io) endpoint and paste it into the config near the top of that page's `<script>`:

```js
const RSVP_ENDPOINT = "https://formspree.io/f/xxxxxxx";
```

## Deploy (free, static)
- **Netlify Drop** — drag the folder onto <https://app.netlify.com/drop>.
- **Vercel** — `vercel` in this folder.
- **GitHub Pages** / **Cloudflare Pages** — connect a repo, no build command.

## Design notes
- **v1 — Declassified Dossier:** Oswald / Special Elite / Courier Prime; film grain, red-string draw-in, typewriter intro; signature interaction = tap-to-declassify redactions.
- **v2 — Glass Onion:** Cormorant Garamond + Jost; near-black + ivory + antique gold; drifting spotlight, concentric "glass onion" rings, roman-numeral rules; restrained, mysterious.
- **v4 — Red Velvet & Gold:** Playfair Display (gold-gradient serif) + EB Garamond; deep velvet-crimson background (subtle drape + grain), metallic gold, a rotating knife-wheel sunburst behind the hero, gilded double-line frames, gold-diamond (◆) dividers. Opulent red-carpet gala, inspired by the Knives Out Collection poster. (Replaced the earlier "Cheeky Gothic" v4.)
- **v5 — Wes Anderson:** Jost (Futura-style geometric caps) + Lora; symmetrical, color-blocked panels in muted Knives-Out pastels (hunter green, oxblood, mustard, dusty rose, cream); chapter cards (I–IV), thin double-line frames, crossed-knives crest, deadpan-whimsical copy.
- All: responsive, `prefers-reduced-motion` fallback, demo-mode RSVP.

> The dark "Wake Up Dead Man" v3 was removed; v5 (Wes Anderson) is the current addition. Versions are intentionally non-contiguous (v1, v2, v4, v5).
