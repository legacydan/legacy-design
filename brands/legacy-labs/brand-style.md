---
brand: Legacy Labs
slug: legacy-labs
website: https://legacylabsai.com
extracted_via: Firecrawl + manual editorial pass
default: true
---

# Legacy Labs — Brand Style

## 1. Visual Theme & Atmosphere

Legacy Labs is operator-grade fintech-meets-AI editorial. Deep navy and near-black backgrounds anchor the system, with one electric cyan accent doing all the emphasis work. The atmosphere reads as: a private office at midnight, a Bloomberg terminal, a Christopher Nolan title card. Premium without being precious. Technical without being cold. The brand carries cinematic confidence ("ACT I · The problem", "VOL. 01 · 2026") while staying tight and operator-direct in voice.

Every surface is built on a strict navy scale (50 → 950) with cyan as the only accent. Type is Inter Tight for display, Inter for body, JetBrains Mono for technical labels and eyebrows. The mood is "we install the system and stay on the line until it runs without us" — confident, hands-on, no fluff. Backgrounds favour gradients across `#060f3d → #0b1f66 → #152e8a` for hero moments, with white paper (`#fff`) and mist (`#f4f6fb`) for content slides. Hairlines are deliberate at `#0a102414` — visible but never loud.

**Key Characteristics:**
- Deep navy 900/950 backgrounds for hero and dark sections
- Cyan `#5eeaff` as the single accent. No second accent ever.
- Inter Tight at display sizes, weight 600–700, tight letter-spacing (-0.02em)
- JetBrains Mono in `text-[11px]` uppercase tracking-[0.12em] for eyebrow labels
- Editorial framing: "ACT I", "Panel 02 →", "STEP 01 · AUDIT", "VOL. 01 · 2026"
- 1px hairline borders, never heavy strokes
- Subtle navy-tinted gradients on hero panels, never decorative gradients on content

---

## 2. Color Palette & Roles

### Brand scale (navy)
| Token | Hex | Notes |
|---|---|---|
| `--brand-50` | `#eaf0ff` | tinted surface, badge backgrounds |
| `--brand-100` | `#d3deff` | subtle highlight |
| `--brand-200` | `#a7beff` | soft fill |
| `--brand-300` | `#7a9dff` | secondary text on dark |
| `--brand-400` | `#4f7bff` | bright link / interactive |
| `--brand-500` | `#2e58e0` | hover state |
| `--brand-600` | `#1e3fb5` | primary CTA fill |
| `--brand-700` | `#152e8a` | dark CTA, header gradient mid |
| `--brand-800` | `#0b1f66` | **primary brand color** |
| `--brand-900` | `#060f3d` | hero background |
| `--brand-950` | `#02061e` | midnight, deepest section |

### Accent (cyan, the only one)
| Token | Hex | Notes |
|---|---|---|
| `--accent-cyan` | `#5eeaff` | the accent. Use for emphasis, single accent per slide. |
| `--accent-cyan-soft` | `#b6f4ff` | glow halo, subtle backgrounds |
| `--accent-cyan-deep` | `#1fb8d9` | dark-mode safe variant |

### Ink (text on light surfaces)
| Token | Hex | Notes |
|---|---|---|
| `--ink-900` | `#0a1024` | primary headings on white |
| `--ink-700` | `#1f2640` | strong body text |
| `--ink-500` | `#4a516b` | body |
| `--ink-400` | `#6b7391` | muted body, captions |
| `--ink-300` | `#98a0b8` | placeholder, disabled |
| `--ink-200` | `#c4cad9` | dividers on light |

### Surfaces
| Token | Hex | Notes |
|---|---|---|
| `--paper` | `#ffffff` | content slide background |
| `--mist` | `#f4f6fb` | section/card backgrounds |
| `--mist-deep` | `#e8ecf5` | borders between mist sections |
| `--hairline` | `#0a102414` | 1px borders, light surface |
| `--hairline-strong` | `#0a102424` | 1px borders, more contrast |

**Color scheme:** dual — dark hero/cover slides, light content slides. Never mid-tones.
**Accent rule:** one accent (`#5eeaff`) per slide. Multiple accents = no accent.
**60-30-10:** dark slides → 60% navy 950, 30% navy 800, 10% cyan. Light slides → 60% paper, 30% ink-700 type, 10% cyan.

---

## 3. Typography Rules

