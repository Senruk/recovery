# Renaissance — Daily Life Tracker

#life #tracker #dashboard #pwa #gamification #supabase

A personal gamified life dashboard at `C:\Users\senru\Documents\Daily-Life-Tracker`.

## Features

- **XP/Level system** — gamified progression with gold/purple theme
- **Water intake tracker** — with quick-add buttons
- **Mood tracking** — emoji-based daily check-in
- **Goals/Tasks** — with checkboxes and progress bar
- **Habit streaks** — daily habit tracking with streak counts
- **KPI dashboard** — hours, earnings, spending, domains, mood, water
- **Pulse chart** — weekly activity bar chart via Chart.js
- **Time tracking** — categories with expandable domains
- **Google Sign-In** — for cloud sync
- **PWA** — `renaissance-pwa/` has manifest.json + service worker

### New Features (June 2026)

- **AI Widget Builder** — describe a widget, AI generates it inline
- **NLQ Chat** — FAB button, natural language queries about your data
- **Badge System** — 15 achievements with unlock tracking
- **Theme System** — 4 themes (Renaissance, Midnight, Emerald, Royal)
- **Custom Domains** — user-defined time tracking categories
- **Proactive Insights** — AI-powered daily suggestions
- **Smart Study** — AI study plans based on past performance
- **Dynamic Weekly Reports** — 3-part AI narrative weekly insights
- **Data Backup/Restore** — full JSON export/import
- **Supabase Auth** — multi-user login/signup
- **Cloud Sync** — data synced to Supabase with RLS

## Navigation

Bottom nav with 8 views: Today, Weekly, Health, Gym, Resell, Recovery, Study, Widgets

## Architecture

- Single-file PWA (HTML/CSS/JS in index.html)
- Groq API (`llama-3.3-70b-versatile`) for AI features
- Google Fit OAuth for health data
- Chart.js for visualizations
- localStorage + Supabase dual-write persistence
- Supabase Auth for multi-user support
- Row-Level Security for data isolation

## Related

- [[Session 2026-06-07 Renaissance App Overhaul]] — full session notes
