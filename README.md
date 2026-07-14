# 📅 Weekly Timetable — Sem III

A clean, installable weekly timetable app for **Diploma in Computer Science & Engineering — Sem III (Batches B1 & B2)**. Works offline, installs like a native app on Android and iPhone, and switches between a mobile-friendly day view and a full desktop grid view.

**🔗 Live app:** _add your GitHub Pages link here once deployed_

---

## ✨ Features

- **📱 Day view (agenda)** — scrollable list of today's (or any selected day's) classes with time, subject, and room. Optimized for phones.
- **🖥️ Week view (grid)** — full Monday–Saturday timetable grid for wider screens, with sticky headers and time column.
- **🔀 Batch toggle** — switch instantly between Batch B1 and Batch B2.
- **📆 Day navigator** — quick-jump pills to any day of the week (mobile view).
- **🟢 Today highlighting** — current day is auto-highlighted in both views, with a "TODAY" badge.
- **🎨 Color-coded lecture types:**
  - 🟢 Common lecture (same for both batches)
  - 🟠 Batch-specific lecture (differs between B1 & B2)
  - 🔴 Weekly Off
  - ⚪ Free / no lecture
  - ⬜ Break
- **👩‍🏫 Faculty & subject legend** — quick reference table of subject codes, full names, and faculty.
- **📲 Installable app (PWA)** — add it to your home screen on **Android** or **iPhone** and it behaves like a native app (its own icon, no browser address bar).
- **📡 Offline support** — once loaded, a service worker caches the app so it keeps working with no internet connection.
- **🌐 Install banner** — the app prompts you to install itself, with tailored instructions for iOS vs Android.

---

## 📥 How to install

### Android (Chrome)
1. Open the live link (above)
2. Tap **Add to Home Screen** when the banner appears (or use Chrome's menu → *Install app*)

### iPhone (Safari)
1. Open the live link (above) in **Safari** (not Chrome)
2. Tap the **Share** icon
3. Tap **Add to Home Screen**

> Once installed, the app opens full-screen with its own icon — just like a regular app.

---

## 🗂️ Repo structure

| File | Purpose |
|---|---|
| `index.html` | Main app — timetable data, layout, and all logic |
| `manifest.json` | PWA config (app name, icons, theme colors) |
| `sw.js` | Service worker — enables offline caching |
| `icon-192.png`, `icon-512.png` | App icons (Android) |
| `icon-512-maskable.png` | Adaptive icon (Android) |
| `apple-touch-icon.png` | Home screen icon (iOS) |
| `favicon-32.png`, `favicon-16.png` | Browser tab favicons |

---

## 🛠️ Updating the timetable

All schedule data lives inside `index.html` in the `DATA` and `WINDOWS` JavaScript objects near the bottom of the file. Batch-specific slots use `{B1: "...", B2: "..."}` objects; shared slots are plain strings. Edit the relevant day/batch entry, commit, and GitHub Pages will redeploy automatically within a minute or two.

---

## 📌 Notes

- Hosted via **GitHub Pages** — HTTPS is required for offline/install features to work, so the app only behaves as a full PWA when accessed via the live link (not when opened as a local file).
- w.e.f. 13 July 2026 · Rev 0