### Font Family
- **Display**: `Inter Tight`, with fallback `system-ui, sans-serif`. Weights 600 / 700. Letter-spacing -0.02em at display sizes. Used for hero headlines, slide titles, big numbers.
- **Body**: `Inter`, with fallback `-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif`. Weights 400 / 500 / 600. Used for all running copy, labels, callouts.
- **Mono Display**: `JetBrains Mono`, with fallback `ui-monospace, SFMono-Regular, monospace`. Weight 500–600. Used for eyebrows, section markers, panel numbers, technical chrome.

### Sizing (Inter Tight modular scale, ratio ≈ 1.333)
| Role | Size | Weight | Line-height | Letter-spacing |
|---|---|---|---|---|
| Hero headline | 72–96px | 700 | 1.05 | -0.02em |
| Slide title (H1) | 56px | 700 | 1.1 | -0.02em |
| Section header (H2) | 40px | 600 | 1.15 | -0.015em |
| Sub-heading (H3) | 28px | 600 | 1.25 | -0.01em |
| Body | 24px | 400 | 1.55 | 0 |
| Caption | 18px | 500 | 1.5 | 0 |
| Eyebrow / mono label | 11–14px | 500 | 1.0 | 0.12em uppercase |

### OpenType
- Inter `cv11` for single-storey `a` if available.
- Tabular numerals (`tnum`) on all numbers in tables, KPIs, and financial figures.

---

## 4. Spacing & Shape

- **Base grid:** 8px. All spacing values ∈ {8, 16, 24, 32, 48, 64, 96, 128}. Section padding typically 96px on hero, 64px on content.
- **Border radius:** 8px on cards, 12px on larger surfaces, `rounded-full` (pill) on tags and small badges. No 2px or 4px. No sharp corners on interactive elements.
- **Borders:** 1px hairline at `var(--hairline)` (`#0a102414`). Never 2px+. Borders carry hierarchy, not decoration.
- **Shadows:** sparingly. When used: `0 1px 2px rgba(10,16,36,0.06), 0 8px 24px rgba(10,16,36,0.08)`. Never on bars or charts.
- **Framework hint:** Tailwind. The live site uses tailwind tokens (`text-brand-800`, `text-cyan`, `text-ink-500`, `font-display`, `font-mono-disp`).

---

## 5. Voice & Personality

- **Tone:** operator. Direct. Confident. Anti-deck.
- **Energy:** medium-high. Editorial without being theatrical.
- **Audience:** SMB owners, healthcare ops leaders, SaaS exec teams, clinical research operators. People with P&L responsibility.
- **Anti-patterns:** corporate-speak, "I'd be happy to," "certainly," "absolutely," "great question," six-bullet slides, em dashes (use periods, hyphens, or commas instead).
- **Patterns we lean into:**
  - Outcome-focused, not feature-focused. ("Cut intake from 12 minutes to 90 seconds" beats "AI-powered intake automation.")
  - Cinematic structure: ACT I / ACT II / ACT III, Panel 01 →, STEP 01 · AUDIT, VOL. 01 · 2026.
  - Short sentences. The reader scans.
  - "We" not "I". Operators in the room.

## Voice samples (real copy from the brand)
- "Your business, empowered."
- "We don't replace what you do. We just make you better at doing it."
- "Secure AI, fit to your flow, wired in by operators who've lived it."
- "We don't pitch tools. We install the system and stay on the line until it runs without us."
- "Five disciplines. One job: give your business leverage."
- "Five steps. No magic. Just the work."
- "We stay on weekly calls until you cut us."
- "We read your business. Hands-on, fast."
- "We choose the fights, then start winning them."

---

## 6. Logo

- **Wordmark:** `Legacy Labs` set in Inter Tight 700, letter-spacing -0.02em. White on dark, ink-900 on light.
- **Lockup:** the wordmark is the primary identity. No icon mark required.
- **Placement on slides (default):** bottom-left, 24px tall, inside the 5% safe zone. Inverted color depending on background.
- **Hero slides:** wordmark may be larger (32px) with a thin cyan rule above or beside.
- **Don't:** add gradients to the wordmark. Don't outline it. Don't rotate it. Don't tile it.

---

## 7. Components — slide patterns

### Cover / hero slide
- Background: linear-gradient(135deg, `#02061e` 0%, `#060f3d` 50%, `#0b1f66` 100%)
- Top-left eyebrow: mono, uppercase, `#5eeaff`, 12px, tracking 0.12em (e.g. `VOL. 01 · 2026`)
- Headline: Inter Tight 700, 88px, white, letter-spacing -0.02em, line-height 1.05
- Sub: Inter 400, 24px, `#a7beff`, line-height 1.55
- Bottom-left: Legacy Labs wordmark, 24px, white, with optional cyan rule above
- Bottom-right (optional): page indicator in mono, 12px, `#7a9dff`

