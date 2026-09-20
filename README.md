# AIhot · Daily AI Briefing (aihot.space)

A **zero-dependency, fully static** Chinese AI news aggregator. Every day it automatically pulls AI news from aihot, then deduplicates, categorizes, and scores it into a single-page daily briefing. Once a week it also rolls up a curated weekly report. The site is deployed automatically by **Cloudflare Pages** — no backend, no build step.

- Visit online: https://aihot.space
- Content source: aihot (a Chinese AI news aggregation platform)
- Tech form: single-file HTML with inline CSS/JS, no CDN, no external font/image dependencies, works offline

---

## What this project does

It turns the AI news scattered across the web each day into a **clean, scannable Chinese daily briefing**. In minutes you can see what new models/products shipped, what happened in the industry, which papers are worth reading, and what practical tips surfaced.

- News is **deduplicated by event** (only the 1–2 most important items per story), so no flood of duplicates.
- Sorted by a **popularity score**; each category shows Top 10 by default, with an option to switch to "All".
- Every item carries a **source attribution and original link** for deeper reading.

## What you can get from it

### 1. Daily AI Briefing (updated daily)

Each day we aggregate the past 24 hours of Chinese AI news into 5 fixed categories:

| Category | Examples |
| --- | --- |
| **Models** | New model releases, version updates, capability benchmarks |
| **Products** | AI apps, tools, and platform launches & iterations |
| **Industry** | Company moves, funding/M&A, policy & regulation |
| **Papers** | Frontier research, new arXiv works, method breakthroughs |
| **Tips** | How-tos, prompt engineering, hands-on experience |

Each news card contains: a global sequential number, title, **popularity score**, source, a **≤60-character Chinese summary**, and an **original link** (opens in a new tab via `target=_blank`).

### 2. AI Hot Topics Leaderboard

A **Top trending-events board** at the top of each daily briefing (highlighted in warm orange) — catch the day's main storyline at a glance.

### 3. Weekly AI Report (updated weekly)

A curated editor's pick from the source platform, aggregated by calendar week with section-by-section deep dives. Weekly report folders are named after the **week's end date (Sunday)**.

---

## How to access the content

The site is archived by date, with fixed URL patterns:

- Daily: `https://aihot.space/days/YYYYMMDD/` (e.g. `days/20260920/` = the 2026-09-20 briefing)
- Weekly: `https://aihot.space/weekly/YYYYMMDD/` (e.g. `weekly/20260913/` = the week 2026-09-07 ~ 09-13)
- Home: `https://aihot.space/` — entry to the latest briefing + archive of past dailies/weeklies

> Cadence: the daily briefing updates every **Beijing Time** calendar day; the weekly report publishes a few days after each week ends.

## Technical features

- **Fully static, zero runtime dependencies**: one HTML file holds all styles and scripts — no build step.
- **Native responsive**: desktop shows a two-column layout (left category nav + main card grid); narrow screens collapse to a top nav bar.
- **Offline-friendly**: no external resources, so you can download and open it locally with a double-click.
- **Lightweight**: no tracking, no ads, no third-party scripts.

## Local preview

After cloning the repo, start any static server from the project root:

```bash
python -m http.server 8765
# open http://127.0.0.1:8765/ in your browser
```

## Disclaimer

All content on this site comes from a third-party aggregation platform (aihot); copyright belongs to the original authors. This site only **organizes and aggregates** the material, and every item is attributed with its source and original link. It is not used for commercial purposes. For takedown or removal requests, please contact the maintainer.

---

_This project is a personal AI news aggregation effort, built to help you track the AI field's daily developments more efficiently._
