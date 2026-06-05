# 30-Day Cut Tracker 💪

A simple, self-contained web app for running a strict 30-day fat-loss program — diet plan, workout split, and a daily progress tracker with notes, all in one page.

Built as a single `index.html` file with no frameworks, no build step, and no dependencies. Just open it and go.

---

## What it does

The app has three tabs:

- **Eat** — the daily meal plan (~2,200 kcal, ~180g protein) with a pre-workout shake, three meals, macro breakdown, and food swaps.
- **Train** — a 5-day gym split (Push / Pull / Legs / Upper / Lower+Core) with exercises, sets, reps, and cardio, plus rest-day guidance.
- **Track** — a 30-day log. Tap to check off Train / Diet / Steps / Water for each day, jot daily notes, and watch a live completion percentage. Each week has progression targets built in.

All progress is saved automatically in your browser, so it's there when you come back.

---

## How it works

It's a single HTML file:

- **Structure & styling** — plain HTML and CSS (no React, no Tailwind, no libraries).
- **Logic** — vanilla JavaScript handles tab switching, the tracker grid, and the percentage bar.
- **Saving** — uses the browser's `localStorage`. Your check-offs and notes live in your own browser; nothing is sent anywhere. (This also means data is per-device for now — see the roadmap.)

Because everything is in one file, hosting it is as simple as serving that file.

---

## Run it locally

Clone the repo and open it:

```bash
git clone https://github.com/Pa1kcool/cut-tracker.git
cd cut-tracker
```

Then either:

- **Quickest:** double-click `index.html` to open it in your browser, **or**
- **Local server (recommended):**
  ```bash
  python3 -m http.server 8000
  ```
  Then visit `http://localhost:8000`.

That's it — no install, no build.

---

## Host it on GitHub Pages

GitHub can serve this as a live website for free.

1. Make the repo **public** (Pages is free only on public repos):
   ```bash
   gh repo edit Pa1kcool/cut-tracker --visibility public --accept-visibility-change-consequences
   ```
   *(or do it on the site: repo → Settings → General → Change visibility)*

2. Enable Pages:
   - Go to **Settings → Pages**
   - Under **Source**, choose **Deploy from a branch**
   - Pick branch **main** and folder **/ (root)**, then **Save**

3. Wait ~1 minute. Your site goes live at:
   ```
   https://Pa1kcool.github.io/cut-tracker/
   ```

To publish any future change, just commit and push — Pages redeploys automatically:

```bash
git add .
git commit -m "describe your change"
git push
```

---

## Roadmap

Possible next steps as the project grows:

- **Cross-device sync** — move from `localStorage` to a backend (Supabase / Firebase) so progress follows you across phone and laptop.
- **Accounts & login** — multi-user support.
- **PWA** — make it installable on a phone home screen.
- **Dockerize** — containerize for consistent deployment anywhere.
- **Native app** — wrap with Capacitor for the App Store.

---

## Disclaimer

This is a personal fitness tool, not medical advice. Consult a doctor before starting any new diet or training program.
