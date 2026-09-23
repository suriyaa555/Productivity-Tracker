# 🎮 Productivity Quest

A personal, gamified habit tracker — turn your daily routine into an XP-earning quest. Built as a single, self-contained static website (HTML + CSS + JavaScript, no build step, no backend).

**Live site:** https://suriyaa555.github.io/Productivity-Tracker/

---

## Features

- **Daily tasks with XP rewards** — Cardio, Weightlifting, Coursera, Job Applying, DSA/LeetCode.
- **Levels & XP bar** — earn 300 XP per level.
- **Weekly goal** — hit **600 XP in a week** to unlock your "meal out" reward 🎉.
- **Streaks** — current streak and best streak, so you *don't break the chain*.
- **Calendar view** — month-by-month grid (◀ ▶ to browse) showing which days you stayed on track.
- **Public read-only + private editing** — anyone can view your progress; only you (after logging in) can check off tasks.
- **Autosaved login** — once you log in on a device/browser, it won't ask again.
- **Offline & private** — all progress is stored in your browser's `localStorage`.

## How editing works

| Who | What they can do |
|-----|------------------|
| Visitors (not logged in) | View everything — tasks, XP, streaks, calendar — **read-only** |
| You (logged in) | Check off / uncheck **today's** tasks |
| Anyone | Click any calendar day to **view** that day's status |

> ⚠️ **Only today's tasks can be changed.** Previous days are view-only (you can see what you completed, but not edit history). Future days are view-only too.

## Login (client-side)

This is a personal, low-stakes tracker, so authentication is handled entirely in the browser. Credentials live in `index.html`:

```js
const AUTH = {
  username: "suriyaa8904",
  password: "quest-tracker-2026"
};
```

> **Security note:** Because this is a static site, these credentials are visible in the page source. This is fine for a personal tracker but is **not** real security — don't reuse this password anywhere important. Change it anytime by editing the `AUTH` block above.

## Customizing

Everything is configurable near the top of the `<script>` in `index.html`:

- **`TASKS`** — add/remove tasks or change their XP values.
- **`XP_PER_LEVEL`** — XP required per level (default `300`).
- **`WEEKLY_GOAL`** — weekly XP target for your reward (default `600`).

## Running locally

No server or install needed — just open the file:

```bash
# clone, then:
open index.html        # macOS
# or double-click index.html in your file explorer
```

## Deployment (GitHub Pages)

This repo is served via GitHub Pages from the `main` branch root. Any push to `main` updates the live site.

---

*Built as a personal project. Data stays in your browser — nothing is sent to any server.*
