# Mike Ziemer AI-Ops State

## Identity

- Project Code: LFNYC-MZ
- Name: Mike Ziemer
- Tier / Risk: Tier 3 — personal-brand / marketing site · Low — static brand site; contact form only, no payments/regulated content
- Canonical Path: /Users/davidmarsh/Desktop/LiFi NYC/Clients/Mike Ziemer/mike-ziemer-v2
- Git-backed: yes · Remote: https://github.com/omgitsthedm/mike-ziemer-v2.git · Default branch: `master`

## Current Stamp

- Updated: 2026-06-28
- Updated By: Claude
- Basis: AI-Ops onboarding (LOCAL ONLY — no push/deploy). Read-only Netlify metadata.
- Git HEAD at onboarding: d86dd8b

## Rules Version

- 2026-06-27-aiops-foundation-v1

## Deploy Model (CRITICAL — git != live)

**MANUAL** Netlify deploy. Every deploy on both sibling projects has `commit_ref: null` (no Git auto-deploy). Latest live deploy 2026-01-31. No custom domain.

- Verify deploy metadata read-only with:
  `netlify api listSiteDeploys --data '{"site_id":"<id>","per_page":5}'`
  (`commit_ref: null` = manual deploy; a non-null commit_ref = a historical git-triggered deploy.)
- **Never `git push` expecting it to update the live site.** Promotion to live is a manual `netlify deploy --prod` and is gated by `APPROVE LIVE CHANGE`.

## Current Live Truth

- Live URL: https://mike-ziemer.netlify.app
- Host: Netlify, static `publish = "."`, no build.
- `.ai/`, `CLAUDE.md`, `AGENTS.md` blocked from public serving via forced-404 redirects in `netlify.toml`.
- Business: Mike Ziemer — Dallas-based concert promoter, festival producer & marketing consultant (20+ yrs in the music industry)
- Production QA status: not run by AI-Ops.
- Netlify projects: `mike-ziemer` (live, manual, last deploy 2026-01-31 19:19) and `mike-ziemer-v1` (older manual site, 2026-01-31 06:12). Canonical repo `mike-ziemer-v2` is deployed (manually) to the `mike-ziemer` project — name mismatch is expected.

## Superseded / Old Versions (do NOT onboard or deploy)

- `mike-ziemer` (repo) — placeholder only (single `README.md`, no site/HTML). The `mike-ziemer` Netlify project is fed manually from repo `mike-ziemer-v2`, not this repo.
- Netlify `mike-ziemer-v1` — older superseded site.

## Why This Repo Is Canonical

`mike-ziemer-v2` is the only repo with an actual site (8 HTML pages, 335 files); `mike-ziemer` contains nothing but a README. Most-recent git activity (2026-04-08) also belongs to v2. Matches the existing client-folder CLAUDE.md.

## QA-PENDING

- Confirm `/.ai/*`, `/CLAUDE.md`, `/AGENTS.md` return 404 on live AFTER the next manual deploy (observational GET). The forced-404 redirects were committed locally but are not live until a manual deploy ships them.
- Confirm with David which Netlify project is the intended single source of truth where sibling projects exist.

## Do Not Touch

- `.env` / secrets / API keys.
- The forced-404 redirects in `netlify.toml` (keeps internal docs private).
- Any Netlify deploy or live mutation without `APPROVE LIVE CHANGE`.
- The superseded repos / sibling Netlify projects listed above.

## Proposed Changes / Inbox

- None yet.

## Next Steps Queue

- Optional: prune/retire the superseded sibling repos + Netlify projects once David confirms the canonical pairing.
- Verify private-file 404s on live after the next manual deploy.

## Recent Session History

- 2026-06-28: Claude onboarded Mike Ziemer to the AI-Ops standard (LOCAL ONLY). Picked canonical repo `mike-ziemer-v2`, created `.ai/{LOCK,RULES_HEADER,RULES,STATE}.md` + repo `AGENTS.md` + repo `CLAUDE.md` (Commands + AI-Ops pointer), and added/extended `netlify.toml` with forced-404 excludes for `/.ai/*`, `/CLAUDE.md`, `/AGENTS.md`. Committed locally only — no push, no deploy. Recorded the manual deploy model (git != live).

## Next Agent Directive

Read `.ai/RULES.md` + `.ai/STATE.md` + `CLAUDE.md` first. **Git is NOT live** — live is a manual Netlify deploy and the git origin is divergent/stale. Any deploy or live mutation is gated by `APPROVE LIVE CHANGE`. Don't read `.env`/secrets. Don't touch the superseded repos / sibling Netlify projects. Keep the forced-404 redirects.

## Emergency / Bypass Notes

- No bypass for deploy / live mutations / secrets / DNS / billing.
- Emergency mode: stop, preserve evidence, smallest reversible action, ask David.
