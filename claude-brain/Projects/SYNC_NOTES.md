# RenV2 Sync Notes

## Current State

### Completed
- [x] `js/config.js` — localStorage-only config, version 2.0.0
- [x] `js/store.js` — STATE, DOMAINS (9 domains), XP/leveling, save+verify, toast system
- [x] `js/views/today.js` — Today view: domain hour logging with entries, mood tracker (5-tier), water logging (4 quick-add amounts), recent activity feed
- [x] `js/views/weekly.js` — Weekly view: 7-day history table, domain breakdown with progress bars, summary KPIs
- [x] `js/app.js` — Bootstrap: initToday() → renderToday() → nav handlers (today/weekly/settings)
- [x] `css/app.css` — Gold/black theme, cards, KPI grid, mood/water buttons, log items
- [x] `index.html` — PWA-ready HTML with sticky header (brand/XP), bottom nav, toast container
- [x] Git repo initialized + committed
- [x] Brain note saved to vault + _MOC.md updated

### NOT Done
- [ ] Deploy to Cloudflare Pages (needs GitHub repo + CF Pages project linking)
- [ ] Test on mobile Safari (PWA localStorage behavior)
- [ ] Settings view content (basic version exists in app.js)
- [ ] Habit tracking UI (store supports it but no view yet)
- [ ] Expense tracking UI (store supports it but no view yet)
- [ ] Sleep tracking UI (store supports it but no view yet)
- [ ] Goals UI (store supports it but no view yet)
- [ ] Reflection/journal UI (store supports it but no view yet)

### V2 Bug Fixes (vs V1)
1. Auth blocking init → NO AUTH. app.js calls `REN_INIT()` immediately after definition
2. Deprecated Groq model 404 → NO AI. Pure offline localStorage
3. Cookie fallback corruption → localStorage ONLY with save verification (read-back check)

### Key Code Paths
- Save: `saveToday()` in store.js → writes localStorage → verifies by read-back → updates history snapshot
- Load: `loadState()` in store.js → reads localStorage → merges missing domain structures
- XP: `calcXP()` sums history snapshots + current day hours × 15 XP/hr; level = floor(XP/100)+1

### Valleys/Cliffs
- `todayKey()` uses local date (not UTC) — fine for personal tracking
- `getDomainHistory()` returns avg/day per domain for the past N days (approximate, from snapshots)
- No offline-first caching yet — localStorage is the only persistence layer

## Tomorrow's Work
1. Deploy V2 to Cloudflare Pages (create GitHub remote first)
2. Mobile test — does localStorage persist on iOS Safari PWA close/reopen?
3. Add Settings view with clear data / export options
