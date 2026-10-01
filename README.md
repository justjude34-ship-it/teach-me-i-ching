# Teach Me the I Ching

**Single-file educational web app** for learning the Book of Changes — Tier 1 Basics + Tier 2 Advanced.

For: Judith Crighton · Sale-ready static HTML (Gumroad / any static host).

## How to open

1. **Double-click** `Teach-Me-the-I-Ching.html` (works via `file://` in any modern browser), or
2. Drop the file on **Vercel / Netlify / any static host**, or
3. Zip and sell/download via Gumroad.

No build step. No npm. No framework.

## Design (locked)

| Token | Hex |
|-------|-----|
| Background | `#000000` (pure black only) |
| Accent primary | `#E040FB` |
| Accent hover/light | `#FF79F2` |
| Accent deep | `#AA00FF` |
| Accent press | `#C51162` |
| Text | Ivory `#f5f0e8` |

## Tiers

- **Tier 1 Basics:** What is the I Ching; yin/yang; eight trigrams; how hexagrams form; coin casting; reading one hexagram simply.
- **Tier 2 Advanced:** Changing lines; yarrow stalks; King Wen / Zhouyi history; Daoist vs Confucian layers; cross-references.

Progress and Tier 2 unlock are stored in `localStorage` on the device.

## Features in this scaffold

- Home with Tier 1 / Tier 2 cards and progress
- Learn player with real Tier 1 lesson content (6 modules)
- Working three-coin cast → King Wen lookup (all 64 names)
- Library: eight trigrams + 64 hexagram browser
- About + reflection disclaimer
- Original plain-language teaching only (no wholesale Wilhelm/Baynes text)

## Disclaimer

For personal reflection and education only. Not medical, legal, financial, or crisis advice. Not a substitute for professional help.

## Files

- `Teach-Me-the-I-Ching.html` — the app
- `PLAN.md` — locked product plan
- `README.md` — this file
