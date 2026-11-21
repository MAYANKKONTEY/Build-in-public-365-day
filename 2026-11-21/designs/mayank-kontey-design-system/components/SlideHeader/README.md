# SlideHeader

The wordmark top-left and the slide number top-right, on every slide, set on the 72px safe margin.

- Wordmark: `MAYANK KONTEY` (or `MK` where space is tight), 26px bold, 0.14em tracking, uppercase.
- Slide number: `// 01`, 26px medium, two digits always.
- Colour follows what's behind it: white (`.mk-header`) over a dark part of the render, ink-700 (`.mk-header--ink`) over bare canvas. Never white on canvas (1.2:1).
- Keep the header identical across a carousel except the number.
