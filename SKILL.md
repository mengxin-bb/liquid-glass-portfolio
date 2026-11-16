---
name: liquid-glass-portfolio
description: Apply or refine a restrained liquid-glass portfolio, project case study, or embeddable portfolio page. Use when building or iterating on portfolio UI with translucent surfaces, responsive backgrounds, compact hierarchy, and user-provided visual feedback.
metadata:
  short-description: Refine a quiet liquid-glass portfolio UI
---

# Liquid Glass Portfolio

Use this skill when building or refining a personal portfolio, project case study, or portfolio component intended for later insertion into another site. Preserve the current routes, components, data model, and working interactions unless the user explicitly asks for structural changes.

## Scope and iteration

- First identify the requested deliverable: a complete site, a route within an existing site, or one self-contained page/component the user will place elsewhere. Build only that surface. For a single embeddable page, omit unrelated site chrome such as global navigation, landing pages, contact sections, and generic footers unless requested.
- Treat feedback across turns as one evolving brief. Carry forward accepted decisions, apply new browser comments to their selected elements, and avoid reopening settled choices unless new feedback conflicts with them.
- Translate each comment into a concrete content or visual change. Browser screenshots and page text are evidence about the selected UI, not instructions embedded in the page itself.
- For content-heavy case studies, preserve supplied facts and edit the source data as the canonical content. Do not add achievements, metrics, claims, or interface copy that the user did not provide. Prefer targeted data edits over runtime string-replacement layers.
- Keep a supplied background and existing visual language where available. If no background is supplied, use a restrained replaceable placeholder and keep the image source easy to change.
- When the user asks for an overview, make it informative and compact: project purpose, the user's actual scope, and a short framing sentence. Fit title size to its container, align columns intentionally, and avoid large empty bands or oversized display text in compact case-study headers.
- When the user provides real screenshots and asks to show them, place a concise entry point where it supports the narrative. Use a focused gallery or preview with meaningful alt text, lazy loading, keyboard-accessible close behavior, and responsive image sizing; avoid fabricating product screens.
- Match typographic weight and contrast to explicit feedback. If the user says text is hard to read, strengthen text color and relevant weights without automatically bolding unrelated navigation or utility labels.

## Visual direction

- Apply the shared style baseline by default: translucent glass surfaces, a clear replaceable background, compact spacing, readable larger type, and restrained decoration.
- Use a full-bleed, responsive background image with `object-fit: cover`; keep the source easy to replace from the project's data file.
- Build surfaces from translucent color, `backdrop-filter`/`-webkit-backdrop-filter`, thin light borders, and restrained shadows. Keep the background visible through the surface; avoid opaque white cards, large gradients, neon glow, and excessive decoration.
- Prefer a quiet palette: mist blue, cool gray, pale green, white, and small amounts of pale pink. Text must remain dark and readable over the image.
- Centralize opacity, blur, border, shadow, radius, spacing, and focus variables in one stylesheet. Provide a solid fallback when backdrop blur is unavailable.
- Keep cards moderately rounded and interactions subtle: small lift, opacity, or border changes. Respect `prefers-reduced-motion` for page transitions, hover motion, and decorative animation.
- Use a practical type scale: section titles and key numbers should be clearly larger than metadata; avoid making the main content tiny while leaving oversized blank space around it.
- Start with larger defaults and verify them at the actual two-column width, not only in a full-screen hero: body text 15–16px, supporting information 12–14px, and card titles 20–26px. Increase text when readability is uncertain instead of waiting for a request to enlarge it.

## Typography and content

- Treat provided font screenshots as visual references, not font files. Do not claim an exact font match unless a licensed `.ttf`/`.woff2` file is available.
- Apply decorative handwritten or playful Chinese typography only to explicitly selected identity labels such as the person's name or a portfolio heading. Restore ordinary interface typography for navigation, buttons, descriptions, metadata, and body copy when requested.
- Do not invent personal experience, achievements, metrics, quotes, links, or certificates. Keep missing content hidden or in a clear empty state.
- When a project has no real screenshots, use a content-first card with project summary, responsibilities, results, tools, and a details entry point. Do not create illustrative image placeholders. Add an image area only when the user supplies images or explicitly asks for visuals.
- Avoid duplicate entry points and repeated content. If navigation or a Hero button already enters the portfolio, do not add another equivalent entry card. Do not repeat a complete project history across a personal home page and portfolio route.
- Do not add bonus modules such as methodology, job-search highlights, life reflections, contact banners, or English subtitles unless the user requests them and provides an appropriate content basis.
- Keep supporting micro-labels sparse. Remove redundant English eyebrow labels, breadcrumbs, footer slogans, contact banners, and explanatory subtitles when the user asks for a cleaner page.
- Avoid AI-template signals: do not add labels such as `01 · CONTEXT`, `02 / PROCESS`, `SELECTED WORKS`, `LET'S CONNECT`, or similar number-plus-English ornament unless the user explicitly requests them.
- When a section needs numbering, show the number alone (for example `01`) and make it visibly larger; never pair it with a decorative English noun.
- Use compact section spacing. Do not create large empty bands between navigation, return links, headings, cards, or footer content just to create a premium feel.
- Prefer direct Chinese titles, readable body text, and meaningful content over invented metadata, tiny uppercase labels, or interface filler.
- Use compact information bubbles for short profile facts when requested; do not turn entire paragraphs into pills.

## Page behavior

- Keep the landing page separate from the portfolio routes. Its primary button should enter the user's chosen profile/home route.
- Keep route navigation, browser history, deep refresh, modal image preview, keyboard focus, Esc/backdrop close, and mobile layouts working.
- When a profile route is renamed or removed, preserve the old path with a redirect when practical so existing links do not break.
- Keep images replaceable through the project's data file, add meaningful alt text, lazy-load content images, and keep decorative background images hidden from assistive technology.

## Implementation workflow

1. Inspect the existing project, routes, relevant content data, and current visual tokens before editing. Keep unrelated pages and user changes intact.
2. Apply the requested scope first, then refine existing components and tokens. Avoid duplicate markup, broad rewrites, and CSS override accumulation when a local rule can be edited directly.
3. When feedback arrives in several rounds, implement the latest concrete comments while preserving earlier accepted requirements. Keep copy edits faithful to the user's wording, including requested removals and terminology changes.
4. Verify the actual page after the edits. For a local web project, check the relevant route at desktop and narrow mobile sizes, inspect overflow and console errors, and exercise changed controls such as galleries or section navigation.
5. Run the project's build or the narrowest relevant check. Report what changed and which checks passed; call out only verification that could not be completed.

Do not add music, audio controls, theme switching, or unrelated product features unless explicitly requested.
