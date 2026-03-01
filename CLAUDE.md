# CLAUDE.md — Ticket Tracker (Beatrice / Person B)

## Who I Am
Beatrice (b-mackenzie-alexander) — **Person B: Frontend**.
My files: `app.js` (primary), `index.html` (styling only, not structure).

## Project Context
Hackathon project for Pursuit — NYC housing maintenance crisis visualizer.
Stack: plain HTML/CSS/JS + Chart.js (CDN). No build step. Served via `python3 -m http.server 8000`.

## Division of Work
- **Ismael (A):** `data-ismael.js` — all HPD API queries
- **Pape (C):** `data-pape.js` — DHS + NYCHA queries; also owns pitch/presentation
- **Beatrice (B):** `app.js` — Chart.js rendering, tables, stat cards, mock data

## My Scope
- `app.js` — charts, tables, stat cards, mock data, `main()` entry point
- `index.html` — CSS/styling tweaks only (not page structure or script tags)
- Do NOT modify `data-ismael.js`, `data-pape.js`, or `data.js`

## Current Mode
`USE_MOCK = true` in `app.js` (line 1).
Ismael will wire in live API once frontend is confirmed working.

## Running Locally
```bash
cd ~/Desktop/ticket-tracker
python3 -m http.server 8000
# open http://localhost:8000
```

## Data Contract
`loadAllData()` (from `data.js`) returns:
```
{
  hero:          { hpdOpenTotal, hpdEmergencyOpen, shelterTotal, shelterChildren }
  avgByType:     [{ type, avgDays, total }]
  avgByPriority: [{ priority, avgDays, total }]
  avgByBoro:     [{ borough, avgDays }]
  openByType:    [{ type, total }]
  oldest:        [{ received, type, priority, borough, address, daysOpen }]
  hpdManaged:    { avgDays, totalClosed, totalOpen, buildingCount }
  shelterTrend:  [{ date, total, children }]
  peakVsNow:     { peak: { date, total }, low: { date, total } }
  nycha:         { byDevelopment: [...], byHazardClass: [...], totalViolations }
}
```
