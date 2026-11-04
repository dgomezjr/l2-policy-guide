# L2 Operations & Policy Guide — Classic Vacations

An internal reference for L2 Customer Service: stages and ownership, booking
changes, air, hotels, cancellations and refunds, payments, goodwill,
escalation, Post-Travel handoff, contacts and routing.

It's a single HTML file. No build step, no server, no dependencies. It runs on
GitHub Pages and can be embedded in SharePoint via iframe, the same way as the
Group Air and RSS Operations guides.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole guide: layout, styling, content (26 topics), and search |
| `README.md` | This file |

Content source: `L2_Guide_Content_v3.md` (kept locally, not published).

## Updating content

All content lives in the `DATA` object inside `index.html`. For anything more
than a small wording fix, send Claude the updated content and have it rebuild
the affected topics so formatting and cross-links stay consistent.

**Before publishing any change:** open `index.html` in a browser and check that
the page loads and search works. A missing comma or quote in `DATA` will blank
the page.

## Publishing

Live at `https://dgomezjr.github.io/l2-policy-guide/`.
GitHub Pages serves the `main` branch, `/ (root)`. Commit a new `index.html`
to `main` and Pages republishes automatically. The repository is public, so
keep confidential material (contract rates, credentials) out of it.

## Embedding in SharePoint

```html
<iframe src="https://dgomezjr.github.io/l2-policy-guide/"
        width="100%" height="900" style="border:0"></iframe>
```

If SharePoint blocks the embed, a site admin needs to allow
`dgomezjr.github.io` under **Site settings → HTML Field Security**.
