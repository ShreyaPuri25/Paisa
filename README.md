# Paisa — Expense Tracker

A single-file, self-hosted expense tracker. Upload a bank statement CSV, auto-categorize spending, track subscriptions and budgets, and watch month-over-month trends. All data stays in your browser (localStorage) — nothing is sent anywhere.

Pre-loaded with May 2026 data to start.

## Features

- **Auto-categorization** of HDFC-style UPI statements (CSV / TSV)
- **Subscriptions** tab — Netflix, YouTube, Apple & co. split out, with auto-detected recurring payments
- **Budgets** with live progress bars
- **Trends** — income vs spending vs invested across months
- **CSV export** (top-right ↓ CSV button)
- **Investments / FD-RD / card bills** kept separate from lifestyle spending
- **Unlimited retention** — every month you import is kept until you clear browser data
- iPad-friendly: import picks files straight from the Files app

## Deploy to GitHub Pages (2 minutes)

1. Create a new repo, e.g. `paisa`.
1. Add `index.html` and `.nojekyll` to the root and push.
1. Repo → **Settings → Pages** → Source: **Deploy from a branch** → Branch: `main` / root → Save.
1. Open `https://<your-username>.github.io/paisa/`.

That’s it — no build step, no dependencies to install. React, Recharts and Babel load from CDN.

## Run locally

Just open `index.html` in a browser, or:

```bash
python3 -m http.server 8000   # then visit http://localhost:8000
```

## Import format

Your CSV needs a **Date**, a **Description / Narration**, and either an **Amount** column or separate **Withdrawal / Deposit** columns. The HDFC statement export works as-is once saved to CSV.

## Data & privacy

Everything lives in `localStorage` under the `paisa_` prefix. Clearing browser data wipes it — use the **CSV export** button to keep backups.