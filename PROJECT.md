# cap-ferret-fire-watch-public

## Purpose

Publish the Cap Ferret fire situation dashboard at a neutral, non-commercial web address. This repository contains only the rendered public site and its public incident data; development remains in the private source repository.

## Dependencies

- `ccn000/cap-ferret-fire-watch` produces the static export.
- GitHub Pages serves the `docs/` directory from `main`.

## Architecture

The M4 builds the private Vinext/React dashboard, renders a static HTML snapshot, copies client assets and bilingual JSON into this repository’s `docs/` directory, and pushes the result. GitHub Pages publishes that directory. The embedded snapshot keeps the page readable when the M4 is offline; timestamps make staleness visible.

## File Map

- `docs/`: generated public dashboard.
- `AGENTS.md`: publication and privacy rules.
- `PROJECT.md`: deployment architecture and current state.
- `CHANGELOG.md`: append-only deployment changes.

## Configuration

No runtime secrets or environment variables are stored here. GitHub Pages uses `main` and `/docs`.

## Runtime notes

Publishing is driven from the private source project with `npm run publish:public`. The public output must never become the authoring source.

## Machine-local runtime notes

The canonical M4 clone sits alongside the private source clone under the canonical repository root. No background server is required for GitHub Pages.

## Current state

The neutral Pages URL is being activated. The prior commercial-domain tunnel remains a temporary fallback only until the neutral publication is verified.

## Next TODOs

- [ ] Verify the first GitHub Pages deployment.
- [ ] Add the public publish command to the hourly incident workflow.
- [ ] Retire the temporary commercial-domain fallback after verification.

## Session log
- **2026-07-24** — Created from governance template.
