# FOF Youth Sports — Design System

A design system for **FOF Youth Sports**, a Charlotte, NC youth sports league for ages 5–12. The brand promise is **Focus On Fundamentals** — what the FOF in the name actually stands for. Convenient, family-friendly, professionally-run rec sports where every kid learns the basics the right way, every parent gets clear info, and every Saturday feels like the best part of the week.

The system is built to feel **playful for kids and polished for parents** — the same tonal balance i9 Sports occupies, but with FOF's local Charlotte voice and a navy + gold palette.

> ⚠ **Note from the design agent:** No existing brand assets, codebase, or Figma file were attached. This system was generated from a verbal brief. **All colors, type pairings, the logo mark, and the photo placeholders are first-pass proposals.** See [Caveats & Asks](#caveats--asks) at the bottom — there's a clear list of things that need real assets or a human call.

---

## Brand at a glance

| | |
|---|---|
| **Name** | FOF Youth Sports |
| **Tagline** | Focus On Fundamentals |
| **Location** | Charlotte, NC |
| **Audience** | Kids ages 5–12 (players); parents 28–45 (decision-makers); coaches (mostly volunteer parents) |
| **Sports** | Soccer · Flag football · Basketball · Baseball / T-ball · Volleyball · Cheer |
| **Personality** | Balanced — playful kid energy, polished parent trust |
| **Inspiration** | i9 Sports model: convenience, family-friendly, no-tryout rec |
| **Type** | Nunito (display, friendly humanist) + DM Sans (body, polished) |
| **Primary palette** | Stadium navy `#0B2A5B` + Jersey gold `#FFC72C` |
| **Imagery** | Real, warm, sunlit candid photos of kids playing |

---

## Sources

This system was built from a verbal brief — no codebase, Figma file, or asset library was attached. If you have any of the following, please attach them and I'll re-read against them:

- An existing logo, wordmark, or sketch
- A registration platform reference (LeagueApps, TeamSnap, SportsEngine etc.)
- Charlotte-specific photos of kids/teams/parks
- A list of competitor links you like or hate

---

## Index — what's in this folder

```
README.md                  ← you are here
SKILL.md                   ← Claude Code skill bridge
colors_and_type.css        ← all CSS variables (colors, type, spacing, radii, shadows, motion)

assets/                    ← logos, sport marks, hero illustrations, photo placeholders
  logo-mark.svg            primary monogram (navy + gold)
  logo-horizontal.svg      lockup with wordmark + tagline
  logo-mark-cream.svg      cream-mode variant
  pattern-pennants.svg     repeating pennant motif
  pattern-confetti.svg     repeating confetti motif (kid-energy moments)
  photo-placeholder.html   stylized "kids playing" photo placeholder template

preview/                   ← cards rendered in the Design System tab
  type-*.html              type specimens
  color-*.html             palette swatches
  spacing.html, radius.html, shadow.html, motion.html
  buttons.html, inputs.html, cards.html, badges.html, ...

ui_kits/
  marketing/               public site (homepage, sport pages, about, signup)
  registration/            register-a-player flow (5-step)
  parent_dashboard/        schedule, team, payments
  coach_dashboard/         roster, attendance, communication
  mobile_app/              game-day companion (iOS frame)

fonts/                     Google Fonts loaded via CSS @import (no local files)
```

---

## Content fundamentals

### Voice
**Warm, direct, parent-respectful.** We talk to busy parents the way a great rec coach talks to them at pickup: confident, no jargon, no hard sell, with just enough fun to remind everyone this is supposed to be a *good time*.

We are NOT:
- Corporate / try-hard ("Maximize your child's athletic potential!" — no.)
- Preachy / character-development heavy ("Building tomorrow's leaders today" — no.)
- Cutesy / over-emoji'd ("⚽️🥳 Sign up your lil champ! 🏆" — no.)
- Hype-bro ("LET'S GOOOO" — no.)

### Tone & casing
- **Sentence case** for everything: headlines, buttons, nav. (No All-Caps Headlines, no "Click Here Now".)
- Eyebrow / label text uses small UPPERCASE with letter-spacing — and only there.
- Numbers and stats are written out for emotion ("**Six sports.** One Saturday."), but use digits for facts ("Ages 5–12, 5 weeks").
- Use a Charlotte lens when natural ("From Ballantyne to NoDa") but never force it.

### Person
- **"You" + "your kid"** — not "your child" (sounds clinical), not "your athlete" (sounds intense).
- **"We"** for the league. ("We'll match you with a team near you.")
- **"Coach"** is a respected role, never "volunteer" in user-facing copy.

### Specific patterns
- **Hero promise:** short verb-led sentence. *Sign up. Show up. Play.*
- **CTAs:** verbs. "Find a league", "Register your kid", "See the schedule." Never "Learn more" or "Click here".
- **Empty states:** warm and specific. *"No games this weekend — coach probably owes you a Saturday back."*
- **Errors:** human, no blame. *"Hmm, that email didn't go through. Try again?"*
- **Microcopy on form labels:** "Your kid's name (the one on the jersey)" beats "Player name".

### Emoji & symbols
- **No emoji in product UI**, headings, or marketing copy.
- Sport pictograms are SVG icons (consistent stroke), never emoji.
- Score/stat displays may use bullet `·` or em dash `—` as separators.
- Stars / trophy moments use vector SVGs from `assets/`, not Unicode `⭐`.

### Real copy snippets

> **Hero:** Six sports. One Saturday. Sign your kid up for a season they'll actually look forward to.
>
> **Sub:** Charlotte's friendliest rec league — every kid plays, every game has a coach, and parents always know what time to be there.

> **Sport page lead (Soccer):** Soccer Saturdays. Five weeks of small-sided games on real grass, with coaches who care more about Cooper getting his first goal than the score on the board.

> **Empty schedule state:** Nothing on the calendar yet. Sign up for a season and your Saturdays start filling in.

> **Payment confirmation:** You're in. We'll email you the team match within a week — coach will reach out before the first game.

---

## Visual foundations

### Color
- **Primary navy `#0B2A5B`** carries headers, headlines, and trust moments. Used at large scale, not as accent confetti.
- **Jersey gold `#FFC72C`** is the energy. CTAs, score highlights, the inside of the logo. Always paired with navy text on top — never gold on white text.
- **Rally red, field green, clay orange, cheer pink** are *sport tags only* (one per sport, used on pills and headers of sport-specific pages). Not general-purpose accents.
- **Cream `#FFF8E7`** is a warm canvas alternative to white — used for sections that need to feel handed-down rather than corporate (about page, testimonials).
- Backgrounds default to **white**; `cream` and `navy-50` are the two acceptable section breaks.
- **Avoid gradients** except for two specific moments: (1) photo placeholder backgrounds, which use a sun-warmed gold→cream gradient on purpose; (2) navy hero overlays for legibility on photos.

### Typography
- **Nunito** for display and headlines. Weights 800–900 only — Nunito at lighter weights looks generic.
- **DM Sans** for body, UI labels, microcopy. Weights 400 / 500 / 700.
- **IBM Plex Mono** appears once, on jersey numbers / scoreboards / countdown timers — never in body copy.
- **Letter-spacing:** displays sit tight (`-0.03em`). Body sits at default. Small UPPERCASE eyebrows open up to `+0.08em`.
- **Line height:** display 1.02, headings 1.12, body 1.55. Body is generous on purpose; parents read this on their phones at the park.

### Spacing & layout
- **4px base grid.** Never freehand spacing — pick from `--sp-1` through `--sp-24`.
- Content max-width `1180px`. Narrow text columns max-width `720px`.
- Generous gutters (24–32px on desktop, 16px mobile).
- Sections breathe: `--sp-20` (80px) vertical between major sections on desktop.

### Cards & surfaces
- **Default card:** white, `--r-md` (14px) corners, `--shadow-sm`, 1px `--color-border` outline. No left-color-stripe accents (banned trope).
- **Feature card:** white, `--r-lg` (20px), `--shadow-md`, with a small navy or gold "tag pill" floated over the top edge instead of a full color band.
- **Sport cards** use a sport-specific accent color in *the tag and a small icon medallion only* — the card itself stays neutral.
- Borders are 1px, soft (`--color-border` `#E5E9F0`). Strong borders are reserved for inputs.

### Buttons
- **Primary CTA:** gold fill, navy text, **bottom-stack shadow** (`--shadow-gold`) so it looks like a 3D pennant button. On press, the button "drops" into the shadow (translate Y +4px, shadow shrinks). Playful but not gummy.
- **Secondary:** navy fill, white text, normal shadow.
- **Tertiary / ghost:** transparent, navy text, 1.5px navy border, fills to navy-50 on hover.
- All buttons: pill radius (`--r-pill`), bold weight, sentence case, generous padding (12px × 24px minimum).

### Hover & press states
- Hover on links: deepen color (navy-500 → navy-700) + 3px underline offset.
- Hover on buttons: slightly darker fill, no scale change.
- Press on primary CTA: translate Y +4px (drops into shadow); shadow stack shrinks.
- Hover on cards: lift via `--shadow-md`, no rotation, no tilt.
- Focus rings: gold at 55% alpha, 3px wide, on all interactives.

### Borders, radii, shadows
- **Radii:** xs 6, sm 10, md 14, lg 20, xl 28, pill 999. Cards default to md. Modals lg. Pills/chips/buttons pill.
- **Shadows** are blue-tinted (rgba 11/42/91) to feel cohesive with the navy palette — never neutral grey.
- **Inset shadows** are not used. Surfaces stack via outline or shadow, not depth-into-page.

### Motion
- **Default ease:** `--ease-out` (cubic-bezier(0.22,0.61,0.36,1)) — confident, not bouncy.
- **Playful spring** (`--ease-back`) is used on TWO moments: signup-success confetti and the "Game On" badge animation on a live-game card. Never on UI chrome.
- Durations: `120ms` for hover, `200ms` for state changes, `360ms` for entrances.
- Page transitions are simple fade + 8px translate — never slides between routes.

### Imagery
- **Real photos of kids playing**, sunlit and candid — not posed, not stock-bro, not heavily filtered.
- Warm color treatment: subtle yellow/cream warming, slight contrast lift. No b&w, no heavy grain.
- Faces are visible but not the only subject — wide angles with field, ball, parents in the periphery work better than close-ups for the kid-and-family energy.
- No illustrations of people. Hand-drawn touches are limited to *non-figurative* doodles: pennants, a stitched ball outline, confetti dots — used as repeating pattern accents, never headlining.
- Photo aspect ratios: 4:3 for cards, 16:9 for heroes, 1:1 for circular avatars. Always with `object-fit: cover`.

### Transparency & blur
- Used **once**: navigation glass effect on top of the homepage hero (backdrop-blur 12px, white 80%). Nowhere else.
- Modal scrims are solid navy at 60% opacity. No frosted glass overlays.

### Fixed elements
- Sticky nav on marketing pages.
- Bottom tab bar on mobile app (5 tabs max).
- Persistent score widget on parent dashboard during a live game (gold pill, navy text, top-right of viewport).

---

## Iconography

- **General UI icons:** [Lucide](https://lucide.dev) loaded from CDN — clean stroke (1.75px), rounded line caps, a perfect match for the rounded humanist type. Always 20px or 24px in product UI, stroked navy, never filled.
- **Sport pictograms:** [Phosphor Icons](https://phosphoricons.com) (regular weight), loaded from CDN, used for ball icons (soccer-ball, basketball, football, baseball, volleyball). **Cheer has no direct match — currently substituted with Phosphor's `confetti`. ⚠ Flag for art direction: a custom pom-pom mark would be better.**
- **Logo / mark:** original SVG (`assets/logo-mark.svg`).
- **Pattern accents:** a pennant repeat and a confetti repeat (`assets/pattern-*.svg`) — used at very low opacity in section backgrounds.
- **No emoji anywhere in product surfaces.** ⭐ 🎉 ⚽ are banned.
- **No icon font** — Lucide's CDN script injects SVGs at runtime, which is what we want.

### Substitutions flagged
| Asked for | Substituted with | Why / fix |
|---|---|---|
| Cheer pictogram | Phosphor `confetti` | No native match — please commission a small pom-pom SVG. |
| Real photos | Stylized warm-gradient placeholders with caption text | No photo library was attached. Swap in real photos before launch. |
| Brand fonts | Google Fonts: Nunito + DM Sans | If you have purchased / licensed fonts, drop them in `fonts/` and update `colors_and_type.css`. |

---

## Caveats & asks

This is a from-scratch system built without any provided assets. The biggest open items, in order of impact:

1. **Real photos.** The single largest visual upgrade is a Charlotte-specific photo library: kids playing, sunlit, candid. Currently the system uses warm-gradient placeholders with descriptive captions.
2. ~~The "FOF" expansion.~~ **Confirmed: Focus On Fundamentals.**
3. **Logo.** The current mark is a clean navy/gold pennant monogram — directionally aligned with what you picked, but a real designer should refine the geometry.
4. **Cheer iconography.** No standard icon set has a great cheer pictogram. Needs a custom mark.
5. **Registration platform.** The registration UI kit is built as a custom flow. If you're planning to integrate LeagueApps / SportsEngine / TeamSnap, the styling will need to bend to their constraints.
6. **Coach role specifics.** The coach dashboard makes assumptions about attendance + parent communication. Validate with a real volunteer coach before extending.

**Please react to anything off-base** and I'll iterate — I'd rather rebuild the right thing than polish the wrong one.
