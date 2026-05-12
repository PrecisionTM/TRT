# DEPLOY — TRT Landing Page
**Precision Telemed · Testosterone Replacement Therapy**

---

## ✅ Conventions Checklist

- [x] No `vh`, `dvh`, or `svh` units used for section/hero heights
- [x] Hero uses `min-height: clamp(560px, 60vw, 860px)` with `height: auto`
- [x] Hero `<img>` uses `object-fit: cover`
- [x] All `position: absolute` layers are inside explicit-height parents
- [x] Brand CSS color tokens applied (`--color-primary`, `--color-fg`, etc.)
- [x] `overflow-x: hidden` on `#page-wrap`
- [x] All image paths are relative (`images/...`) — no absolute `/` paths
- [x] `vercel.json` contains only `{ "cleanUrls": true }`
- [x] No unused/stale files in `images/logos/`
- [x] `download` blank placeholder file present
- [x] No `node_modules/`, no `.gitignore`, no build artifacts

---

## 📁 File Structure

```
vercel-trt/
├─ index.html                          ← Single-file landing page (inline CSS + JS)
├─ vercel.json                         ← { "cleanUrls": true }
├─ DEPLOY.md                           ← This file
├─ download                            ← Empty placeholder (required by repo convention)
└─ images/
   ├─ hero-bg.jpg                      ← Hero background
   ├─ science-visual-trt-v3.jpg        ← Science section image
   ├─ trt-result-1.jpg                 ← Before/after result photo 1
   ├─ trt-result-2.jpg                 ← Before/after result photo 2
   ├─ doctors/
   │  ├─ dr-palumbo.jpg
   │  ├─ angela-kifer-thomas.jpg
   │  ├─ dr-patel.jpg
   │  ├─ dr-colon-molero.jpg
   │  ├─ samuel-palmer.jpg
   │  ├─ dr-akler.jpg
   │  ├─ brett-whaley.jpg
   │  ├─ michael-gype.jpg
   │  ├─ dr-chandler.jpg
   │  ├─ brittany-umana.jpg
   │  └─ dr-ahmed.jpg
   └─ logos/
      ├─ lecom-real.png                ← LECOM seal (Palumbo + Chandler) — black on black bg, filter: invert(1)+sage
      ├─ utmb-real.png                 ← UTMB Galveston seal (Kifer-Thomas) — filter: invert(1)+sage
      ├─ cu-colorado-real.png          ← CU interlocked mark (Dr. Patel) — pre-colored sage, filter:none
      ├─ ponce-real.png                ← Ponce School of Medicine (Colón-Molero) — filter: invert(1)+sage
      ├─ vanderbilt-real.png           ← Vanderbilt V mark (Palmer) — pre-colored sage, filter:none
      ├─ mount-sinai-real.png          ← Mount Sinai wordmark (Dr. Akler) — filter: invert(1)+sage
      ├─ texas-tech-real.png           ← Texas Tech TT mark (Brett Whaley) — filter: invert(1)+sage
      ├─ cleveland-state-real.png      ← Cleveland State seal (Michael Gype) — filter: invert(1)+sage
      ├─ maryville.svg                 ← Maryville University M mark (Brittany Umana) — SVG, filter: brightness(0)+sage
      └─ kentucky-real.png             ← UK interlocked mark (Dr. Ahmed) — black on white, filter: invert(1)+sage
```

---

## 🎨 Logo Filter Notes

All `.doctor-card__inst img` receive the sage tint filter by default:
```css
filter: invert(1) brightness(0) saturate(100%) invert(32%) sepia(22%) saturate(520%) hue-rotate(75deg) brightness(88%) contrast(92%);
```

**Exceptions (inline `style="filter:none;"`):**
- `cu-colorado-real.png` — already pre-colored sage green
- `vanderbilt-real.png` — already pre-colored sage green

**SVG exception (no leading `invert(1)`):**
- `maryville.svg` — has its own CSS rule with `brightness(0)` + sage tint (no invert needed)

---

## 🔗 CTA URLs

| Button | URL |
|---|---|
| Check My Eligibility (primary, all CTAs) | `https://precisiontelemed.com/start-testosterone-program/` |
| Sermorelin cross-sell | `https://precisiontelemed.com/sermorelin/` |

---

## 🚀 Deploy to Vercel via GitHub

```bash
# 1. Create a new repo (e.g. "precision-trt")
git init
git add .
git commit -m "Initial TRT landing page"
git branch -M main
git remote add origin https://github.com/YOUR-ORG/precision-trt.git
git push -u origin main
```

Then in Vercel:
1. Go to https://vercel.com/new
2. Import the `precision-trt` repo
3. Framework Preset → **Other**
4. Root Directory → leave empty (or `vercel-trt/` if deploying subfolder)
5. Build Command → leave empty
6. Output Directory → leave empty
7. Click **Deploy**

---

## ⚠️ Do NOT

- Add a `package.json` or build script
- Use a catch-all rewrite rule `/(.*)`
- Set absolute image paths (`/images/...`)
- Use `vh`, `dvh`, or `svh` for section heights
- Add `node_modules/` or `.gitignore` inside this folder
- Add unused files to `images/logos/` — keep only actively referenced files

---

## 📐 Page Section Order

1. **HERO** — Deadlift man, dark overlay, CTA
2. **SOCIAL PROOF STRIP** — 4.7★, 5,000+ patients, board-certified, 503A pharmacy, all 50 states
3. **AS SEEN IN** — Business Insider, Yahoo Finance, AP News, Digital Journal, Science Times, Digital Fitness World
4. **SYMPTOM CHECKER** — "Are You a Candidate?" + stat card
5. **BEFORE & AFTER** — Real Patient Results (trt-result-1.jpg, trt-result-2.jpg)
6. **DOCTORS CAROUSEL** — 11 board-certified physicians
7. **INLINE CTA** — "Ready to Feel Like Yourself Again?"
8. **BENEFITS** — 6 benefit cards (energy, muscle, fat loss, clarity, libido, sleep)
9. **TIMELINE** — 4 cards (Weeks 1–2, 3–6, Month 2–3, 3–6)
10. **THE SCIENCE** — Data bars, mechanism cards, clinical references + CTA
11. **TRANSPARENT PRICING** — Comparison cards ($400 clinic vs $199 flat)
12. **TESTIMONIALS** — 5 Trustpilot-verified reviews
13. **FAQ** — 6 accordion questions (2 with clinical references: safety + results timeline)
14. **SERMORELIN CROSS-SELL** — Banner
15. **FINAL CTA BAND** — "Take Back Your Testosterone. Start Today."
