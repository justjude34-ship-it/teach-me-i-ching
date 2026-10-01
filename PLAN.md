# Teach Me the I Ching — App Plan (LOCKED)

**For:** Judith Crighton  
**Working title:** Teach Me the I Ching (spoken: “Te-I Ching”)  
**Goal:** Calm, beginner-friendly **educational** web app — two clear tiers so beginners start simple and graduate into depth. Reflection tool, not fortune-telling. Original plain-language teaching only.  
**Status:** Spec locked. Primary deliverable = **single-file HTML**.

---

## 0. Locked decisions

1. **Delivery: single-file HTML web app** — ONE self-contained `.html` file. No build step, no framework, no npm. All CSS, JS, and content INLINE. Opens via `file://` or any static host (Vercel static / Gumroad zip).
2. **Two tiers clearly linked:**
   - **Tier 1 Basics** — what the I Ching is; yin/yang; eight trigrams; how hexagrams form; coin casting; reading one hexagram simply.
   - **Tier 2 Advanced** — line texts & changing-line dynamics; yarrow stalk in detail; historical context (King Wen, Zhouyi, Confucian commentaries); Daoist vs Confucian layers; hexagram cross-references.
3. **Graduation:** After Tier 1 complete → clear “Enter Advanced” path (localStorage unlock).
4. **Original teaching only** — no wholesale Wilhelm/Baynes copyrighted text. Short original paraphrases + public-domain structure.
5. **Sale-ready** — polished dark UI suitable for Gumroad.

---

## 1. Stack (no Next.js)

| Piece | Choice | Why |
|-------|--------|-----|
| App | **Single `.html` file** | Double-click / static host; zero toolchain |
| State | **localStorage** | Progress + unlock Tier 2 — no auth |
| Deploy | Static host or Gumroad file download | Vercel can serve the one file if desired |

**Out of scope for v1:** accounts, cloud sync, payments, AI chat, Next.js, npm, full yarrow stalk simulator (Tier 2 explains it in text first).

---

## 2. Design system (LOCKED)

| Token | Hex | Use |
|-------|-----|-----|
| Background | `#000000` | Pure black only — never charcoal gray |
| Surface / card | `rgba(255,255,255,0.04)` + light border | Cards on pure black |
| Text | `#f5f0e8` (ivory) | Body copy |
| Muted | `#a8a29a` | Secondary labels |
| Accent primary | `#E040FB` | Buttons, links, highlights, interactive |
| Accent hover/light | `#FF79F2` | Hover, focus, progress fill |
| Accent deep | `#AA00FF` | Pressed / deep emphasis |
| OK / done | `#5ecf8e` | Completed lessons |
| Serif titles | Georgia / system serif | Headings, hexagram names |
| Sans body | system-ui / Segoe UI | Lesson body |

Light line illustrations (trigram SVG strokes) in ivory/fuchsia on black. Bottom nav or top tabs; progress dots; professional spacing/shadows.

---

## 3. Two-tier curriculum

### Tier 1 — Basics

| Module | Focus |
|--------|--------|
| **T1-M1** What is the I Ching? | Book of Changes; mirror not fortune-telling |
| **T1-M2** Yin & yang | Solid / broken lines; stack bottom → top |
| **T1-M3** Eight trigrams | Heaven, Earth, Thunder, Wind, Water, Fire, Mountain, Lake |
| **T1-M4** How hexagrams form | Lower + upper = 64; King Wen order intro |
| **T1-M5** Coin casting | Quiet question; three-coin 6/7/8/9; six lines |
| **T1-M6** Read one hexagram simply | Name + Judgment + Image; changing lines lightly |

**Graduation UX:** Tier 1 complete → “Enter Advanced” unlocks Tier 2.

### Tier 2 — Advanced (soft-locked until graduation)

| Module | Focus |
|--------|--------|
| **T2-M1** Line texts & changing lines | Old yin / old yang; primary vs relating |
| **T2-M2** Yarrow stalk in detail | 50 stalks; probabilities vs coins |
| **T2-M3** Historical context | King Wen; Zhouyi; Confucian commentaries |
| **T2-M4** Philosophical layers | Daoist vs Confucian readings |
| **T2-M5** Hexagram cross-references | Inverse / nuclear / pairs |

---

## 4. Information architecture

| Screen | Purpose |
|--------|---------|
| **Home** | Tier 1 / Tier 2 cards; resume; Cast now |
| **Learn** | Lesson player; module list; progress |
| **Cast** | Question → coin simulator → King Wen result |
| **Library** | Eight trigrams + browse 64 hexagrams |
| **About** | Purpose, credits, **disclaimer** |

---

## 5. Cast engine

- Three fair coins → heads = 3, tails = 2 → sum 6/7/8/9 per line.
- Six lines bottom → top.
- 6 = old yin (changing); 7 = young yang; 8 = young yin; 9 = old yang (changing).
- Binary yang=1 / yin=0 → King Wen lookup table (full 64 names with pinyin/English).
- Judgment/Image: short **original** 1–2 sentence placeholders (detailed for first 8; stubs for rest).

---

## 6. Files

| Path | Role |
|------|------|
| `Teach-Me-the-I-Ching.html` | The entire app |
| `README.md` | How to open, tiers, disclaimer |
| `PLAN.md` | This plan |

Local mirrors: `/workspace/artifacts/teach-me-i-ching/` and `/workspace/artifacts/Teach-Me-the-I-Ching.html`.

---

## 7. Disclaimer (required on About + Cast)

For personal reflection and education only. Not medical, legal, financial, or crisis advice. Not a substitute for professional help.

---

## 8. Next after scaffold

1. Expand Judgment/Image originals for all 64.
2. Full Tier 2 lesson pages (beyond stubs).
3. Optional journal under Cast result.
4. Gumroad packaging + cover art.
5. Legal pass before public sale.

---

*Plan locked for Judith Crighton — single-file HTML, pure black `#000000` + fuchsia `#E040FB`, Tier 1 + Tier 2.*
