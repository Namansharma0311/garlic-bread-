# Glug & Grate No. 7 🧄🧀

A single-page, self-contained website featuring a cheesy garlic oil bottle
that tips over and spills when you flip a toggle switch.

## Files

- `garlic-spill.html` — the entire site (HTML, CSS, and JS in one file, no
  external dependencies or build step required).

## How to run it

Just open `garlic-spill.html` in any modern web browser (double-click it,
or drag it into a browser tab). No server, install, or internet connection
needed.

## What it does

- A hand-drawn SVG bottle labeled "Glug & Grate No. 7" sits on the page.
- A **Steady / Spilling** toggle switch sits below it.
- Flipping the toggle:
  1. Rotates the bottle ~108° like it's tipping over.
  2. Grows an oil "stream" pouring out of the neck.
  3. Expands a puddle on the counter beneath it.
  4. Scatters 14 small garlic cloves, cheese shreds, and basil flecks
     outward with randomized direction and rotation.
  5. Shows a random deadpan status message (e.g. *"This was, technically,
     avoidable."*).
- Flipping it back resets the bottle upright and clears the mess.

## Tech details

- **No dependencies** — plain HTML/CSS/JS, no frameworks or libraries.
- **CSS-driven animation** — a single `.spilled` class toggled on the
  `#stage` container drives the bottle rotation, stream growth, and puddle
  scale via CSS transitions.
- **JS-driven bits** — clicking the toggle calls `spawnBits()`, which
  dynamically creates small SVG elements (clove / cheese / basil shapes)
  and animates them via a `@keyframes drop` rule using randomized
  `--dx`, `--dy`, and `--rot` CSS custom properties.
- **Accessible** — the toggle is a real `<button role="switch">` with
  `aria-checked`, and all animations are disabled under
  `prefers-reduced-motion: reduce`.

## Customization ideas

- Swap the oil color/gradient for a cheese-sauce look.
- Add a sound effect on spill.
- Make the bottle auto-spill on page load or on a timer/loop.
- Add more garnish shapes (chili flakes, parsley, parmesan curls).
