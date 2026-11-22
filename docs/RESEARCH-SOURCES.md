# Research sources and repeatable game-guide workflow

**Scope:** The 18 CUSA game guides in [INDEX.md](../games/INDEX.md). **Research baseline:** 2026-11-21. **Goal:** choose the simplest *evidence-supported* ItemzFlow dumping setting and compatible repackaging method. **No automatic downloads, builds, console actions, or source edits.**

## Five-step workflow (user and agent)

1. **Identify:** Verify CUSA, title, edition, region/content ID, package category (gd/gp/gdo/remaster), installed update, DLC and firmware. Check [SerialStation](https://serialstation.com/), [OrbisPatches](https://orbispatches.com/), [PSDevWiki](https://www.psdevwiki.com/ps4/) and official release notes. These establish metadata, **not successful dumping**.
2. **Find real reports:** Search exact `"CUSA12345"` and game title with `ItemzFlow dump`, `Dump All`, `patch`, `GP4`, `repack`, `trophy`, `install`, `launch`, and error text across [ItemzFlow issues](https://github.com/LightningMods/Itemzflow/issues), [Reddit r/ps4homebrew](https://www.reddit.com/r/ps4homebrew/), [ConsoleMods](https://consolemods.org/wiki/PS4:Ripping_PS4_Game_Backups), and tool issues. Prefer first-person reports with exact mode/version/logs and follow-up confirmation; a question, vote, or unsourced claim is **not success evidence**.
3. **Cross-check implementation:** Compare the six ItemzFlow modes against upstream code, release notes, and known limitations. Check [ItemzFlow](https://github.com/LightningMods/Itemzflow), [playstation-tools fpkg](https://github.com/Daaboulex/playstation-tools/blob/main/docs/fpkg.md), [unified-fpkger](https://github.com/MangoScango/unified-fpkger), [hippie68 ftpdump](https://github.com/hippie68/ftpdump), and [hippie68 ps4-ftp](https://github.com/hippie68/ps4-ftp). Alternatives help diagnose limitations; **do not silently replace ItemzFlow** as the recommended dumper.
4. **Check packaging:** Consult [CyB1K tools / ConsoleMods](https://consolemods.org/wiki/PS4:Ripping_PS4_Game_Backups), [LibOrbisPkg](https://github.com/maxton/LibOrbisPkg), [PS4PKGTool](https://github.com/pearlxcore/PS4PKGTool), [Orbis](https://github.com/Antti/orbis), and [unified-fpkger](https://github.com/MangoScango/unified-fpkger). Identify exact builder/version, base/patch/combined/DLC relationships, GP4 exclusions, keystone, trophy, PlayGo, verification and console outcomes. **PC validation or shadPS4 launch does not equal PS4 console launch.**
5. **Record the decision:** Update the individual game guide and [INDEX.md](../games/INDEX.md) with the exact mode, whether retail updating is advised and to which version, whether a successful dump is *documented*, whether a working reinstall is *documented*, research date, strongest direct source, caveats and next unresolved test. **No proof → UNPROVEN / NOT VERIFIED**, not failure. Prefer one method only when evidence supports it.

## Research source catalog

| Source | Use | Evidence limitations |
|---|---|---|
| [ItemzFlow code, releases, issues](https://github.com/LightningMods/Itemzflow) | Mode behavior, bug fixes, sandbox prompts, logs, version regressions | General code is not game-specific success |
| [ConsoleMods dumping guide](https://consolemods.org/wiki/PS4:Ripping_PS4_Game_Backups) | ItemzFlow, GP4, trophy, patch packaging procedures | General reference |
| [playstation-tools fpkg](https://github.com/Daaboulex/playstation-tools/blob/main/docs/fpkg.md) | ItemzFlow .dumping marker, ELF signing, GP4 filtering, LibOrbisPkg, PlayGo hash issue | Linux base gd workflow; **does not merge patch folders** |
| [unified-fpkger](https://github.com/MangoScango/unified-fpkger) | FTP/PFS dumping, incomplete PlayGo, unified app+patch, remaster-style builder, DLC | Alternative implementation, not proof for a CUSA |
| [hippie68 ftpdump](https://github.com/hippie68/ftpdump) | Network dump alternative, trophy handling, remaster handling, troubleshooting | Requires compatible FTP payload; alternative, not ItemzFlow success |
| [PS4PKGTool](https://github.com/pearlxcore/PS4PKGTool) | PKG metadata, update pairing, validation, experimental merge/build | **OrbisPkgTool-generated packages not tested on jailbroken PS4** per maintainer |
| [Antti/orbis](https://github.com/Antti/orbis) | Read-only PKG metadata/integrity, full-file update handling, delta restrictions | No proof of console install/launch |
| [Axekinn/ps4-scraper](https://github.com/Axekinn/ps4-scraper) | CUSA lookup and Sony retail update metadata | Third-party scraper; verify against official data; not dumping proof |
| [SerialStation](https://serialstation.com/), [OrbisPatches](https://orbispatches.com/), [PSDevWiki](https://www.psdevwiki.com/ps4/) | Title ID, edition, patch history, firmware and format metadata | Metadata, not a best-method endorsement |
| [Reddit r/ps4homebrew](https://www.reddit.com/r/ps4homebrew/) | First-hand results, screenshots, version-specific failures, workarounds | User reports are unverified until corroborated; cite permalink and date |
| [Reddit ItemzFlow sandbox issue report](https://www.reddit.com/r/ps4homebrew/comments/1qwcmay/itemzflow_not_dumping_games_correctly_solution/) | User reports tiny/incomplete dumps fixed by declining Sandbox prompt; potential diagnostic | Anecdotal, version-specific; **not universal advice**; trace linked GitHub issue |

## Evidence labels (keep separate)

- **DUMP PROVEN:** exact CUSA + ItemzFlow version/mode + documented completed dump, with corroborating log/files/verification or reproducible firsthand evidence. This **does not** mean PKG works.
- **PKG BUILT:** actual package emitted; no install claim.
- **PKG VALIDATED:** independent package validation passed; no install claim.
- **CONSOLE PROVEN:** exact output installed **and launched on a real PS4**, with version/firmware and reproducible evidence. Prefer independent confirmation.
- **UNPROVEN:** sources do not establish the claimed stage. **FAILED:** a documented test of the exact stage failed. **UNKNOWN:** insufficient evidence even to classify the attempt.
- For multiple reports, distinguish **single user report**, **corroborated reports**, **developer test**, and **local operator report**. Do not inflate an anecdote to independent proof.

## Source record for every claim

Use this compact format in each game guide:

`Source URL | accessed date | CUSA/edition | tool + version | ItemzFlow mode | retail patch | packaging tool + version | observed stage | exact outcome/error | evidence type | limitations`

**Reddit rules:** cite original thread/comment permalink, date, and actual reported result; inspect replies for retractions, fixes and subsequent install results. Do not treat recommendations without testing as completed tests. Never invent a missing mode or version.

**Stop conditions:** If exact CUSA evidence is missing, say **NO PROVEN BEST METHOD** and give only a clearly labeled provisional candidate. Never treat newer retail updates, a successful dump, a completed build, emulator results, or tool feature lists as console-tested success.

**Safety:** Research and documentation are read-only relative to the user's hardware and game files. Do not download or distribute copyrighted games, defeat validation, change SFO identity to force builds, execute payloads, or merge to main without separate authorization.

## New community troubleshooting evidence — 2026-11-21

| Original report | Observed outcome | Classification / scope |
|---|---|---|
| [Crash N. Sane Trilogy DLC not detected (2026-09-20)](https://www.reddit.com/r/ps4homebrew/comments/1wlif0k/query_regarding_ps4_dlcdumping_issues/) | User reports installed/playable Crash DLC not shown by ItemzFlow and no expected `-ac` mount | **CUSA not stated in thread; Crash title-specific DLC failure, not proven fix or base dump** |
| [ItemzFlow sandbox issue (2026-02-05)](https://www.reddit.com/r/ps4homebrew/comments/1qwcmay/itemzflow_not_dumping_games_correctly_solution/) | User reports MB-sized dumps, then successful dump after declining Sandbox prompt | General anecdote; check version and whether prompt exists |
| [ItemzFlow incomplete dump thread (2025–2026)](https://www.reddit.com/r/ps4homebrew/comments/1msz4q2/itemzflow_manager_not_dumping_the_full_game/) | Several firsthand incomplete-dump reports; one follow-up reports ItemzFlow 1.08 removed Sandbox prompt and produced installable packages | General, not one of the 18 CUSA-specific proven methods |
| [Bloodborne redump success (2026-03-02)](https://www.reddit.com/r/ps4homebrew/comments/1rhyarr/help_creating_bloodborne_pkg/) | User reports failed tiny dump followed by 29 GB dump and working PKG after declining Sandbox | Different game; supports completeness check only |
| [Spider-Man Miles Morales missing language data (2025-12-10)](https://www.reddit.com/r/ps4homebrew/comments/1pizpvb/help_dumping_a_game/) | User reports update dump stuck until required language data was installed | **CUSA20176, not Spider-Man CUSA02299**; diagnostic lead only |
| [ItemzFlow missing app.pkg report (2026-03-19)](https://www.reddit.com/r/ps4homebrew/comments/1rygazx/itemzflow_dumper_problem/) | User reported dump issues and later claimed disabling background PKG installation fixed them | General anecdote; no CUSA-specific validation |

**Diagnostic checklist before packaging:** check ItemzFlow version; review full dump log for incomplete/missing files; compare expected size and file count; verify any `.dumping` or completion markers are not substitutes for file integrity; check game language-data installation and DLC visibility where relevant; treat Sandbox guidance as **version-dependent**, not a blanket instruction. **Do not rewrite or bypass metadata/validation.**
