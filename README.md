# 日本語の世界 — Nihongo no Sekai

A static, reading-first Japanese learning website. Open `index.html` locally or host it with GitHub Pages.

## What exists now
- Volume 0: 19 authored introductory lessons (0.1–0.19), explanations, example sentences, short stories, vocabulary, 59 auto-checked questions, writing prompts, and memory tips.
- Volume 1–6: library placeholders only, **not** completed textbooks.

- Dark mode, focus reading mode, mobile layout, local progress, JSON backup and restore.

## Publish to GitHub Pages
1. Create a public GitHub repository (e.g. `nihongo-no-sekai`).
2. Upload `index.html`, `assets/`, and `data/` into the repository root.
3. In repository Settings → Pages, select **Deploy from a branch**, `main`, `/ (root)` and Save.
4. Open the URL shown by GitHub Pages once deployment finishes.

No build step, npm install, backend or paid service required. Google Fonts are optional and require internet; local fallback fonts work offline.

## Add future content
- Existing lesson data is in `data/volume0.js` as `window.VOLUME0 = [...]`.
- Each lesson has `slug`, `title`, `subtitle`, `goal`, `concepts`, `examples`, `story`, `translation`, `words`, `questions`, `task`, `tip`.
- The volume list and routing are in `assets/app.js`. To activate a new volume, add a separate data file, include it in `index.html`, and extend the router and sidebar. The placeholders currently have stable `#/volume/1` etc. URLs.
- For long-term maintenance, migrate each lesson to an individual JSON/Markdown content file with a static-site generator. This zero-build release is designed to be simple to publish first.

## Content limitations


## Privacy
Progress uses browser localStorage. Export backups because browser cleanup can delete it. No analytics or accounts.

## Reading-first pronunciation edition
All in-page speech synthesis, voice selectors, audio buttons, and audio diagnostic panels have been removed. The new Pronunciation Guide gives rough English comparison words, articulation guidance, mora drills, minimal pairs and a read-cover-type routine. English approximations are not exact Japanese phonetics. External native-audio websites remain optional.
