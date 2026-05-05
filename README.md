<div align="center">

# Legacy Design

### A Claude skill for slides that don't look like AI made them.

**Brand DNA × 20 codified design principles → beautiful HTML decks, on demand.**

Built for Legacy Labs operators. Ships with the Legacy Labs brand pre-loaded plus 70+ other brand systems for client work.

</div>

---

## What it does

Legacy Design is a Claude Code skill that combines two things every other AI deck generator misses:

1. **Brand DNA** — the Legacy Labs system by default, extracted live from any URL via Firecrawl, or picked from **70+ pre-built brand systems** (Stripe, Apple, Linear, Spotify, Vercel, Notion, Tesla, Airbnb…)
2. **20 codified design principles** — pulled from Tufte, Reynolds, Duarte, Williams, Refactoring UI, Müller-Brockmann, Mayer, WCAG 2.2

Every deck ships on-brand and objectively well-designed. No purple gradients. No six-bullet hero slides. No drop shadows on bars. No em dashes when it's a Legacy deck.

---

## Why we built it

Legacy Labs runs on operator output. We don't write 40-page decks. But every audit, every plan, every weekly client review still needs slides that match how we sound: direct, premium, navy + cyan, no fluff. This skill turns "we need a deck for that" into a one-shot command.

It's also the asset engine for client work. Drop a client's URL in and Legacy Design picks up their brand and builds inside it. Same skill, two modes: ours and theirs.

---

## The 20 rules

Every slide passes the same 20 checks.

| # | Rule | Source |
|---:|---|---|
|  1 | One idea per slide | Reynolds; Duarte |
|  2 | Glanceable in ≤3 seconds | Duarte; NN/g |
|  3 | ≤7±2 visual chunks; ideal 3–5 | Miller 1956; Cowan 2001 |
|  4 | ≥40% whitespace ratio | Refactoring UI; Reynolds |
|  5 | 5% edge safe-zone, all sides | Broadcast title-safe |
|  6 | Type on a modular scale (1.25–1.618) | Tschichold; Bringhurst |
|  7 | Maximum 4 type sizes per slide | Refactoring UI |
|  8 | Body ≥24px, title ≥48px | Reynolds; Duarte |
|  9 | Line-height 1.4–1.6 body, 1.05–1.2 display | Butterick; Bringhurst |
| 10 | Line length ≤60 characters | Bringhurst |
| 11 | WCAG contrast ≥4.5:1 body, aim 7:1 (AAA) | WCAG 2.2 |
| 12 | 60-30-10 color split | Itten; Refactoring UI |
| 13 | One accent per slide | Tufte |
| 14 | Never encode meaning by hue alone | WCAG 1.4.1 |
| 15 | 8pt grid for all spacing | Bryn Jackson; Material |
| 16 | Align everything to one grid | Müller-Brockmann |
| 17 | Proximity: related ≤16px, unrelated ≥48px | Gestalt; Williams |
| 18 | Data-ink ratio ≥80% | Tufte 1983 |
| 19 | F-pattern: headline + key visual top-left | NN/g eye-tracking |
| 20 | Two valid modes — pick one and stay | Tufte vs Reynolds |
| 21 | Brand logo on every slide (default ON) | Legacy house rule |

---

## Install

```bash
git clone https://github.com/legacy-labs/legacy-design ~/.claude/skills/legacy-design
```

Then in Claude Code or Cowork:

```
> use legacy-design — make me an investor deck on the Q3 audit numbers
> use legacy-design — build a sales one-pager for omnicure.com about our intake automation
> use legacy-design — generate a board update on the Derma-X retail launch
```

The skill will:
1. Confirm the brand (Legacy Labs by default, or pick a client)
2. Ask for content brief: headline + 3–5 points
3. Generate `slides.html` applying brand DNA × 20 rules
4. Open in browser. Iterate via natural conversation.

---

## The Legacy Labs brand system

The default brand entry lives at [`brands/legacy-labs/brand-style.md`](brands/legacy-labs/brand-style.md). Highlights:

- **Palette.** Deep navy (`#060f3d`) and midnight (`#02061e`) backgrounds. Brand 800 (`#0b1f66`) primary. Cyan (`#5eeaff`) as the only accent. White paper, mist surfaces.
- **Type.** Inter Tight for display, Inter for body, JetBrains Mono for technical labels and small caps.
- **Voice.** Operator. Outcome-focused. No em dashes. Editorial framing welcome (Act I / Act II, Vol. 01, etc.).
- **Logo.** Wordmark, bottom-left, 24px tall, on every slide.

---

## Brand library — 70+ pre-built systems

Use them when the deck is *for* a client.

| Tech / AI | Finance | Auto / Lifestyle | Media | Productivity |
|---|---|---|---|---|
| Anthropic / Claude · OpenAI · DeepSeek · Linear · Vercel · Stripe · Cursor · GitHub · Figma · Webflow · Framer · Mintlify · Notion · Raycast · Lovable · Resend · Sentry · Supabase · Superhuman · MongoDB · Sanity · Posthog · Replicate · Runway · Hashicorp · ElevenLabs · Cal · Clay · Composio · ClickHouse · Cohere · Mistral · Together · x.ai · Ollama · OpenCode · Expo · Pinterest · Glaido | Stripe · Mastercard · Coinbase · Binance · Kraken · Revolut · Wise · Shopify | Tesla · BMW · BMW M · Bugatti · Ferrari · Lamborghini · Renault · Nike · Airbnb · Apple · Starbucks · Grind · Vodafone | The Verge · Wired · Spotify · YouTube · Sony · PlayStation · IBM | Notion · Slack · Miro · Intercom · Zapier · Uber · NVIDIA · SpaceX · VoltAgent · Warp |

Each entry is a single `brand-style.md` file: colors, type, voice, components, source URL. Add your own using `brands/_template.md`.

---

## How the skill works (under the hood)

```
   ┌─────────────────────────────────────────┐
   │  1. Brand DNA       legacy-labs (default)│
   │                     OR URL → Firecrawl   │
   │                     OR brands/<name>.md  │
   ├─────────────────────────────────────────┤
   │  2. Design rules    principles/...md     │
   ├─────────────────────────────────────────┤
   │  3. Compose         brand × rules → HTML │
   └─────────────────────────────────────────┘
                      ↓
                  slides.html
```

The skill's runbook lives in `SKILL.md`. The 20 design principles (with research citations and numeric thresholds) live in `principles/design-principles.md`.

---

## Credits

- **Forked from** [Power Design](https://github.com/ItsssssJack/power-design) by Jack Roberts, MIT-licensed.
- **Brand library** — sourced from [VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md), restructured upstream.
- **Design research** — Edward Tufte, Garr Reynolds, Nancy Duarte, Robin Williams (CRAP), Adam Wathan & Steve Schoger (Refactoring UI), Josef Müller-Brockmann, Matthew Butterick, Robert Bringhurst, Richard Mayer, Nielsen Norman Group, WCAG 2.2.
- **Legacy Labs brand entry** — extracted from [legacylabsai.com](https://legacylabsai.com).

---

## License

MIT — see [LICENSE](LICENSE).

---

<div align="center">

**A Legacy Labs production · Vol. 01 · 2026**

[legacylabsai.com](https://legacylabsai.com)

</div>
