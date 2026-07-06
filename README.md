# Wakara Secure360 Challenge

A free interactive cybersecurity, AI governance, and digital resilience assessment platform for SMEs, built by Wakara Technologies Limited.

## Live Flow

1. `index.html` — Landing page with hero, how-it-works, and category overview.
2. `assessment.html` — Business persona selection, 5 interactive risk scenarios with live scoring and feedback.
3. `report.html` — Dashboard (radar + category charts, badges), lead capture form, PDF report generation, and consultation funnel.

## Tech Stack

- HTML5 + Tailwind CSS (CDN)
- Vanilla JavaScript (ES6)
- Chart.js for radar/bar charts
- jsPDF for client-side PDF report generation
- Browser Local Storage for session state (no backend required)

## Structure

```
index.html          # landing page
assessment.html     # assessment flow
report.html         # results dashboard + PDF report
scan.html           # website security snapshot
styles.css          # shared styles
app.js              # session persistence, shared helpers
scenarios.js        # loads scenario data
scoring.js          # scoring engine (people/process/technology/data/AI pillars)
charts.js           # Chart.js radar + bar chart renderers
pdf.js              # jsPDF report builder
leadcapture.js      # lead form validation + storage
scannerworker.js    # Cloudflare Worker for the security scanner
scenarios.json      # personas, scenarios, badges, risk levels
.nojekyll           # prevents Jekyll processing on GitHub Pages
```

## Running Locally

This is a static site — no build step required.

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Deployment

Designed for GitHub Pages — push to the `main` branch and enable Pages in repo Settings → Pages → Source: Deploy from branch (`main`, root `/`). No build step needed.

The `.nojekyll` file at the root ensures GitHub Pages serves the static files directly without Jekyll preprocessing.

Live site: `https://anny320.github.io/secure360/`
