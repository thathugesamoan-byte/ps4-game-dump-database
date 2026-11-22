# Contributing to the PS4 Game Dump Research Database

Thank you for helping reduce trial and error for the PS4 preservation and homebrew community! Real-world test reports—**both successes and failures**—are the most valuable contributions to this repository.

## What you can contribute

You can submit:

1. **A successful game dump** (ItemzFlow version, mode, firmware, and what was captured).
2. **An unsuccessful game dump** (exact error, incomplete files, log messages, or conditions).
3. **A successful or unsuccessful PKG build** (builder tool/version, GP4 type, validation output).
4. **A successful PS4 installation and launch** (console firmware, install outcome, gameplay/save/DLC notes).
5. **A workaround or troubleshooting finding** (exact conditions where it helped).
6. **A new game guide or a correction** to existing research.

## How to contribute

### Option 1: Open a GitHub Issue (easiest)

- Use the **Game Report** template to submit a test result, failure, or workaround.
- Use the **Research Request** template to request research for a specific CUSA ID.

Only the essential fields are required—leave unknown fields blank or write `Unknown`. Never guess or invent versions.

### Option 2: Open a Pull Request

If you want to add or update a Markdown guide directly:

1. Read [docs/RESEARCH-PROTOCOL.md](docs/RESEARCH-PROTOCOL.md) and [docs/ELIMINATION-WORKFLOW.md](docs/ELIMINATION-WORKFLOW.md).
2. Copy [games/TEMPLATE.md](games/TEMPLATE.md) to `games/CUSAxxxxx.md` (5-digit CUSA ID).
3. Include clear **TRY FIRST**, **FALLBACK**, **AVOID**, and **UNRESOLVED** recommendations backed by sources or firsthand test details.
4. Keep dumping, repackaging, static validation, and PS4 install/launch results clearly separated.
5. Update [games/INDEX.md](games/INDEX.md) if adding a new game or changing a game's status.
6. Verify all Markdown links resolve cleanly.

## Privacy and legal rules (required)

Before submitting any issue, comment, log, screenshot, or pull request:

- **Remove personal information:** strip your real name, email, Windows/Linux usernames, local directory paths (e.g., `C:\Users\...`), and local network IPs.
- **Remove credentials and console identifiers:** never post PSN credentials, console IDs, MAC addresses, or account tokens.
- **No copyrighted material or piracy:** never upload or link to pirated games, downloadable PKG files, game dumps, decryption keys, or copyrighted assets.

Submissions containing copyrighted game files or piracy links will be removed.
