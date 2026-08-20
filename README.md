# 1KDays

A Gregorian calendar paired with the 1000-day cycle-day count used in pig production, plus breeding-batch tracking for service, farrowing, and weaning dates.

Live at [1kdays.mncubs.com](https://1kdays.mncubs.com).

Single-file static app: `index.html`. No build step, no dependencies beyond a Google Fonts stylesheet link.

## Features

- **Monthly calendar** — standard Gregorian month view, with the 1000-day cycle-day label (`CC-DDD`) shown on every date. Today is highlighted; the first day of the week is configurable (Sunday–Saturday).
- **1000-day cycle-day count** — a continuous day count since a configurable reference date (Cycle 00 / Day 000), formatted as `CC-DDD` and wrapping into a new cycle every 1000 days. A "jump to cycle-day" field jumps the calendar straight to any `CC-DDD`.
- **Breeding batches** — add a label, color, and first-service (AI) date. Each batch auto-projects farrowing (service + gestation, default 114 days) and weaning (farrowing + lactation, default 21 days) for that one cycle. A configurable ± day window (default 3) marks the days around the expected farrowing date, since gestation length varies. Batch colors are kept unique — a color already in use is disabled with the next free one auto-suggested.
- **Batch history** — once a batch's weaning date passes, it's automatically archived out of the active list into a collapsible History section, freeing its color for reuse. Its dates keep showing correctly on the calendar wherever you browse back to them.
- **Tap any day** to see its cycle-day and any breeding batch whose cycle covers it — service, farrowing, weaning, possible farrowing window, or "day N of gestation/lactation" — plus the full date set for that cycle.
- Swipe left/right on the grid, or use the prev/next buttons, to change month.
- Light/dark theme (system-aware, with a manual toggle), with settings and batches saved in the browser via `localStorage`.
- Installable as a home-screen app; prompts to refresh when a new version is deployed.

## Running locally

It's a static file — open `index.html` directly in a browser, or serve it:

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080`.
