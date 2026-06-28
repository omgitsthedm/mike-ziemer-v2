# Mike Ziemer AI-Ops Rules Header

Project Code:

LFNYC-MZ

Project Name:

Mike Ziemer

Business Line:

Client Projects under Little Fight NYC

Tier:

Tier 3 — personal-brand / marketing site

Risk:

Low — static brand site; contact form only, no payments/regulated content

Canonical Path:

/Users/davidmarsh/Desktop/LiFi NYC/Clients/Mike Ziemer/mike-ziemer-v2

Remote:

https://github.com/omgitsthedm/mike-ziemer-v2.git  (default branch: `master`)

Host:

Netlify — **static site, `publish = "."`** (whole repo root), no build. Internal files are blocked from public serving via forced-404 redirects on `/CLAUDE.md`, `/AGENTS.md`, and `/.ai/*` (so `.ai/`, `CLAUDE.md`, `AGENTS.md` are NOT public).

Live URL:

https://mike-ziemer.netlify.app

Stack:

Static HTML/CSS/JS. No framework, no build step.

## Commands

- Dev / preview: serve the folder statically (e.g. `npx serve .` or `netlify dev`); no build needed.
- Build: none (`publish = "."`, static).
- Deploy: **MANUAL Netlify deploy** — `netlify deploy --prod --dir=.` (git is NOT wired to live; git origin is divergent/stale). Deploy = production action → gated by `APPROVE LIVE CHANGE`.

## Locked Rules

- **Git is NOT live.** Live is a manual Netlify deploy; the git remote is divergent/stale. Never treat a git push as a deploy.
- Live client site — treat any deploy or live mutation as a production action (gated by `APPROVE LIVE CHANGE`).
- The contact / lead form is a real submission path — do not submit test leads against production.
- Images `.webp` + `width`/`height` + lazy-load below the fold. Mobile-first, WCAG AA, LiFi footer.
- `.env`/secrets are never read. DNS/domain/billing changes are gated.
- `.ai/`, `CLAUDE.md`, `AGENTS.md` stay private via the forced-404 redirects in `netlify.toml` — do not remove them.

## QA Harness Map

Observational (agent may run): `git status/log`, read source/config, static local serve, public GET to the live `.netlify.app` URL, read-only Netlify deploy metadata (`netlify api listSiteDeploys`).

Transactional/gated (David-run / approved): any Netlify deploy; real contact/lead-form submissions; DNS/domain/env/billing changes.
