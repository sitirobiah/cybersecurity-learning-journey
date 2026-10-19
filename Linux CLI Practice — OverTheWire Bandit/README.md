## Overview
This folder documents my beginner practice with Linux command-line tools through OverTheWire Bandit.

**Goal:** Learn how to navigate Linux, inspect files, understand permissions, use SSH, work with text and archives, and explore basic networking concepts.

## Folder Structure
- `01_Bandit_Level_Writeups/` — Short notes grouped by level.
- `02_Command_Reference/` — Quick explanations of useful commands.
- `03_Lessons_Learned.md` — Summary of the skills practiced.

## How to Use These Notes
Each level group includes the main idea, commands, and a short explanation. Commands may need small changes depending on the current directory or file names.

## Security Note
These notes intentionally do not include passwords, private keys, or other credentials. In a public portfolio, never publish challenge passwords or secret files.

## Progress
- [x] Practiced the Bandit levels covered in these notes
- [x] Reviewed common Linux CLI commands
- [ ] Continue practicing without step-by-step tutorials
"""
files["01_Bandit_Level_Writeups/README.md"] = r"""# Bandit Level Notes

The notes are grouped by related levels to keep them short and easy to review.

| File | Main topics |
|---|---|
| `01_Levels_00-05.md` | SSH, listing files, reading files, hidden files, unusual filenames |
| `02_Levels_06-10.md` | Finding files, permissions, searching text, file types, Base64 |
| `03_Levels_11-15.md` | ROT13, file inspection, compression and archives, SSH keys |
| `04_Levels_16-20.md` | Ports, TLS, comparing files, setuid |
| `05_Levels_21-25.md` | Cron jobs, scripts, networking, SSH keys and shell behavior |
| `06_Levels_26-Completed.md` | Restricted shells, reading files, final review |

**Learning approach:** Understand what each command does, why it is useful, and how to verify its output. These notes are summaries, not a replacement for the challenge instructions.
"""
