# Daily Planner PWA — Setup Guide

## What's included
- `index.html`  — the full app (one file)
- `manifest.json` — PWA install config
- `sw.js`         — service worker (offline support)
- `icon-192.png` / `icon-512.png` — app icons

---

## How to install on Pixel 7 (Android)

### Option A — Host it yourself (recommended)
1. Put all 5 files on any web host (GitHub Pages, Netlify, Vercel — all free)
2. Open Chrome on your Pixel 7 and navigate to the URL
3. Tap the **⋮ menu → "Add to Home screen"**
4. Done — it installs like a native app

### Option B — Run locally with a quick Python server
If you're on the same WiFi as your PC:
```bash
cd /path/to/planner
python3 -m http.server 8080
```
Then on your Pixel, open Chrome and go to `http://YOUR-PC-IP:8080`

### Option C — GitHub Pages (easiest free hosting)
1. Create a GitHub repo, upload all 5 files
2. Go to Settings → Pages → Deploy from main branch
3. Your URL: `https://yourusername.github.io/repo-name`

---

## Features
- **Hour-by-hour timeline** for every day
- **Swipe left/right** to navigate days
- **Alarm sounds** using Web Audio API (works even in background if PWA installed)
- **System notifications** (accept permission prompt on first launch)
- **Color-coded events** — 5 colors
- **Duration display** — shows start–end time on each event chip
- **Optional notes** per event
- **Per-event alarm toggle**
- **Offline support** — works without internet after first load
- **Data persists** in localStorage (survives app close/reopen)
- **Settings tab** — toggle sounds/banners, clear all events

## Alarm notes
- Alarms use Web Audio (synthesized tones) — no audio file needed
- The app must be open OR installed as a PWA for alarms to fire
- Accept the notification permission on first launch for system banners
- Alarms are scheduled up to 48 hours in advance
