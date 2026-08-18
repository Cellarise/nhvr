# NHVAS Mass Accreditation Atlas

Single-page interactive map of NHVAS Mass Management accreditation: operators and
nominated mass vehicles by suburb, across the jurisdictions present in the extract.

## What is here

- `index.html` — the whole thing. Data, styles and script are inlined, no build step,
  no external requests.
- `vercel.json` — response headers only (noindex, nosniff, no referrer).

Source data, analysis and the workbook stay in the knowledge repo at
`projects/NHVR/2026-08-17-mass-accreditation-heatmap/output`. Regenerate `index.html`
from `heatmap.html` there if the data changes.

## Data caution

The map names individual accredited operators and their vehicle counts. It is drawn
from an NHVR extract, not from published data. Treat any deployment as needing access
control.

## Deploy on Vercel

1. Push this repo to GitHub (private).
2. In Vercel, import the repo. Framework preset: **Other**. Leave build command and
   output directory empty. Vercel serves the repo root as static files.
3. Turn on **Deployment Protection** (Settings → Deployment Protection) before sharing
   the URL. Vercel Authentication limits access to your team; Password Protection or a
   Shareable Link suits an external reviewer.

## Local check

    python3 -m http.server 8000

Then open http://localhost:8000
