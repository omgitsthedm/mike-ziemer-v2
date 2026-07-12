# CLAUDE.md — Mike Ziemer
> AI-Ops onboarded: 2026-06-28 (canonical repo)
> AI-Ops: read `.ai/RULES.md` + `.ai/STATE.md` first (authoritative). This file is the human summary.

## Commands  (REQUIRED)
- Dev/preview: `npx serve .` (or `netlify dev`) — static site, no build
- Build: none (`publish = "."`)
- Deploy: **MANUAL** — `netlify deploy --prod --dir=.` (**git push does NOT deploy**; git origin is divergent/stale). Deploy = production → needs clear, scoped confirmation from David.
- Lint/format: n/a (static)
- ⚠️ Git is NOT live. The contact/lead form is a real submission path — no test leads against production.

## Client Info
- **Business:** Mike Ziemer — Dallas-based concert promoter, festival producer & marketing consultant (20+ yrs in the music industry)
- **Live URL:** https://mike-ziemer.netlify.app (Netlify, static, no custom domain)
- **Deploy model:** manual Netlify deploy (see `.ai/STATE.md`)
- **Tier / Risk:** Tier 3 — personal-brand / marketing site · Low — static brand site; contact form only, no payments/regulated content

## Canonical / Superseded
- **Canonical repo:** `mike-ziemer-v2` (this folder)
- **Superseded (do not onboard/deploy):** see `.ai/STATE.md` → "Superseded / Old Versions".

## Decisions Log
| Date | Decision | Context |
|------|----------|---------|
| 2026-06-28 | AI-Ops onboarded; `mike-ziemer-v2` chosen as canonical | Version-duplicate cleanup; recorded manual deploy model (git != live) and forced-404 privacy for internal docs |

## Current Status
- **Phase:** deployed / maintenance
- **Last worked on:** 2026-06-28 (AI-Ops onboarding, local only)
- **What's done:** `.ai/` scaffold + AGENTS.md + this CLAUDE.md + `netlify.toml` forced-404 excludes; committed locally
- **What's pending:** verify private-file 404s on live after next manual deploy; David to confirm canonical pairing & retire siblings
- **Needs from David:** confirmation to prune superseded repos / sibling Netlify projects
