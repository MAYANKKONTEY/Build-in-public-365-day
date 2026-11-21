# Mayank Kontey

Mayank Kontey is a personal brand that teaches creators, founders and small businesses how to use AI creatively for branding, marketing, video editing and sales. This system covers Instagram carousels (1080 × 1350) that break down AI workflows, marketing psychology and business ideas, and how to repurpose them for LinkedIn.

The look in one line: **a warm paper canvas, one chrome-and-glass render, one frosted card of words, and a single spark of orange.**

## Voice

- Non-technical. Explain the result, not the model. "Give the AI one post that worked" beats "provide a few-shot exemplar".
- Short sentences, active verbs, second person.
- Covers make one promise. Content slides teach one idea each.
- Skip hype words and filler: no "game-changer", "unlock", "delve", "revolutionary". No emoji on slides.
- Cover headline UPPERCASE. Everything else sentence case, except eyebrows, number words and the wordmark (uppercase, tracked).

## Visual foundations

**Canvas.** Every slide starts on `paper-200` (#EFEDE8). `paper-100` and `paper-300` are its light and shadow sides. Never pure white, never a dark background slide.

**The render.** The hero visual is a 3D render of soft organic glass and chrome shapes with visible light refraction, sitting on the paper canvas. One render family per carousel: the cover shows it full bleed; content slides recompose it so the object fills the upper part of the frame. Shapes, not scenes: no people, devices, logos or icons inside renders.

**Glass.** Words on content slides live on one frosted panel: `glass-surface` (42% warm grey), `glass-blur` 18px, `radius-glass` 28px. No borders, shadows or gradients on the card.

**Orange.** `orange-500` (#E8721E) appears in two places only: a call to act (swipe arrow, CTA pill) and light reflections inside the render. If orange is decorating, remove it. Never orange text, never an orange slide.

**Ink.** `ink-700` / `ink-900` are rare: slide chrome over bare canvas, a cover headline over a light render, and CTA labels.

## Color

| Token | Value | Use |
| --- | --- | --- |
| `paper-200` / `canvas` | #EFEDE8 | Slide background |
| `paper-100` · `paper-300` | #F6F4EF · #E7E4DC | Canvas light and shadow sides |
| `orange-500` / `accent` | #E8721E | CTAs and reflections only |
| `orange-600` · `400` · `300` · `100` | #CF6212 · #F08534 · #F7A368 · #FBE3CE | Reflection core, glow and falloff in renders; pressed CTA |
| `glass-surface` | rgba(122,121,118,.42) | Glass card fill |
| `on-glass` | #FFFFFF | Titles, cover headline |
| `on-glass-eyebrow` | 70% white | Eyebrows, number words |
| `on-glass-muted` | 62% white | Body on glass |
| `on-glass-faint` | 42% white | Decorative only (dots) |
| `ink-700` · `ink-900` | #46443E · #1A1916 | Rare dark type |

## Type

One family: **Geist** (Google Fonts), falling back to Helvetica Neue, Arial.

| Style | Size / weight | Leading · tracking | Case |
| --- | --- | --- | --- |
| `cover-headline` | 110–130px (120) · Extra Bold 800 | 0.98 · -0.03em | UPPERCASE |
| `slide-title` | 56–64px (60) · Bold 700 | 1.05 | Sentence case |
| `body` | 30–34px (32) · Regular 400 | 1.35 | Sentence case, max 3 lines |
| `eyebrow` (also number words) | 28–30px (28) · Medium 500 | 1.2 · 0.18em | UPPERCASE |
| `slide-number` | 26px · Medium 500 | 1.2 | `// 01` |
| `wordmark` | 26px · Bold 700 | 1.2 · 0.14em | UPPERCASE |

Sizes are at 1080px width. On a phone the slide shows at roughly 36% scale, so 32px body reads like 11–12px text. That is why body never goes below 30px and never runs past three lines.

## Slide anatomy

All slides: 1080 × 1350, 72px `safe-margin` on every edge, wordmark top-left, `// 0N` top-right.

**Cover (01)**

- Render full bleed.
- Bottom-left, inside the margins: eyebrow → 24px → headline (2–4 lines) → 48px → swipe cue.
- Type sits on the darkest, quietest part of the render.
- Carousel dots / swipe cue live here and nowhere else.

**Content (02 onward)**

- Render in the upper part of the frame.
- One glass card: 72px from left, right and bottom, 720px tall (≈53% of the frame).
- Inside the card: `MK` mark at the top; number word (`ONE`, `TWO`…), title and body anchored to the bottom.

**Final slide.** Same as a content slide, with a `CTAPill` under the body ("Save this for later", "Follow for more").

## Contrast

The glass is translucent, so whatever is behind the card decides whether the words are readable. Measured against WCAG (4.5:1 for body, 3:1 for large text):

| Render behind the card | White title | 70% eyebrow | 62% body |
| --- | --- | --- | --- |
| ≈ ink-900 (#1A1916) | 10.2:1 | 6.0:1 | **5.1:1 ✓** |
| ≈ ink-700 (#46443E) | 6.9:1 | 4.4:1 | 3.8:1 ✗ |
| ≈ #7A7976 mid grey | 4.4:1 | 3.0:1 | 2.7:1 ✗ |
| bare canvas (#EFEDE8) | 1.9:1 ✗ | 1.6:1 ✗ | 1.5:1 ✗ |

**The rule:** compose every render so its darkest chrome sits directly behind the glass card and behind the cover type. The light, airy part of the render goes above.

**Flag:** with the spec's values, 62% white body only passes over near-black chrome. If the renders come out lighter, the fix is to raise body to about 75% white or deepen the glass, not to shrink or bolden the text. This is left as the spec states until you decide.

Orange: text on `orange-500` is ink-900 (5.7:1). White on it is 3.1:1 and fails at body size.

## Imagery: making the render

Generate renders as 4:5 portraits (1080 × 1350) in an image model. A starting prompt:

> Abstract 3D render, soft organic shapes of frosted glass and polished chrome, light refracting through the glass, warm off-white studio background (#EFEDE8), one small warm orange (#E8721E) reflection, dark chrome mass in the lower half, soft shadows, minimal, editorial, no text.

For content slides, ask for the object in the upper half with dark chrome reaching into the lower half. Keep the same lighting and palette across one carousel so the slides read as a set.

## Repurposing for LinkedIn

- Keep the same 1080 × 1350 slides and export them as one PDF for a LinkedIn document post.
- Swap the last slide's CTA to a LinkedIn action ("Follow for weekly AI breakdowns").
- The caption carries more of the argument on LinkedIn; the slides stay identical.

## Using this system

- Colours, spacing, radius, blur and frame size are CSS variables from `tokens.css` (`--canvas`, `--glass-surface`, `--safe-margin`, `--glass-blur`…).
- Components are plain HTML + CSS classes in `components/bundle.css` (`.mk-slide`, `.mk-render`, `.mk-header`, `.mk-glass`, `.mk-cover-copy`, `.mk-swipe`, `.mk-cta`). No JavaScript.
- Author slides at full size inside `.mk-slide` and export each at 1080 × 1350. `.mk-render--cover` and `.mk-render--content` are placeholders; replace them with `background-image` on `.mk-render`.

## Assumptions

The brief defined colours, type, glass and layout. These were filled in and can be changed:

- Body line height 1.35; wordmark style (26px bold, 0.14em); `MK` mark size.
- Spacing steps 16 / 24 / 48 / 56px (only the 72px safe margin was given); card height 720px.
- Pill radius, swipe-cue design and the CTA pill.
- No logo file was supplied, so the wordmark is set in Geist. Add the mark under assets when you have one.
