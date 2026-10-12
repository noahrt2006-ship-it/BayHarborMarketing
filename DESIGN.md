# Whitetail Media · Design system

Modern northern Michigan × digital craft × premium minimalism.
Quiet, confident, precise. Color is an accent, never decoration. All tokens live in `:root` at the top of `index.html`.

## Color
| Token | Value | Use |
|---|---|---|
| `--paper` | `#F6F4EE` | Default page (warm ivory) |
| `--ivory` | `#EFECE3` | Alternate light section, hover wash |
| `--ink` | `#0F100E` | Text, primary buttons |
| `--char` | `#151714` | Dark sections (Work, About, footer, care plan) |
| `--forest` | `#2F4738` | Button hover fill, highlight contour, mock site |
| `--moss` | `#8A9A8C` | Accents on dark |
| `--mute` / `--stone` | `#5F625B` / `#8D8E86` | Secondary / tertiary text |
| `--blaze` | `#D2552A` | The one signal color: location pin, focus ring, input focus line |
| `--line` / `--line-2` | ink at 10% / 20% | Hairlines and rules |

Sections resolve color through surface tokens (`--bg --fg --fg-2 --rule --rule-2`); `.dark` swaps them.

## Type
- Sans: **Geist** (300–700). Display at weight 500, tracking -0.045 to -0.058em.
- Accent: **Instrument Serif** italic, one or two words per headline.
- Labels: **Geist Mono** 11px, uppercase, +0.09em, tabular numbers.

| Role | Size |
|---|---|
| Hero | `clamp(3rem, 9.3vw, 10.5rem)` / 0.9 |
| Section XL | `clamp(2.6rem, 6.6vw, 7rem)` / 0.96 |
| L | `clamp(2rem, 4.2vw, 4.4rem)` |
| M | `clamp(1.55rem, 2.5vw, 2.4rem)` |
| Lead | `clamp(1.15rem, 1.45vw, 1.4rem)` / 1.45 |
| Body | 17px / 1.55 |

## Space, grid, shape
- 4pt scale: 4 8 12 16 24 32 48 64 96 128. Section padding `clamp(112px, 13vw, 208px)`.
- 12-column grid, gap `clamp(16px, 2vw, 28px)`, max width 1520, gutter `clamp(20px, 4.2vw, 64px)`.
- Radii: 8 / 16 / 28 / pill. No drop shadows except the floating nav and the browser mock.

## Components
- **Section header**: hairline rule that draws in, `01 / Services` mono label left, aside label right, XL headline, lead on the right.
- **Buttons**: pill, 54px, uppercase 12px. Hover: forest fill rises from below, label rolls up, arrow nudges right. Press scales to 0.965.
- **Links**: underline draws left to right on hover, arrow shifts.
- **Lists**: hairline-separated rows with a small forest dot.
- **Form**: underline fields with floating labels and a blaze focus line; needs are pill toggles.
- **Nav**: full-width at top, compacts into a floating blurred pill after 60px of scroll; a soft indicator slides to the active section; the pill turns dark over dark sections.
- **Mobile menu**: full-screen dark curtain, oversized links rising in sequence, CTA + phone + email + local time.
- **Service rows**: oversized number + title, a live visual (mini site that assembles; care dashboard with status bars), ticks, price, CTA.
- **Build sequence**: pinned scroll section; Layout, Brand, Content, Launch each change the browser mock, then a phone joins.
- **Case study**: Desktop / Tablet / Phone toggle with a sliding indicator; the whole case is one link.
- **Timeline**: Scout, Build, Launch, Grow on a rail that fills as you scroll, each with a line drawing.
- **Pricing**: two plan cards joined by a "+", prices count up, one-line total underneath.
- **Map**: Lower Peninsula drawn from real coordinates, graticule, Iosco County outline, Tawas City pin.
- **Team**: two-person studio; headline plus one statement, no portraits.
- **Form states**: inline errors, valid ticks, and a dark "Thank you" panel that wipes in.

## Opening shot
- The page opens on a desk scene (one WebGL canvas, real camera perspective, textures generated in canvas; the hero sits on top with a single 2D transform): oak desk, a 27" display, keyboard, mouse, mug, forest-linen notebook, a framed Tawas Bay contour print, late window light with a white pine shadow.
- Scrolling dollies the camera toward the monitor; the screen is the real hero, so the last frame is the site itself. Phones get a pivoted (portrait) display.
- Loader: the Whitetail Media logo / "Loading experience" on char, then the room fades up from black.
- Reduced motion, no JS, or `?flat` in the URL: plain hero, no scene.

## Motion
- Easing: `--e-out cubic-bezier(.16,1,.3,1)` for arrivals, `--e-io cubic-bezier(.77,0,.18,1)` for curtains.
- Load order: grid lines, nav, headline lines (staggered 120ms), meta, copy, CTAs, scroll cue.
- Scroll: masked word reveals on headlines, intro text lights up word by word, the build section pins and assembles a site step by step, the timeline rail fills, the map coastline draws in.
- No bounce, no overshoot. Everything respects `prefers-reduced-motion`.

## Environment
Generated topographic contours (Lake Huron shoreline feel) with one Tawas City pin, a faint grain layer, and 44.27° N / 83.52° W used sparingly.