### Content slide (light)
- Background: `#ffffff`
- Top-left eyebrow: mono, uppercase, `#1e3fb5`, 12px, tracking 0.12em
- Title: Inter Tight 700, 56px, `#0a1024`
- Body: Inter 400, 24px, `#1f2640`, max-width 60ch
- Single accent (cyan) on one element only: a number, an underline, an icon, a chip
- Bottom-left: Legacy Labs wordmark, 24px, `#0a1024`

### Stat / KPI slide
- Big number: Inter Tight 700, 144–192px, `#0b1f66` on light or white on dark
- Label below: mono, uppercase, 14px, tracking 0.12em, `#4a516b`
- Single supporting line: Inter 400, 24px
- The cyan accent: a 4px underline on the number, OR a small cyan dot before the label

### Quote slide
- Background: `#02061e`
- Massive italic quote: Inter Tight italic 600, 56px, white, max-width 18 words
- Attribution: mono uppercase, 14px, `#5eeaff`, tracking 0.12em
- Wordmark bottom-left

### Five-step / process slide
- Mono numbered eyebrows ("STEP 01 · AUDIT") in cyan
- 5 columns or stacked rows, each with: number, name, one-sentence outcome
- One cyan dot per row maximum
- No icons unless they're flat 1-color line icons in `#0b1f66`

---

## 8. Quick Reference (for Claude)

```css
:root {
  /* brand scale */
  --brand-50:  #eaf0ff;
  --brand-100: #d3deff;
  --brand-200: #a7beff;
  --brand-300: #7a9dff;
  --brand-400: #4f7bff;
  --brand-500: #2e58e0;
  --brand-600: #1e3fb5;
  --brand-700: #152e8a;
  --brand-800: #0b1f66;
  --brand-900: #060f3d;
  --brand-950: #02061e;

  /* accent — the only one */
  --accent-cyan:      #5eeaff;
  --accent-cyan-soft: #b6f4ff;
  --accent-cyan-deep: #1fb8d9;

  /* ink */
  --ink-900: #0a1024;
  --ink-700: #1f2640;
  --ink-500: #4a516b;
  --ink-400: #6b7391;
  --ink-300: #98a0b8;
  --ink-200: #c4cad9;

  /* surfaces */
  --paper: #ffffff;
  --mist: #f4f6fb;
  --mist-deep: #e8ecf5;
  --hairline: #0a102414;
  --hairline-strong: #0a102424;

  /* type */
  --font-display: "Inter Tight", system-ui, sans-serif;
  --font-body: "Inter", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  --font-mono: "JetBrains Mono", ui-monospace, SFMono-Regular, monospace;

  /* shape */
  --radius-sm: 8px;
  --radius-md: 12px;
  --radius-pill: 9999px;
}

/* Hero gradient */
.hero {
  background: linear-gradient(135deg, var(--brand-950) 0%, var(--brand-900) 50%, var(--brand-800) 100%);
  color: #fff;
}

/* Eyebrow (mono uppercase) */
.eyebrow {
  font-family: var(--font-mono);
  font-size: 12px;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--accent-cyan);
}

/* Display headline */
.headline {
  font-family: var(--font-display);
  font-weight: 700;
  font-size: 88px;
  line-height: 1.05;
  letter-spacing: -0.02em;
}
```

---

## 9. Don'ts (Legacy-specific)

- Don't use a second accent. Cyan only.
- Don't use em dashes in body copy. Period, hyphen, or comma.
- Don't centre-align body content. F-pattern, top-left.
- Don't use gradients on cards or charts. Only on hero backgrounds.
- Don't use stock-photo people. If a visual is needed, use abstract navy/cyan compositions or actual product UI screenshots.
- Don't write paragraphs on slides. Slides are headlines and supporting fragments.
- Don't pile multiple cyan elements on one slide. One accent per slide.

---

## Reference

**Website:** [https://legacylabsai.com](https://legacylabsai.com)
**Sister entities:** Legacy Care Financial · Legacy Care Foundation (501c3) · Derma-X
**Tagline:** "Your business, empowered."
**Brand line:** "We don't replace what you do. We just make you better at doing it."
