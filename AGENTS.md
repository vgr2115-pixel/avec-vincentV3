# AGENTS.md

## Project overview

Static marketing website for "AVEC VINCENT" (private tutoring in Lyon).
Pure HTML/CSS/JS — no build step, no backend, no package manager, no dependencies.

## Running the app

Served via nginx (docker-compose.base44.yml) on host port 3000.
Files are bind-mounted read-only, so HTML/CSS/JS edits appear on browser refresh — no rebuild needed.

```
docker compose -f docker-compose.base44.yml up -d
```

## Key files

- `index.html` — homepage
- `cours.html` — courses & pricing
- `credit-impot.html` — tax credit info
- `a-propos.html` — about / method
- `reserver.html` — booking form (composes a `mailto:` link, no server-side submission)
- `legal.html` — legal pages
- `script.js` — nav toggle, contact info injection, form logic
- `style.css` — all styling

## No secrets required

The site has no backend or external API calls. No credentials are needed.
