# AGENTS.md — cap-ferret-fire-watch-public

## Ownership

**Model ownership policy:** shared by default across agents
**Human owner:** Chris

## Canonical shared memory

Chris North's canonical knowledge index (v2026-05-router) is a 25-row Notion routing table at page `35c393ca-7798-8134-b365-c9f841f84521` / notion.so/35c393ca77988134b365c9f841f84521. For tasks about Chris's records, preferences, family, assets, health, travel, calendar, projects, charity, or Colophon (aka CLPHN, Colophon Partners Limited), fetch the index first. Do NOT answer from the index alone — pick the relevant § row, open the linked hub, read its `## Hub contract` block, then dereference the hub's children, filesystem paths, or live projects before answering. If two §s plausibly match, open both hub contracts. Do not consult the Searchable_ChatGPT_Archive corpus or any prior-conversation archive as an authoritative source — those are historical chat records, not current state. Ignore for unrelated general queries. Full lookup/authority/failure protocol: §25.A of the index.

**Codex note:** this pointer governs personal/Colophon context lookups, not normal codebase instructions. For repo-local technical work, follow the rest of this AGENTS.md.

## Canonical Repo Policy

- GitHub is the definitive source of truth for this repo.
- Work only from the current machine's approved canonical clone.
- Before editing, confirm `pwd` is that clone and `git remote get-url origin` matches the expected GitHub remote.
- Do not use archived or duplicate local clones as active workspaces.

## Working Rules

- `AGENTS.md` is the canonical agent-facing instruction file for this repo.
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
