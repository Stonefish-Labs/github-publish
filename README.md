# GitHub Publish

Publish projects to GitHub cleanly. Use when creating new repos, initializing git, setting up .gitignore, adding topics, or pushing to GitHub. Handles common setup tasks for clean, organized repositories.

## Overview

This skill guides agents through publishing projects to GitHub with proper setup — .gitignore, README, topics, and clean commits. It covers authentication, authorship rules, and the full workflow from local init to repo creation and topic tagging.

## Installation

Install via the agent marketplace CLI:

```bash
marketplace install github-publish
```

Or manually copy the `skills/github-publish/` folder into your agent's config directory:

```bash
# Cursor
cp -r skills/github-publish ~/.cursor/skills/

# Claude Code
cp -r skills/github-publish ~/.claude/skills/

# Codex
cp -r skills/github-publish ~/.codex/skills/

# Roo
cp -r skills/github-publish ~/.roo/skills/
```

## Usage

**Trigger phrases:** "publish to GitHub", "create a new repo", "push to GitHub", "add .gitignore", "add topics to repo"

The skill walks through:
1. Ensuring .gitignore exists (with templates for Python, Node, Rust)
2. Ensuring README exists
3. Verifying git identity before init
4. Creating the GitHub repo via `gh repo create`
5. Adding discoverability topics

## Structure

```
github-publish/
├── README.md
├── LICENSE
├── .gitignore
└── skills/
    └── github-publish/
        ├── SKILL.md
        └── references/
            ├── gitignore-templates.md
            └── topics-reference.md
```

## License

MIT
