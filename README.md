# BVI 2027 — The Ship's Log

Status site for our crewed BVI charter aboard **Do More** (62' Lagoon catamaran), **April 18–25, 2027**, out of Nanny Cay Marina, Tortola.

**Live site:** https://austinfitzpatrick.github.io/bvi2027/

## What's here

- `index.html` — The Ship's Log: booking timeline, action items, guest manifest, cost breakdown, flight suggestions, and contacts. This is the whole site — no build step, no backend.
- `pitch/` — the original boat-selection pitch site, kept for posterity.
- `emails/` — the paper trail: broker email threads, marina hotel emails.
- `guides/` — the broker's getting-there and hotel-suggestion PDFs.
- `contracts/` — the blank CYBA contract draft. Signed documents are NOT here (see below).
- `calendar/` — .ics files linked from the site (charter week, final payment reminder).
- `private/` — gitignored, local only: signed contract, card authorization, receipts, personal travel documents. Never commit these; the site's "Signed contract" link deliberately shows a "ask Austin" toast instead.

## Updating the site

Everything is hand-edited in `index.html`:

- **Guest statuses** live in the `GUESTS` array in the inline script near the bottom. Each task is `"todo"`, `"done"`, `"na"`, `"prog"` (in progress), `"warn"`, or `"unknown"`. Task labels are in `TASK_LABELS`.
- **Timeline and action items** are plain HTML in the `#log` and `#actions` sections.

Publishing is just a push — GitHub Pages serves `main` directly and rebuilds in about a minute:

```sh
git add -A && git commit -m "Update statuses" && git push
```

Note: this repo is public. Keep anything personal (receipts, photos, scratch files) out of it — see `.gitignore`.
