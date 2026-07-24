# AGENTS.md — cap-ferret-fire-watch-public

## Ownership

**Model ownership policy:** shared by default across agents  
**Human owner:** repository owner

## Canonical Repo Policy

- GitHub is the definitive source of truth for this repo.
- Work only from the current machine's approved canonical clone.
- Before editing, confirm `pwd` is that clone and `git remote get-url origin` matches the expected GitHub remote.
- Do not use archived or duplicate local clones as active workspaces.

## Working Rules

- `AGENTS.md` is the canonical agent-facing instruction file for this repo.
- This is a deployment-only public repository. The private source project generates `docs/`; do not hand-edit generated site files here.
- Never add private operational details, credentials, household information, unpublished incident notes, or commercial branding.
- Keep the published dashboard marked `noindex`.
- Do not create a new `CLAUDE.md` for repo instructions. Move durable project context into `PROJECT.md`, `REFERENCE.md`, or `RUNBOOK.md` as appropriate.
- Default working style is trunk-based development; follow `ccn000/clphn-governance/TRUNK_BASED_DEVELOPMENT.md` unless this repo explicitly documents a narrower exception.
- Prefer agent-agnostic wording and file ownership rules over tool-specific instructions.
- Future commits may be blocked by installed governance hooks unless the commit message includes `Agent: codex` or `Agent: claude-code`.

## File Ownership Zones

| Zone | Owner | Notes |
|------|-------|-------|
| `PROJECT.md` | **SHARED** | Current state, architecture, and working context |
| `CHANGELOG.md` | **SHARED** | Append-only change log with rationale |
| `AGENTS.md` | **COORDINATED** | Shared operating rules for any coding agent |
| `docs/` | **GENERATED** | Published dashboard copied from the private source project |
