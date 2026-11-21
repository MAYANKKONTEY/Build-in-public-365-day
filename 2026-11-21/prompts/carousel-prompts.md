# Carousel Prompts (Mayank Kontey brand)

Three prompts: Prompt 1 sets up the design system once, Prompt 2 makes a carousel each time, Prompt 3 adapts it for LinkedIn. The design system built from Prompt 1 is in [`../designs/mayank-kontey-design-system/`](../designs/mayank-kontey-design-system/).

## Prompt 1 — Design system setup

Paste into **Claude Design → Set up your design system**, splitting it across the "Company name and blurb" and "Any other notes" fields.

```
Company name: Mayank Kontey

Blurb / design system:
Mayank Kontey is a personal brand teaching creators, founders and small businesses how to use AI creatively for branding, marketing, video editing and sales. Explanations are non-technical. This design system is for Instagram carousels (1080×1350) that break down AI workflows, marketing psychology and business ideas, and for repurposing them to LinkedIn.

Visual style:
- Clean, editorial, Apple-style minimalism
- Hero visual: chrome and frosted-glass 3D render imagery (soft organic glass shapes, light refraction)
- Backgrounds: warm off-white canvas (#EFEDE8 range)
- Accent: warm orange (#E8721E), used sparingly for CTAs and light reflections only
- Content cards: frosted glass panels (semi-transparent grey, rounded corners, background blur) layered over the renders
- High-contrast white type on glass panels

Color tokens:
- Accent: orange-600 #CF6212, orange-500 #E8721E (primary accent), orange-400 #F08534, orange-300 #F7A368, orange-100 #FBE3CE
- Paper: paper-100 #F6F4EF, paper-200 #EFEDE8 (canvas), paper-300 #E7E4DC
- Ink: ink-700 #46443E, ink-900 #1A1916 (rare dark type only)
- Glass surface: rgba(122,121,118,0.42), backdrop blur 18px, radius 28px
- Text on glass: #FFFFFF (primary), 62% white (muted), 42% white (faint)

Typography:
- Font: Geist, fallback "Helvetica Neue", Arial, sans-serif
- Cover headline: Extra Bold, 110–130px, leading 0.98, tracking -0.03em, UPPERCASE
- Eyebrow label: Medium, 28–30px, tracking 0.18em, UPPERCASE, 70% white
- Slide title: Bold, 56–64px, sentence case, leading 1.05
- Body: Regular, 30–34px, 62% white, max 3 lines
- Slide number: "// 01" style, Medium, 26px, top-right

Layout rules:
- Brand wordmark "MAYANK KONTEY" (or "MK") top-left, slide number top-right on every slide
- Cover: full-bleed glass render, eyebrow + headline bottom-left
- Content slides: one frosted glass card, lower 50–60% of frame; inside it a small brand mark, a number word (ONE, TWO…), title, body
- 72px safe margins; never place text over the busiest part of the render
- Carousel dots or swipe cue on the cover only
```

## Prompt 2 — Make a carousel

```
<role>
You are a senior social designer and copywriter for the Mayank Kontey brand. You turn one idea into a save-worthy Instagram carousel using the saved Mayank Kontey design system.
</role>

<context>
Audience: creators, founders and small-business owners aged 18–35 who want to use AI for branding, marketing and content but are not technical.
Topic: [e.g. "How to make sharper marketing for your brand with Claude"]
Key points I want covered: [paste 4–6 bullets or your rough notes]
Goal of this carousel: [saves / follows / DMs for "keyword"]
</context>

<task>
Create a [7]-slide Instagram carousel (1080×1350) using the saved design system exactly: glass render backgrounds, frosted glass content cards, Geist type, orange accent used only on the CTA.
</task>

<constraints>
- Cover headline: max 8 words, UPPERCASE, a clear promise or outcome. A vague headline kills the swipe.
- Each content slide teaches ONE idea: title max 7 words, body max 25 words. Glass cards can't hold more, and dense slides get skipped.
- Use plain language. Name real tools (Claude, ChatGPT, CapCut, Canva) instead of "AI tools".
- Banned words: delve, unlock, game-changer, revolutionize, leverage, "in today's fast-paced world".
- Vary the render crop/angle per slide so the carousel doesn't look repetitive.
- Don't invent stats or results. If a point needs proof I haven't given, write it as a method, not a claim.
</constraints>

<output_format>
Slide 1 (cover): eyebrow label + headline + "// 01"
Slides 2–[6] (content): number word (TWO, THREE…) + title + body + "// 0X"
Slide [7] (CTA): short recap line + one action ("Save this for your next post" / "Comment AI and I'll send the workflow") with the orange accent on the action
Then render all slides as designs.
</output_format>
```

## Prompt 3 — Resize for LinkedIn

Send as a follow-up after the Instagram carousel is approved.

```
Adapt this approved carousel for LinkedIn as a 1080×1080 document post. Keep the design system, copy and slide order. Re-crop each render so the glass card and text stay inside the square safe area, and reduce the cover headline size if it wraps past 4 lines. Then write a LinkedIn caption: a 1-line hook, 3 short lines of context, and a question to end on. No hashtags beyond 3.
```

**Model:** Sonnet works for Prompts 2 and 3. Use Opus only if the design system comes out inconsistent.

**Iterate:** after the first render, send *"Critique these slides for weak hooks, crowded cards and vague claims, then fix them."*
