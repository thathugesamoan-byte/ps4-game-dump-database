# Evidence-based elimination: choose what to try first

**Purpose:** Minimize unnecessary real-console dumping, transfers, and packaging attempts across [the 18-game index](../games/INDEX.md). Do not require an official or fully proven workflow to make a useful recommendation. Do **not** equate absence of success evidence with evidence of failure.

## Simple decision sequence

1. **Classify installed content:** CUSA, edition, installed retail update, DLC, firmware, and package type. Do not update just because a newer patch exists.
2. **Rule out incompatible options:** Use source-backed limitations and actual failed tests. Record the **exact scope** (CUSA, game/patch version, ItemzFlow mode/version, builder/version, error). A builder failure cannot eliminate a dumping mode.
3. **Rank remaining options:** **TRY FIRST** (best-supported practical choice), **FALLBACK** (reasonable alternative), **AVOID** (documented failure/inapplicable under specified conditions), **UNRESOLVED** (not enough evidence). Generic defaults are weaker than CUSA-specific user reports and actual logs.
4. **Minimize work:** Favor a single capture if it preserves required components, but prefer separate base/patch dumps when a combined dump is known to create unpackageable inputs. Use `Dump DLC Only` for independently preserved DLC. Do not use `Dump all + GP4FV` as a packaging shortcut.
5. **Test one variable at a time:** First verify source completeness; then packaging GP4; then PKG build; then static validation; finally PS4 installation/launch when separately authorized. Record results and update the guide/index. Stop repeating an unchanged failing combination.

## What counts as elimination?

| Evidence | Can eliminate | Cannot eliminate |
|---|---|---|
| ItemzFlow reports no DLC and exported files are missing | That DLC-capture path under the reported conditions | Base dumping, other versions or DLC methods |
| `img_verify` fails on forbidden files/trophy | That exact GP4/build candidate until corrected | All dumps of the game |
| CyB1K base builder rejects `REMASTER_TYPE` | Base-mode packaging of that remaster-marked source with that builder | Remaster-aware packaging or other retail sources |
| Builder strips `EMU_VER` and validator rejects output | That specific PS2 Classic packaging configuration | All PS2 Classic dump methods |
| A retail patch is unavailable or incompatible | That exact patch/version/firmware combination | Base-only dump or another compatible patch |
| No reports found | **Nothing** | Never label a method failed solely for lack of reports |

## User-facing decision card required in every guide

- **TRY FIRST:** exact ItemzFlow mode; whether to update before dumping; short reason; confidence (High/Medium/Low).
- **FALLBACK:** next practical mode and when to switch.
- **AVOID:** only methods with a reason; tag each **Confirmed incompatible**, **Documented failure**, **Not applicable**, or **Unverified risk**. Unverified risk is *not* a proven failure.
- **DUMP EVIDENCE:** Success documented / Failure documented / Not verified.
- **BACKUP EVIDENCE:** Console install+launch documented / Build only / Validation failure / Not verified.
- **STOP/CHANGE TRIGGER:** concrete error or missing content that justifies switching.
- **SOURCE:** direct permalink and date for any documented failure/success.

## Initial evidence-informed prioritization (not proven recipes)

| Game | Try first | Fallback | Avoid or caution |
|---|---|---|---|
| Minecraft | Dump All if patch needed; otherwise base-only | Separate base and patch | No known title-specific failure of Dump All |
| The Forest | Base-only to isolate base source | Dump All if patch preservation needed | **Do not reuse the existing BLOCKED GP4/build candidate unchanged** (five encrypted artifacts and trophy error) |
| Crash N. Sane Trilogy | Separate base-only and patch-only for clear package inputs | Dump All if component outputs are distinct | **Do not assume Dump DLC Only succeeds**; user report says DLC not detected, CUSA unspecified |
| Jak 3 | Dump Base Game Only | No validated alternate mode | **Avoid repeating the same CyB1K build that strips EMU_VER** |
| Days Gone | Dump Remaster Only **if combined/remaster package confirmed**; otherwise Dump All | Separate base and patch for standard retail install | **Avoid CyB1K base mode on the observed REMASTER_TYPE=1/APP_VER=01.81 input** |
| Other 13 | Dump All for base+installed patch; base-only if no patch needed | Separate base and patch | No CUSA-specific failures established; no exclusions based solely on silence |

