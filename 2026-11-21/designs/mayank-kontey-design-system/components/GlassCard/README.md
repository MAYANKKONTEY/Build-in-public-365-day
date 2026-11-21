# GlassCard

The frosted panel that carries every content slide's words: `glass-surface` fill, `glass-blur` backdrop blur, `radius-glass` corners, 56px padding.

**Inside, top to bottom**

1. `.mk-card-mark`: `MK`, 24px bold, 70% white. Pinned to the top of the card.
2. `.mk-card-copy` (pushed to the bottom): `.mk-numword` (`ONE`) → `.mk-title` → `.mk-body`.

**Contrast: the rule that matters most**

The card is 42% grey, so what shows through decides whether the words are readable. White title needs the render behind the card at about `#7a7976` or darker. The 62% white body needs it near `ink-900` to reach 4.5:1. Over bare canvas nothing on the card passes. Compose the render so its darkest chrome sits directly behind the card (see the preview).

**Don't**

- Add borders, inner shadows or gradients to the card. The spec defines none.
- Put orange on the card except a CTA pill.
- Stack two cards on one slide.

The consumer provides: number word, title, body, and a render that is dark behind the card.
