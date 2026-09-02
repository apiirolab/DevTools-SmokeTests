---
name: format-check
description: Checks formatting of changed files before commit.
allowed-tools: read_file, grep, list_directory
---

# Format Check Skill

This skill validates the formatting of changed files and reports:
- Indentation and whitespace violations
- Line-length overruns
- Import ordering issues
