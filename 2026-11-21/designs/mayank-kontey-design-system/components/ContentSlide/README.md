# ContentSlide

Slides 02 onward: the render in the upper part of the frame and one frosted GlassCard in the lower ~53%, carrying one idea.

**Structure** (`.mk-slide` › `.mk-render` + `.mk-header` + `.mk-glass`)

- `.mk-render`: the same render family as the cover, recomposed so the object sits in the top half and its dark mass runs behind the card.
- `.mk-header`: wordmark + `// 02`. Use `.mk-header--ink` (ink-700) when the top band is bare canvas; plain `.mk-header` (white) only over a dark part of the render.
- `.mk-glass` placed by the slide: 72px from left, right and bottom, 720px tall (lower 53%; the spec allows 50–60%).

**Rules**

- One card per slide, one idea per card. Number words count the ideas (`ONE`, `TWO`…), not the slides.
- No swipe cue or dots on content slides.
- Body ≤ 3 lines. If it runs longer, split the idea across two slides.
- Never put the card over the busiest part of the render; move the render, not the card.

The consumer provides: the render, the slide number, the number word, title and body.