**Note:** The “Other 13” count covers the 18-game list minus the five historical local-evidence games. All entries are practical starting hypotheses, not proven successful methods.

## Source priority

1. Exact CUSA + same patch/mode/builder: reproducible successes and failures with logs, screenshots or follow-up PS4 install/launch.
2. Exact game (different CUSA): useful lead, **not automatic compatibility**.
3. Upstream developer issue, release or implementation demonstrating a general limitation.
4. Reddit first-person account with precise conditions and follow-up; corroboration raises confidence.
5. General tutorials and inference: lower confidence; never present as confirmed failure or success.

For source catalog and search sequence, use [RESEARCH-SOURCES.md](RESEARCH-SOURCES.md). Record negative results only after actually testing a configuration or finding a specific firsthand failure. Do not turn an unanswered search into an “avoid.”

## Mandatory failure-first investigation and elimination ledger

A complete reinstall is **not required** to make progress. A documented failure at any stage can prevent repeating an unchanged attempt, provided its scope is preserved.

1. **Search for negative evidence before recommending a method.** Search the exact CUSA and title, then the relevant mode, update, builder, error string, upstream issues, follow-up comments, and known fixes. Include reports that end at dump, GP4, build, validation, install, or launch.
2. **Record each distinct attempt** using the table below. Preserve original report date, direct permalink, tool/build versions, source type, and the actual observed result. Unknown fields stay `Unknown`; never fill them from a different report.
3. **Check whether the failure is still applicable.** Compare CUSA/edition, source type, retail update, firmware, ItemzFlow version and mode, builder and GP4 configuration. Check later comments, fixes, releases, and successful retests. A fixed bug is a historical warning, not a permanent exclusion.
4. **Apply the narrowest defensible decision:** `ELIMINATE — matching conditions` for a reproduced or sufficiently documented incompatibility; `CONDITIONAL AVOID` for a firsthand failure whose conditions match but independent corroboration is absent; `CAUTION` for different-CUSA, general, disputed or version-unknown reports; `UNTESTED` when no applicable test exists. Do not turn an anecdote into a universal prohibition.
5. **Rank surviving choices independently by stage.** An extraction failure may eliminate that extraction configuration, not all builders. A GP4 or PKG failure may eliminate that build configuration, not the underlying dump. Select the lowest-work remaining candidate and an error-triggered fallback; label it `PROVISIONAL` unless a higher stage is actually demonstrated.
6. **Stop and revise** when the same unchanged configuration has already failed under matching conditions. Only retry if a meaningful variable or documented fix changes; record what changed and the resulting stage.

### Failure / exclusion ledger (repeat rows as necessary)

| Source and report date | Applicability (exact CUSA / same title / general) | Stage and tested configuration | Observed failure and evidence quality | Later fix or retest | Decision, scope and next alternative |
|---|---|---|---|---|---|
| Direct permalink | CUSA, edition, retail patch, firmware | Tool versions, mode, builder/GP4 | Exact error, log or firsthand account | Verified release, local patch, unresolved or unknown | ELIMINATE / CONDITIONAL AVOID / CAUTION / UNTESTED; precise conditions and fallback |

**Decision rules:** `ELIMINATE` means do not repeat **that combination**; it never means the entire game is undumpable. `CONDITIONAL AVOID` means avoid the matching configuration while seeking confirmation. `CAUTION` is not an exclusion. `UNTESTED` is not failure. A single report can support a scoped operational warning but must remain identified as single-reporter evidence. A proposed PR or locally modified build is not a released fix.

### Research completion standard

A game guide may be **decision-useful without a proven reinstall** if it identifies the best remaining candidate, the exact known dead ends, applicability and sources, a concrete fallback trigger, and missing validation. Do not claim a method was exhaustively eliminated merely because searches returned nothing. Update the index when a new failure changes the recommended method or fallback.
