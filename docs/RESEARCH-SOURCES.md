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


## Upstream issue and retest findings — 2026-11-21

These findings are new diagnostic evidence, **not proof that the corresponding fix ships in a released ItemzFlow build**:

| Source (original date) | Observed stage and conditions | Operational decision |
|---|---|---|
| [ItemzFlow issue #142](https://github.com/LightningMods/Itemzflow/issues/142) (2026-09-28) | Firsthand report: PSN installations with absent optional language data can hang while dumping. God of War is named among affected games; **CUSA not specified**. | If stuck on a missing language file, inspect installation completeness and the dumper log before repeating the same dump or changing packaging. |
| [ItemzFlow PR #152](https://github.com/LightningMods/Itemzflow/pull/152) (2026-11-17; **open, unmerged as reviewed**) | Contributor-reported PS4 Pro test using a locally patched ItemzCore on **Destiny CUSA00568**: base and patch dumps finished after skipping absent language files, with selected file spot checks. No PKG build or console reinstall shown. | Technical lead for a missing-language hang; **not evidence that a released ItemzFlow version includes the fix**, and not a proven solution for God of War. |
| [ItemzFlow issue #140 and author's retest](https://github.com/LightningMods/Itemzflow/issues/140#issuecomment-6229539038) (2026-09-25 / 2026-10-17) | For **CUSA03877** patch extraction, directory-creation errors caused an incomplete dump; reporter says a locally changed recursive directory creation operation then completed the dump. | Treat `Unable to open/create output subdirectory` as a **dump-stage** failure; do not assume MMAP patches or an alternate PKG builder are the cause. The local modification is **not confirmed upstream**. |
| [ItemzFlow issue #138](https://github.com/LightningMods/Itemzflow/issues/138) (2026-08-20) | Firsthand **CUSA01054** small-DLC omission; reporter says a locally modified size check restored captured files. | Investigate small DLC omissions by content size and actual extracted files. Do not generalize this game-specific retest to Crash DLC. |
| [ItemzFlow issue #153](https://github.com/LightningMods/Itemzflow/issues/153) (2026-11-18) | Reporter states **Alien: Isolation CUSA00362** installed v1.04 but `Dump Patch Only` claims no installed patch. | `No patch` can be a detection issue, not proof the retail update does not exist. |
| [ItemzFlow issue #66](https://github.com/LightningMods/Itemzflow/issues/66) (2024-09-05) | User reports patch dumping appearing frozen after rejecting GP4 creation and instead uses separate base/patch dumps. | When progress is ambiguous, examine logs and component folders rather than assuming a completed or failed dump. |
| [CyB1K remaster builder issue #3 and maintainer comment](https://github.com/CyB1K/PS4-Fake-PKG-Tools-3.87/issues/3#issuecomment-1019483264) (2022-01-23) | Maintainer says remaster packages can be built manually but warns that subsequent patch construction is problematic. | Evaluate remaster-aware builders against **patchability** as well as build success; do not suggest falsifying metadata to force a regular base build. |

### Issue/PR verification checklist

Before promoting an issue report to a recommendation, inspect the **original body and follow-up comments**; for a proposed fix verify whether the PR was merged, which releases contain it, the game/CUSA tested, and the highest outcome stage demonstrated. In each guide mark `applies directly to this CUSA`, `same title, CUSA unknown`, or `general diagnostic only`. A locally patched build is not a released fix. Do not repeat identical source catalogs in every guide.

## Targeted supplementary-source audit — 2026-11-21

The following sources are **diagnostic references**, not evidence of a successful ItemzFlow dump or working reinstall for any of the 18 tracked CUSA IDs. Apply [scoped elimination rules](ELIMINATION-WORKFLOW.md): match stage, CUSA, versions, conditions, and later fixes before excluding a configuration.

| Source | Use in failure-first research | Evidence boundary |
|---|---|---|
| [Al-Azif dumper-testing](https://github.com/Al-Azif/dumper-testing) | Investigate incomplete installations, missing language/disc assets, dumper hangs, and historical implementation limitations | Upstream/general behavior; not CUSA07408 proof or proof a fix shipped in ItemzFlow |
| [OpenOrbis LibOrbisPkg](https://github.com/OpenOrbis/LibOrbisPkg) | Package builder implementation, metadata and GP4 handling; compare with [maxton LibOrbisPkg](https://github.com/maxton/LibOrbisPkg) | A builder capability is not a validated game-specific PKG |
| [LibOrbisPkg PKG Information](https://github.com/maxton/LibOrbisPkg/wiki/PKG-Information) | Inspect PKG structure and metadata when distinguishing extraction from build errors | Reference material, not a console test |
| [PSDevWiki PKG files](https://www.psdevwiki.com/ps4/PKG_files) | Package/PFS format diagnostics | Reference material, not game-specific outcome evidence |
| [ShadPKG repository](https://github.com/seregonwar/ShadPKG) | Alternative extraction/patch-layout diagnostics and logging | Patch omissions may be intentional; the previously suggested HOWWORKS.md path was not confirmed accessible |
| [shadPS4 wiki](https://github.com/shadps4-emu/shadPS4/wiki) | Emulator-oriented file/package diagnostics | Emulator compatibility is **never** proof of installation or launch on real PS4 hardware |
| [ItemzFlow official Discord invite](https://discord.gg/GvzDdx9GTc) | Locate firsthand troubleshooting reports and ask for logs/versions | Message history **not audited**; no Discord-specific claim verified |

### Concrete upstream packaging issues worth checking

| Direct report | Stage / reported failure | Scoped research action |
|---|---|---|
| [OpenOrbis LibOrbisPkg #26](https://github.com/OpenOrbis/LibOrbisPkg/issues/26) | Reported PlayGo chunk-hash allocation exception during package building | **Builder-stage diagnostic only.** Check exact builder revision, PlayGo metadata, comments and fixes before repeating matching build; does not eliminate ItemzFlow dumping |
| [OpenOrbis LibOrbisPkg #7](https://github.com/OpenOrbis/LibOrbisPkg/issues/7) | Reported duplicate `sc0` entries / trophy-metadata structure concerns | **Packaging/metadata diagnostic only.** Investigate sc0 layout and validation errors; does not establish cause of The Forest or Crash trophy errors |

### Implications for tracked games

- **God of War CUSA07408:** Al-Azif's general missing-language/disc-data behavior strengthens the *diagnostic hypothesis* from [ItemzFlow #142](https://github.com/LightningMods/Itemzflow/issues/142), but neither establishes a CUSA07408 failure or a released fix.
- **The Forest CUSA10518 / Crash CUSA07402:** The LibOrbisPkg issue reports supply builder-stage investigation leads for trophy/sc0 and PlayGo problems. They are **not confirmed fixes or matching-CUSA failures**.
- **Jak 3 CUSA07841 / Days Gone CUSA08966:** Package-format references may help identify builder compatibility, but no new metadata-preserving PS2 Classic build or remaster-aware CUSA08966 reinstall was demonstrated.
- **Other tracked titles:** No new exact-CUSA method exclusions established by this source audit. **All 18 console-reinstall success statuses remain Not verified.**

**Follow-up audit standard:** Read the issue body, comments, linked commits, closure and release notes before describing a workaround as fixed. Log the exact builder/version, error and stage. Do not copy an issue's diagnosis to a different game without matching evidence.
