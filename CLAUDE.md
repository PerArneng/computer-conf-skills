# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Purpose

This repository contains Claude Code skills for installing software and configuring computers. Skills are markdown files that provide step-by-step instructions for machine setup tasks.

## Repository Structure

```
.claude/skills/
├── conf-skill-creator/SKILL.md       # Meta-skill for creating new skills
├── configure-claude-code/SKILL.md    # Claude Code settings configuration
└── manage-zellij-installation/SKILL.md  # Zellij terminal multiplexer
```

## Creating New Skills

Use the `/conf-skill-creator` skill when asked to create installation or configuration skills. Each skill must include:

- **Frontmatter**: `name` and `description` in YAML format
- **Prerequisites**: Required dependencies
- **Installation**: Step-by-step commands
- **Verify**: How to confirm success
- **Update**: How to upgrade to newer versions
- **Uninstall**: How to remove software and clean up configs

## Conventions

- One skill per tool/configuration
- Use Homebrew on macOS, apt on Debian/Ubuntu
- Prefer idempotent commands that can safely re-run
- Include rollback steps for complex changes
