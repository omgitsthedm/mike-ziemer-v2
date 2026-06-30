# SOURCE_OF_TRUTH.md — Mike Ziemer v2

Last verified: 2026-06-30 by Codex.

## Repository

- GitHub: `https://github.com/omgitsthedm/mike-ziemer-v2.git`
- Default branch: `master`
- Canonical working path: `Clients/Mike Ziemer/mike-ziemer-v2`
- Current Codex branch: `codex/agency-standard-mike-ziemer-v2-20260629`
- Backup branch for the original local AI-Ops commit: `backup/consolidation-mike-ziemer-v2-20260629`

## Production Linkage

- Host: Netlify.
- Live URL: `https://mike-ziemer.netlify.app`
- Intended live site: `mike-ziemer`
- Intended live site id: `10a06b60-afab-40cb-9d7a-c9de27dd81fd`
- Publish dir: `.`
- Build command: none.
- Deploy model: manual Netlify deploy; Git is not live and pushing `master` does not publish.
- Any Netlify deploy, DNS/env/billing change, or live contact-form test requires `APPROVE LIVE CHANGE`.

## Current Local Netlify Warning

- `netlify status` in this checkout currently reports `admitiq-pilot` (`97100759-5110-448b-9f44-101d62ce54b3`), not `mike-ziemer`.
- Do not deploy from this checkout until the Netlify link is corrected and David approves the deploy.

## Source Layout

- Static HTML/CSS/JS in the repo root.
- No package manager or build output is required.
- `netlify.toml` contains forced-404 redirects for internal AI docs.

## Clone Topology Observed

- `Clients/Mike Ziemer/mike-ziemer-v2`: canonical; had one local AI-Ops commit ahead of `origin/master`.
- `Clients/Mike Ziemer/Website/current/mike-ziemer-v2`: clean but one commit behind after fetch.
- `Clients/Mike Ziemer/Website/mike-ziemer-v2`: clean but one commit behind after fetch.

## Verification

- Live root returned HTTP 200.
- Live title: `Mike Ziemer | Concert Promoter, Festival Producer, Marketing Consultant`.
- Live `/.ai/STATE.md`, `/CLAUDE.md`, and `/AGENTS.md` returned 404.
- `agency-doctor --fix` installed the standard ignore file, this source-of-truth file, and the local pre-commit secret hook on the Codex branch.
