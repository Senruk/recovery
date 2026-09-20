# Renaissance V2 — Daily Life Tracker

**Status:** 🔴 Built — git committed, deploying to Cloudflare Pages
**Date:** 22 August 2026
**Path:** `claude-brain/projects/renV2/`

## Why V2?

V1 had 3 critical issues:
1. **Auth blocking init** — `checkAuthOnLoad()` ran before `init()`, so the UI never populated even though user saw "logged in"
2. **Deprecated Groq model** — `llama-3.3-70b-versatile` returns 404, AI features broken
3. **Save corruption** — cookie fallback (4KB limit) silently corrupted localStorage; JSON.parse failures on every load

V2 is a clean rebuild: **no auth, no external APIs, no cookies**. Pure localStorage PWA.

## Architecture

```
renV2/
├── index.html          # PWA manifest, sticky header + bottom nav
├── css/app.css?v=2     # Gold/black theme (no cream/terracotta)
├── js/
│   ├── config.js?v=2   # Storage keys, version
│   ├── store.js?v=2    # Data layer (STATE, DOMAINS, XP, save/verify)
│   ├── app.js?v=2      # Bootstrap (init → render → nav handlers)
│   └── views/
│       ├── today.js    # Domain logging, mood, water, recent activity
│       └── weekly.js   # 7-day history, domain breakdown, summary
```

## Key Design Decisions

- **9 Domains** with emoji + color, not generic task categories
- **XP = 15/hr** logged, level = floor(XP/100)+1
- **Save verification** — immediately reads back from localStorage to confirm write
- **No auth gate** — `REN_INIT()` runs immediately, renders `today` by default
- **Mood: 5-tier** (😩 to 🔥), Water: 150/250/350/500ml quick-add
- **History snapshot** on each save (hours, income, spent, mood, water, timestamp)

## V1 Issues Fixed

| Issue | V1 cause | V2 fix |
|-------|---------|--------|
| Nothing saves | Cookie fallback corrupted JSON | localStorage-only with verified save |
| 404 AI errors | `llama-3.3-70b-versatile` deprecated | No AI — offline only |
| "Logged in but nothing loads" | `checkAuthOnLoad()` before `init()` | No auth. `init()` → `renderToday()` |

## Deployment

- Git repo initialized in `renV2/` (NOT home directory)
- Deployed to: `daily-life-v2.pages.dev` (pending Cloudflare Pages creation)
- Stays separate from V1 at `daily-life-57t.pages.dev`