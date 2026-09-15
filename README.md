# Car Trends

Static HTML dashboards for tracked car listing prices (Ferrari, McLaren, Lamborghini, Ford GT Gen 1).

## GitHub Pages

1. Repo Settings → Pages
2. Source: Deploy from branch `main` / root (`/`)
3. Site URL: `https://dboundz.github.io/car-trends/`

### Canonical brand pages
- `ferrari.html`, `mclaren.html`, `lamborghini.html`, `ford.html`

### Legacy redirects (bookmarks / social)
- `ferrari-488-f8.html` → `ferrari.html`
- `mclaren-lt.html` → `mclaren.html`
- `lamborghini-huracan.html` / `lamborghini-aventador-sv.html` → `lamborghini.html`
- `ford-gt-gen1.html` → `ford.html`

Dashboards are self-contained (data embedded). Chart.js loads from CDN.


## Download data (JSON)

Same payloads embedded in the dashboards (for friends & tooling):

- https://dboundz.github.io/car-trends/ferrari.json
- https://dboundz.github.io/car-trends/mclaren.json
- https://dboundz.github.io/car-trends/lamborghini.json
- https://dboundz.github.io/car-trends/ford.json
- https://dboundz.github.io/car-trends/data.json (overview)
- Index: https://dboundz.github.io/car-trends/data/

Each brand page footer has **Download data (JSON)**.
