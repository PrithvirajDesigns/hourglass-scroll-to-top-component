# Hourglass Scroll-to-Top

A floating scroll-to-top button shaped like an hourglass. The sand runs as you
scroll, and the glass flips when you change direction. On hover it turns into
an up arrow, and clicking it scrolls back to the top.

## Features

- **Scroll-driven sand:** the upper bulb empties in proportion to how far you
  are through the page. At the bottom the sand is a triangle in the lower bulb.
- **Flips on direction change:** scroll up and the glass turns over, the sand
  settles at the new bottom, then drains as you scroll back up.
- **Hourglass to arrow:** hovering or focusing the button swaps the hourglass
  for an up arrow with a short crossfade.
- **Appears after scrolling:** hidden at the top, it fades in after 200px
  (configurable) and fades out when you return.
- **Accessible:** it's a real `<button>` with an `aria-label`, a visible focus
  ring, keyboard support, and `prefers-reduced-motion` support (still glass,
  no flipping).
- **Touch friendly:** a tap scrolls straight to the top, with no hover needed.
- **Lightweight:** inline SVG, CSS transitions, a passive scroll listener
  throttled with `requestAnimationFrame`, and no dependencies.

## Usage

Copy `HourglassScrollTop.jsx` and `HourglassScrollTop.css` into your React
project, then render it once in your layout:

    import HourglassScrollTop from "./HourglassScrollTop";

    <HourglassScrollTop />

### Props

| Prop        | Default          | Description                          |
| ----------- | ---------------- | ------------------------------------ |
| `threshold` | `200`            | Pixels scrolled before it appears    |
| `label`     | `"Scroll to top"`| Accessible name for the button       |
| `className` | `""`             | Extra class on the button            |

### Styling

Position, size and colours are set with CSS variables (`--hgst-size`,
`--hgst-offset-x`, `--hgst-offset-y`, `--hgst-z`, `--hgst-bg`, `--hgst-fg`).
The defaults are a `#121212` button with a white hourglass.

## Demo

Open `index.html` for a standalone demo page. To run the source project:

    npm install
    npm run dev

## Tech

React, CSS, inline SVG.
