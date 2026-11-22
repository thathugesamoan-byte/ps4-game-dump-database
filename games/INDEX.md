# ItemzFlow game dumping — quick decision list

**Reviewed:** 2026-11-21. **Games:** 18. This is the first page to consult before dumping. Click a game for its source links, caveats, and repackaging notes. For coding agents: follow [research protocol](../docs/RESEARCH-PROTOCOL.md), then the linked guide.

## Read this first
- **Mode to try** = provisional recommendation, **not** a confirmed CUSA-specific success. `Dump All` is the generic starting point for standard base+patch installations, **not proof of the best method for every title**.
- **Documented successful dump** = direct evidence that ItemzFlow completed dumping this exact CUSA with the stated mode. **Not verified** means evidence is insufficient; it does not mean the game cannot be dumped.
- **Documented working backup** = source-backed PKG build, validation, PS4 installation and launch. A PKG file alone does not qualify.
- **Retail update** = whether to install a retail patch **before** dumping. **Unknown** means do not automatically update. Verify CUSA, firmware, patch dependencies, and title-specific success first.
- **Research needed** = Yes until a defensible, game-specific workflow and outcome are documented.

## All games

| Game | CUSA | ItemzFlow mode to try* | Update first? | Successful dump documented? | Working backup documented? | More research? |
|---|---|---|---|---|---|---|
| [Minecraft](CUSA00744.md) | `CUSA00744` | Dump All* | Conditional | **Not verified** | **Not verified** | **Yes** |
| [The Forest](CUSA10518.md) | `CUSA10518` | Dump Base Game Only* | Conditional | **Not verified** | **Not verified** | **Yes** |
| [Crash Bandicoot N. Sane Trilogy](CUSA07402.md) | `CUSA07402` | Separate base + patch* | Conditional; 1.07 candidate | **Not verified** | **Not verified** | **Yes** |
| [Jak 3](CUSA07841.md) | `CUSA07841` | Dump Base Game Only* | No verified update | **Not verified** | **Not verified** | **Yes** |
| [Days Gone](CUSA08966.md) | `CUSA08966` | Remaster Only if combined; else Dump All* | Conditional | **Not verified** | **Not verified** | **Yes** |
| [God of War](CUSA07408.md) | `CUSA07408` | Dump All* | Unknown | **Not verified** | **Not verified** | **Yes** |
| [Injustice 2](CUSA05462.md) | `CUSA05462` | Dump All* | Unknown | **Not verified** | **Not verified** | **Yes** |
| [Marvel's Spider-Man](CUSA02299.md) | `CUSA02299` | Dump All* | Unknown | **Not verified** | **Not verified** | **Yes** |
| [Call of Duty: Black Ops III](CUSA02290.md) | `CUSA02290` | Dump All* | Unknown | **Not verified** | **Not verified** | **Yes** |
| [Mortal Kombat X](CUSA00967.md) | `CUSA00967` | Dump All* | Unknown | **Not verified** | **Not verified** | **Yes** |
| [Far Cry 4](CUSA00496.md) | `CUSA00496` | Dump All* | Unknown | **Not verified** | **Not verified** | **Yes** |
| [Watch Dogs](CUSA00021.md) | `CUSA00021` | Dump All* | Unknown | **Not verified** | **Not verified** | **Yes** |
| [Assassin's Creed Valhalla](CUSA18522.md) | `CUSA18522` | Dump All* | Unknown | **Not verified** | **Not verified** | **Yes** |
| [Star Wars: Squadrons](CUSA15080.md) | `CUSA15080` | Dump All* | Unknown | **Not verified** | **Not verified** | **Yes** |
| [Watch Dogs: Legion](CUSA13115.md) | `CUSA13115` | Dump All* | Unknown | **Not verified** | **Not verified** | **Yes** |
| [Ghost of Tsushima](CUSA11456.md) | `CUSA11456` | Dump All* | Unknown | **Not verified** | **Not verified** | **Yes** |
| [Horizon Zero Dawn Complete Edition](CUSA10237.md) | `CUSA10237` | Dump All* | Unknown | **Not verified** | **Not verified** | **Yes** |
| [We Happy Few](CUSA09406.md) | `CUSA09406` | Dump All* | Unknown | **Not verified** | **Not verified** | **Yes** |

*All modes above are **provisional**. For **Days Gone**, `Dump Remaster Only` applies to a genuine combined/remaster package, **not** merely a game with “remastered” in its name. For **Jak 3**, PS2 Classic packaging remains unresolved.*

## How to use this list
1. Find the CUSA and open the game guide.
2. Read the **QUICK DECISION** at the top. If the retail-update decision is Unknown/Conditional, **do not install a patch solely on this guide's authority**.
3. If preserving DLC, investigate `Dump DLC Only` for content not loaded by `Dump All`. `Dump All + GP4FV` is a verification dump, not the default packaging GP4.
4. Do not treat a completed dump as a playable backup. Build and validate on a protected copy; any real console testing requires separate authorization.

## Evidence and next research priorities
- **0/18** have a documented, independently verified CUSA-specific ItemzFlow mode → build → install → launch chain in the currently reviewed material.
- **5/18** have useful historical local evidence (Minecraft, The Forest, Crash, Jak 3, Days Gone), but it does **not** prove the listed dumping mode.
- **Highest priority:** Days Gone (remaster/combined packaging), Jak 3 (PS2 Classic EMU_VER), The Forest (blocked image verification), Crash (patch 1.07 dependencies and trophy checks).
- **Remaining 14** also require game-specific successful dump evidence and retail update decisions; prioritize edition/DLC-heavy titles such as Valhalla, Black Ops III, Injustice 2, Ghost of Tsushima and Watch Dogs: Legion.
- **General sources:** [ConsoleMods dumping guide](https://consolemods.org/wiki/PS4:Ripping_PS4_Game_Backups), [ItemzFlow releases](https://github.com/LightningMods/Itemzflow/releases), [unified-fpkger](https://github.com/MangoScango/unified-fpkger). These describe capabilities, **not** successful tests of all listed games.


**Research sources and workflow:** [Five-step evidence-first source catalog](../docs/RESEARCH-SOURCES.md). Use this before adding or revising a game. Distinguish documented successful ItemzFlow dumping from PKG validation and real-PS4 installation/launch.

## Research update — 2026-11-21

- **Crash Bandicoot DLC:** [Firsthand Reddit report](https://www.reddit.com/r/ps4homebrew/comments/1wlif0k/query_regarding_ps4_dlcdumping_issues/) documents installed DLC **not detected by ItemzFlow**. It does **not** confirm CUSA07402 specifically, a working fix, or successful base dumping. See [Crash guide](CUSA07402.md).
- **All 18 games:** No newly established CUSA-specific successful ItemzFlow dump **with exact mode**, or independently verified dump → build → real-PS4 install/launch chain. Keep **Not verified** statuses.
- **General diagnostics:** Version-specific Sandbox/incomplete-dump reports and language-file issues are now catalogued in [RESEARCH-SOURCES.md](../docs/RESEARCH-SOURCES.md). These are troubleshooting leads, not reasons to label any listed game proven.


## Ranked methods and negative evidence

Follow [the evidence-based elimination workflow](../docs/ELIMINATION-WORKFLOW.md). For each game, distinguish **TRY FIRST**, **FALLBACK**, **AVOID** (with exact tested conditions), and **UNRESOLVED**. Lack of a documented success is **not** proof of failure. A failed packaging configuration must not be used to rule out an ItemzFlow dumping mode. Update the decision and source evidence after each relevant test or firsthand report.


## Evidence expansion — 2026-11-21 (upstream issues and retests)

- **God of War (CUSA07408):** [ItemzFlow issue #142](https://github.com/LightningMods/Itemzflow/issues/142) names the **game title** among examples of missing-language-data dump hangs, but does **not state CUSA07408**. [Open fix proposal #152](https://github.com/LightningMods/Itemzflow/pull/152) was contributor-tested on a **different CUSA**, so it is not a released or CUSA07408-verified workaround. See [guide](CUSA07408.md).
- **BO3 (CUSA02290):** A [firsthand disc-dump report](https://www.reddit.com/r/ps4homebrew/comments/1n2d982) indicates unexpectedly small output, but **does not establish CUSA, mode or successful remedy**. Treat as a completeness diagnostic, not a confirmed CUSA02290 failure. See [guide](CUSA02290.md).
- **General upstream findings:** [Directory-creation failure with local retest](https://github.com/LightningMods/Itemzflow/issues/140#issuecomment-6229539038), [small-DLC omission report](https://github.com/LightningMods/Itemzflow/issues/138), [patch-not-detected report](https://github.com/LightningMods/Itemzflow/issues/153), and [remaster packaging maintainer caveat](https://github.com/CyB1K/PS4-Fake-PKG-Tools-3.87/issues/3#issuecomment-1019483264) inform troubleshooting but **do not validate a dumping method for any of the 18 tracked CUSA IDs**. Full evidence notes in [sources](../docs/RESEARCH-SOURCES.md).
- **Status unchanged:** no newly proven exact-CUSA ItemzFlow dump or end-to-end working backup in this batch. All previous 18 success fields remain **Not verified**.

## Failure-first review coverage — 2026-11-21

**18/18 CUSA guides** now contain a scoped failure-first elimination review. This is a structured reclassification of **existing repository evidence**, not 18 new independent external investigations or console tests. The decision terms are [ELIMINATE / CONDITIONAL AVOID / CAUTION / UNTESTED](../docs/ELIMINATION-WORKFLOW.md). An absent failure report eliminates nothing.

| CUSA | Negative evidence currently recorded | Scope / action |
|---|---|---|
| [CUSA10518](CUSA10518.md) The Forest | Local encrypted-artifact and trophy image-verification errors | **CONDITIONAL AVOID:** same GP4/build candidate; no ItemzFlow mode eliminated |
| [CUSA07841](CUSA07841.md) Jak 3 | Local PS2 Classic build lost EMU_VER and failed static validation | **CONDITIONAL AVOID:** same builder/GP4 configuration |
| [CUSA08966](CUSA08966.md) Days Gone | Local base builder rejected remaster-marked source | **CONDITIONAL AVOID:** same builder mode and metadata combination |
| [CUSA07402](CUSA07402.md) Crash N. Sane Trilogy | Local patch GP4/trophy errors; title-level DLC detection failure reported without CUSA | **CONDITIONAL AVOID** unchanged patch build; **CAUTION** DLC detection |
| [CUSA07408](CUSA07408.md) God of War | Title-level missing-language-data hang; CUSA unspecified | **CAUTION**, not a CUSA07408 exclusion |
| [CUSA02290](CUSA02290.md) Black Ops III | Title-level unexpectedly small dump report; CUSA/mode unknown | **CAUTION**, verify completeness |
| [CUSA00744](CUSA00744.md) Minecraft | No matching failed ItemzFlow mode documented | **UNTESTED**, retain provisional choices |
| Other 11 guides | No matching failed mode documented in existing research | **UNTESTED**, retain provisional choices |

**General packaging restriction:** GP4FV verification projects are not default packaging GP4s; this does not imply `Dump All` itself fails. All 18 game-specific end-to-end success fields remain **Not verified**. The next research pass must independently inspect original reports, follow-up fixes and exact-CUSA conditions before promoting a caution to an exclusion.

## Supplementary-source audit integration — 2026-11-21

The [source catalog](../docs/RESEARCH-SOURCES.md#targeted-supplementary-source-audit--2026-11-21) now includes Al-Azif dumper-testing, OpenOrbis LibOrbisPkg, PKG-format references, ShadPKG, shadPS4 diagnostics and the official ItemzFlow Discord as a **not-yet-audited message channel**. [LibOrbisPkg #26](https://github.com/OpenOrbis/LibOrbisPkg/issues/26) (PlayGo build exception) and [#7](https://github.com/OpenOrbis/LibOrbisPkg/issues/7) (sc0 duplication) are **general builder-stage leads**, not new exact-CUSA exclusions. God of War's missing-language warning gains general upstream context; The Forest/Crash trophy and packaging issues gain investigation references. **No recommendation was promoted to proven and no console-install success status changed.**
