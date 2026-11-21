# CoverSlide

Slide 01: a full-bleed glass/chrome render with the eyebrow and headline bottom-left, and the only swipe cue in the carousel.

**Structure** (`.mk-slide` › `.mk-render` + `.mk-header` + `.mk-cover-copy`)

- `.mk-render` full bleed. Set `background-image` to the real render; `.mk-render--cover` is a placeholder only.
- `.mk-header`: wordmark `MAYANK KONTEY` top-left, `// 01` top-right, both on the 72px safe margin.
- `.mk-cover-copy`: `.mk-eyebrow` (2–4 words) → `.mk-headline` (UPPERCASE, 2–4 lines, 110–130px) → `.mk-swipe`.

**Rules**

- The headline sits on the darkest, calmest part of the render. Never over the specular highlight or the orange reflection.
- White headline needs a dark region behind it (ink-700 or darker). If the render is light there, add `.mk-cover-copy--ink` (ink-900 headline, ink-700 eyebrow) rather than adding a scrim.
- Headline 6–9 words. If it needs a fourth line at 110px, the line is too long: cut words, don't shrink.
- One promise per cover. The eyebrow names the topic (`AI FOR CREATORS`, `MARKETING PSYCHOLOGY`), the headline says what the reader gets.

The consumer provides: the render, the eyebrow, the headline, and the number of dots (= slide count).
