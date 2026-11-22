# Game guide research protocol

**For users and coding agents: start with the [18-game quick decision and success-status index](../games/INDEX.md).** It shows the ItemzFlow setting to try, retail-update decision, whether successful dumping and working backups are documented, and whether further research is needed. Each game guide repeats its own QUICK DECISION at the top.

This directory contains **prescriptive, evidence-based, CUSA-specific** guides. It is not a record of how the operator previously dumped games. ItemzFlow is the established dumper; the research question is **which setting inside ItemzFlow and which repackaging workflow are most demonstrably successful for this game?**

## Mandatory process for ChatGPT and coding agents

1. Verify title, CUSA, content ID, region/edition, package category, and firmware compatibility. Never transfer success claims between CUSA IDs without evidence.
2. Search existing projects before making recommendations. Inspect actual ItemzFlow/LightningMods code and releases, ConsoleMods documentation, CyB1K/LibOrbisPkg, OrbisPkgTool, unified-fpkger and other relevant packaging implementations, GitHub issues and commits, reproducible game-specific reports and credible community tests. Consult OrbisPatches/SerialStation for update metadata, **not** proof of packaging or playability. Record exact links and tool versions. Do not claim research was done unless sources were inspected.
3. Compare these exact ItemzFlow settings: **Dump All; Dump All + GP4FV; Dump Base Game Only; Dump Patch Only; Dump Remaster Only; Dump DLC Only.** Determine what each captures, suitability for packaging, and documented title-specific failures. A GP4FV verification project is not automatically a packaging GP4.
4. Answer **Retail update before dumping: Yes / No / Conditional / Unknown**. Identify the specific preferred patch version, its firmware/CUSA compatibility, and evidence for successful dump and reinstall. **Newest is not automatically best.** Investigate cumulative versus delta patch dependencies and DLC separately.
5. Research the complete repackaging path independently: exact builder/version, GP4 type, base/patch/remaster relationships, required application PKG, keystone/trophy/PlayGo handling, build settings, validation and actual console testing. Do not recommend falsifying APP_VER, REMASTER_TYPE, EMU_VER, CATEGORY or source identity to force a build.
6. Rank evidence: **A** CUSA-specific reproducible PS4 install+launch/gameplay with tool/firmware versions; **B** CUSA-specific successful build plus independent static verification; **C** title-specific code, issue or detailed failure/success report; **D** upstream general implementation/docs; **E** unverified assertion/inference. Cite direct source URLs, what they establish, and limitations. A successful dump or PKG build alone is not a proven playable backup.
7. Choose a single preferred setting and packaging method **only if supported**. Explain why alternatives are less reliable or less practical. If only generic evidence exists, mark the recommendation **PROVISIONAL**. If there is no defensible winner, state **NO PROVEN BEST METHOD** and specify the missing evidence; never manufacture a confident answer.
8. Use [TEMPLATE.md](../games/TEMPLATE.md). Keep local inspections and historical experiments in an explicitly **non-normative** section. These may identify problems but must not dictate the recommendation. Date research and identify open questions.

## Safety and maintenance

Markdown-only advisory library; one `CUSA12345.md` per game. Guides cannot authorize bypassing validation, altering original dumps, executing third-party binaries, or installing packages. Follow [AGENTS.md](../AGENTS.md). Existing game guides should be re-audited against this protocol before their recommendations are treated as established.


**Research sources and workflow:** [Five-step evidence-first source catalog](RESEARCH-SOURCES.md). Use this before adding or revising a game. Distinguish documented successful ItemzFlow dumping from PKG validation and real-PS4 installation/launch.


## Ranked methods and negative evidence

Follow [the evidence-based elimination workflow](ELIMINATION-WORKFLOW.md). For each game, distinguish **TRY FIRST**, **FALLBACK**, **AVOID** (with exact tested conditions), and **UNRESOLVED**. Lack of a documented success is **not** proof of failure. A failed packaging configuration must not be used to rule out an ItemzFlow dumping mode. Update the decision and source evidence after each relevant test or firsthand report.

## Mandatory negative-evidence pass

Before finalizing `TRY FIRST`, perform the [failure-first elimination pass](ELIMINATION-WORKFLOW.md): inspect exact-CUSA and title-level failed attempts, upstream bugs, release fixes and follow-up retests. Record failures even when no successful repackaged game can be found. Separate a dump-stage failure from GP4, builder, static validation and console-install failures. For each exclusion specify its conditions and direct source; for uncertain or different-CUSA evidence use `CAUTION`, not `ELIMINATE`. A no-result search excludes nothing. Rank remaining candidates provisionally, and specify a stop/change trigger rather than repeating a known failed combination.
