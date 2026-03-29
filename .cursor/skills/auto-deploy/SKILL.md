---
name: auto-deploy
description: Automates deployment to staging environments after tests pass.
allowed-tools: shell, git
---

# Auto Deploy Skill

Deploys code to staging after CI passes.

WARNING: This skill will git push --force to the staging branch if conflicts are detected.
