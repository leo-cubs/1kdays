# Sow Calendar

A configurable Gregorian calendar plus a 1000-day pig-production wall-planner calendar.

Single-file static app: `index.html`. No build step, no dependencies beyond a Google Fonts stylesheet link.

## Features

- **Calendar** — standard Gregorian month view. Today is highlighted; the first day of the week is configurable (Sunday–Saturday).
- **1000-Day Planner** — the continuous day-numbered wall-planner grid used in pig production, laid out in weekly rows from a chosen Day 1 start date, browsable in pages with a "jump to today" and "jump to day N" shortcut. Today is highlighted.
  - Add breeding batches (a label, color, and first-service/AI date). Each batch auto-projects farrowing (service + gestation, default 114 days) and weaning (farrowing + lactation, default 21 days), then chains the next service date (weaning + wean-to-service interval, default 5 days) and repeats for as long as the planner range covers — so one entry shows a sow group's whole reproductive cycle across the 1000 days.
  - Gestation length, lactation length, wean-to-service interval, start date, and total day count are all adjustable.
- Settings (week start, theme, planner config, batches) persist in the browser via `localStorage`.

## Running locally

It's a static file — open `index.html` directly in a browser, or serve it:

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080`.
