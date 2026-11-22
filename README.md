# PS4 Game Dump Research Database

A community-driven, evidence-based research database documenting the most reliable methods for dumping, repackaging, and preserving **legally owned** PlayStation 4 games using tools such as [ItemzFlow](https://github.com/LightningMods/Itemzflow).

**Start here:** Browse the **[18-Game Quick Decision Index](games/INDEX.md)** to look up a title by CUSA ID.

---

## What this project is

Dumping and repackaging PS4 games involves significant trial and error across ItemzFlow dumping modes, retail updates, DLC, PS2 Classics, and remaster/combined packages. This repository reduces unnecessary trial and error by collecting **documented successes, failures, community reports, and evidence-based recommendations** organized by CUSA ID.

### What it provides

- **Game-specific guides organized by CUSA ID** ([games/INDEX.md](games/INDEX.md)).
- **Recommended ItemzFlow dumping modes** (`Dump All`, `Dump Base Game Only`, `Dump Patch Only`, `Dump Remaster Only`, `Dump DLC Only`, and why `Dump All + GP4FV` is not a default packaging GP4).
- **Retail update considerations** (whether updating before dumping helps or hurts, and why newest is not automatically best).
- **Recommended repackaging workflows** (GP4 structure, base/patch/remaster relationships, validation notes).
- **Documented successful and unsuccessful attempts** so users do not repeat known-failing combinations.
- **Known incompatibilities and troubleshooting** with direct source references.
- **Community-submitted findings** clearly labeled by evidence level.

### What it does NOT provide

- **No pirated games, downloadable PKG files, or game dumps.**
- **No copyrighted game files, keys, or proprietary binaries.**
- **No guarantees** that every documented method will work on every console, firmware, or edition.
- **No instructions for obtaining games without authorization.**

> **Lawful preservation notice:** This database is intended strictly for lawful personal preservation, backup, and technical research of games you legally own on consoles you own, subject to applicable laws in your jurisdiction.

---

## Evidence-based recommendations

Every game guide separates dumping, repackaging, static validation, and real PS4 console testing, and ranks methods into four categories (see [docs/ELIMINATION-WORKFLOW.md](docs/ELIMINATION-WORKFLOW.md)):

- **TRY FIRST:** Best-supported practical method to attempt first.
- **FALLBACK:** Reasonable alternative if the first option does not fit or hits a documented trigger.
- **AVOID:** Methods with documented failures or incompatibilities, always stating the exact tested conditions.
- **UNRESOLVED:** Methods lacking sufficient evidence.

**Core honesty rules:**
- Never classify an untested method as failed.
- Never describe a method as proven without supporting evidence.
- Dumping success, PKG build success, static validation, and actual PS4 installation/launch are tracked separately—a successful build is never proof of playability.
- Community reports are valuable even when independently unverified; they are always labeled accordingly.

---

## Repository structure

```text
ps4-game-dump-database/
├── README.md                         # Project overview (this file)
├── AGENTS.md                         # Rules for AI/coding agents researching or updating guides
├── CONTRIBUTING.md                   # How to submit reports, research requests, and PRs
├── CODE_OF_CONDUCT.md                # Community standards
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── game-report.yml           # Submit a dump, build, install, or failure report
│   │   └── research-request.yml      # Request research for a CUSA ID
│   └── PULL_REQUEST_TEMPLATE.md      # Checklist for documentation pull requests
├── games/
│   ├── INDEX.md                      # Quick decision table for all tracked games
│   ├── TEMPLATE.md                   # Standard game guide template
│   └── CUSAxxxxx.md                  # Individual CUSA-specific game guides
└── docs/
    ├── RESEARCH-PROTOCOL.md          # Mandatory research standards and evidence grades (A–E)
    ├── ELIMINATION-WORKFLOW.md       # TRY FIRST / FALLBACK / AVOID / UNRESOLVED decision process
    └── RESEARCH-SOURCES.md           # Five-step source catalog and community diagnostics
```

---

## Five-step research workflow

New guides and updates follow the five-step workflow documented in [docs/RESEARCH-SOURCES.md](docs/RESEARCH-SOURCES.md) and [docs/ELIMINATION-WORKFLOW.md](docs/ELIMINATION-WORKFLOW.md):

1. **Identify** the exact game, CUSA ID, edition, content ID, package category, and firmware context.
2. **Search** GitHub, Reddit (`r/ps4homebrew`), ConsoleMods, developer documentation, and PS4 metadata databases.
3. **Eliminate** methods with documented incompatibilities (recording exact tested conditions).
4. **Rank** remaining dumping and repackaging options (`TRY FIRST`, `FALLBACK`, `AVOID`, `UNRESOLVED`).
5. **Record** recommendations, direct source links, evidence grades, and unresolved questions.

---

## How to contribute

Real-world reports—both successes and failures—make this database useful for everyone. See **[CONTRIBUTING.md](CONTRIBUTING.md)** for full details:

- **Submit a game test report or workaround:** Open a **Game Report** issue.
- **Request research on a title:** Open a **Research Request** issue.
- **Add or update a guide directly:** Open a **Pull Request** following [games/TEMPLATE.md](games/TEMPLATE.md) and [docs/RESEARCH-PROTOCOL.md](docs/RESEARCH-PROTOCOL.md).

> **Privacy reminder:** Before posting logs or screenshots, remove personal information, usernames, local file paths, credentials, console identifiers, and any copyrighted game data.

---

## Attribution & Licensing

This repository's original documentation and game guides are licensed under **[Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE)** ([creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)).

External documentation and tools cited in this database retain their own licenses and copyrights, and no third-party source code or binaries are bundled here:

- **[ConsoleMods Wiki — Ripping PS4 Game Backups](https://consolemods.org/wiki/PS4:Ripping_PS4_Game_Backups)** ([CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)) — referenced and summarized for general ItemzFlow/GP4 procedures without implying endorsement.
- **[ItemzFlow](https://github.com/LightningMods/Itemzflow)**, **[LibOrbisPkg](https://github.com/maxton/LibOrbisPkg)**, **[unified-fpkger](https://github.com/MangoScango/unified-fpkger)**, **[OrbisPatches](https://orbispatches.com/)**, **[SerialStation](https://serialstation.com/)**, and **[PSDevWiki](https://www.psdevwiki.com/ps4/)** — referenced by URL for metadata and upstream tool behavior.
- **[CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)** — adapted from [Contributor Covenant](https://www.contributor-covenant.org/) principles (CC BY 4.0).
