# DEPLOY — TRT Landing Page
**Precision Telemed · Testosterone Replacement Therapy**

---

## ✅ Conventions Checklist

- [x] No `vh`, `dvh`, or `svh` units used for section/hero heights
- [x] Hero uses `min-height: clamp(560px, 60vw, 860px)` with `height: auto`
- [x] Hero `<img>` uses `object-fit: cover`
- [x] All `position: absolute` layers are inside explicit-height parents
- [x] Brand CSS color tokens applied (`--color-primary`, `--color-fg`, etc.)
- [x] `--section-gap: clamp(1rem, 2vw, 1.5rem)` used throughout
- [x] `overflow-x: hidden` on `#page-wrap`
- [x] All image paths are relative (`images/...`)
- [x] `vercel.json` contains only `{ "cleanUrls": true }`
- [x] Hero image downloaded locally (`images/hero-bg.jpg`)
- [x] Science visual downloaded locally (`images/science-visual-trt-v3.jpg`)

---

## 📁 File Structure

```
vercel-trt/
├─ index.html                        ← Single-file landing page (inline CSS + JS)
├─ vercel.json                       ← { "cleanUrls": true }
├─ DEPLOY.md                         ← This file
├─ download                          ← Empty placeholder
└─ images/
   ├─ hero-bg.jpg                    ← Hero background (downloaded locally)
   ├─ science-visual-trt-v3.jpg      ← Science section image
   ├─ trt-result-1.jpg               ← Before/after result photo 1
   ├─ trt-result-2.jpg               ← Before/after result photo 2
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
      ├─ lecom.svg
      ├─ utmb-health.svg
      ├─ cu-colorado.svg
      ├─ ponce.svg
      ├─ vanderbilt.svg
      ├─ tel-aviv.svg
      ├─ texas-tech.svg
      ├─ cleveland-state.svg
      ├─ maryville.svg
      └─ kentucky.svg
```

---

## 🔗 CTA URLs

| Button | URL |
|---|---|
| Check My Eligibility (primary) | `https://precisiontelemed.com/start-testosterone-program/` |
| Consult a Doctor First | `https://precisiontelemed.com/start-general-consultation-program/` |
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
13. **FAQ** — 6 accordion questions
14. **SERMORELIN CROSS-SELL** — Banner
15. **FINAL CTA BAND** — "Take Back Your Testosterone. Start Today."
