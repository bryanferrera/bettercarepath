# bettercarepath.com

Three-page static site for M&L In-Home Care:

| Path | File | Purpose |
|---|---|---|
| `/` | `index.html` | Main landing page — organic traffic, full company website |
| `/report` | `report.html` | Lead-capture opt-in for the 2026 Family Care Report (paid social ads) |
| `/thank-you` | `thank-you.html` | Post-submission confirmation + PDF download |

## Local development

```bash
python3 -m http.server 4321
# then open http://localhost:4321
```

## Deployment

Auto-deploys to Vercel on push to `main`. Clean URLs are handled by `vercel.json` (`cleanUrls: true`), so `report.html` is served at `/report`.

## Assets

- `images/` — landing-page and thank-you-page photos
- `assets/2026-family-care-report.pdf` — the lead-magnet PDF (linked from the thank-you page download button)

## Phase 2 (not done yet)

- Replace placeholder form handlers with Go HighLevel API integration (`report.html` form + both landing-page forms)
- Compress `images/why-1.jpg` (21MB) and `images/why-3.jpg` (13MB) — they're served full-resolution today
- Extract inline `<style>` blocks into shared `styles/*.css` if a true design system is needed
