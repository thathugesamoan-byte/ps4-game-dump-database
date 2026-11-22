# AGENTS.md — Rules for Coding & Research Agents

This repository is a public, Markdown-only, evidence-based research database for dumping and repackaging legally owned PS4 games.

## Read order

1. [README.md](README.md) — project scope, non-goals, and lawful preservation notice.
2. [docs/RESEARCH-PROTOCOL.md](docs/RESEARCH-PROTOCOL.md) — mandatory research standards and evidence grades (A–E).
3. [docs/ELIMINATION-WORKFLOW.md](docs/ELIMINATION-WORKFLOW.md) — `TRY FIRST` / `FALLBACK` / `AVOID` / `UNRESOLVED` decision rules.
4. [docs/RESEARCH-SOURCES.md](docs/RESEARCH-SOURCES.md) — five-step research workflow and source catalog.
5. [games/INDEX.md](games/INDEX.md) and [games/TEMPLATE.md](games/TEMPLATE.md).

## Hard rules

- **Markdown documentation only.** Do not add code engines, scrapers, binaries, game files, PKG files, keys, or copyrighted assets.
- **One file per CUSA ID** under `games/CUSAxxxxx.md` (5-digit CUSA format). Always keep [games/INDEX.md](games/INDEX.md) in sync when adding or updating a game guide.
- **Every game guide must clearly distinguish:**
  - `TRY FIRST` — best-supported practical method.
  - `FALLBACK` — reasonable alternative.
  - `AVOID` — methods with documented failures or incompatibilities, with exact tested conditions.
  - `UNRESOLVED` — methods lacking sufficient evidence.
- **Keep workflow stages separate.** Track dumping success, PKG build success, independent static validation, and real PS4 console installation/launch separately. A successful dump or PKG build is never proof of playability.
- **Never fabricate or overstate evidence:**
  - Use `Unknown` or `Not verified` where information is missing.
  - Never classify an untested method as failed.
  - Never transfer success claims between different CUSA IDs without evidence.
  - Never claim research was performed unless the cited sources were actually inspected.
  - Label community reports clearly as community-reported (and note whether corroborated or unverified).
- **Never recommend unsafe shortcuts.** Do not recommend falsifying `APP_VER`, `REMASTER_TYPE`, `EMU_VER`, `CATEGORY`, or source identity to force a build, or bypassing package integrity checks.
- **Preserve privacy and public-release hygiene.** Never commit personal information, local machine paths, LAN IPs, credentials, console identifiers, private repository links, or piracy links.
- **Respect licensing and attribution.** Link to external projects and wikis (e.g., ConsoleMods CC BY 4.0, GitHub repos, Reddit permalinks) rather than copying third-party text or code.
