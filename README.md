# SOS 110 — Chapter 3 Web Slideshow

A click-through web version of the Chapter 3 ("Matter and Energy: What Are the
Building Blocks of Sustainability?") slides — 21 slides.

This folder is **self-contained** — everything it needs is inside it (only Google
Fonts, the Firebase SDK, and the embedded energy calculator come from public URLs).

## Contents
- `index.html` — the slideshow (open this)
- `media/` — slide images
- `firebase-config.js` — Firestore config for the live class interactives
- `.nojekyll` — tells GitHub Pages to serve all files as-is

## Live interactives

Four **Fact-or-Fiction True/False polls** (slides 4–7) and one **opinion poll**
embedded on the "Mining Garbage for Plastic" slide (slide 12) sync across every
open copy through Firebase Firestore.

**Open the projected copy with `?host` appended to the URL:**

```
https://ryanpcornell.github.io/sos110-chapter-3/?host
```

Students use the plain URL (no `?host`). On the host copy the vote buttons are
hidden and you get:

| Slide | Host controls |
|---|---|
| 4–7 (Fact or Fiction) | **Reveal answer** (flashes TRUE/FALSE) · **Reset results** |
| 12 (Biddle's question) | **Reset results** |

Other slides also include self-contained interactives that need no backend: a
**Build-an-Atom** builder (slide 10), an animated **Photosynthesis** reaction
(slide 15), the embedded **Vehicle Energy Flow** 1st-Law calculator (slide 17,
from ryanpcornell.github.io/energy/), and an interactive **10% Rule energy
pyramid** (slide 20).

### Keyboard
`←` / `→` navigate · `F` fullscreen · `O` slide menu

## Re-building this bundle

The deck is generated from `_deck-builder/chapter3.py` (not stored in this repo):

```bash
cd "…/Web Apps/_deck-builder"
DECK_OUT="…/Web Apps/chapter-3-web/index.html" python3 chapter3.py
```

(Then copy `Chapter 3 Slideshow/media/` and `firebase-config.js` into this folder
if any images or the Firebase config changed.)

## Hosting on GitHub Pages

Upload the *contents* of this folder to the repo root (so `index.html` is at the
top level), then **Settings → Pages → Source: Deploy from a branch → `main` /
`(root)`**.
