# Heardly Book Skills 🧠

Executable AI skill toolkits for 100+ books — one skill per book.
Each skill is a complete, AI-ready toolkit that can be used by any compatible agent.

## Compatible With

This repository supports **two distribution channels**:

- **ClawHub** (`_meta.json`) — Publish to the official OpenClaw skill registry at [clawhub.ai](https://clawhub.ai/heardlyapp)
- **agentskills.io / Open Standard** (`SKILL.md` frontmatter) — Compatible with Hermes Skills Hub, LobeHub, theskills.sh, and other agent skill markets

## Quick Start

```bash
# Clone the repo
git clone https://github.com/heardlyapp/book-skills.git

# For OpenClaw users — symlink to workspace
ln -s $(pwd)/book-skills/skills/* ~/.openclaw/workspace/skills/

# Or install individual skills from ClawHub
openclaw skills install atomic-habits
```

## Structure

```
book-skills/
├── index.json           ← Searchable skill index (100+ entries)
├── skills/
│   ├── atomic-habits/   ← One directory per book
│   │   ├── SKILL.md     ← AI-executable toolkit with YAML frontmatter
│   │   ├── _meta.json   ← ClawHub metadata (publisher, homepage)
│   │   └── references/  ← 5 reference files with book cases
│   ├── nonviolent-communication/
│   └── ... (100+ skills)
└── README.md
```

## Skill Format (agentskills.io Compatible)

Each `SKILL.md` includes standard YAML frontmatter:

```yaml
---
name: atomic-habits
description: James Clear's Atomic Habits — an executable toolkit...
version: 1.0.0
license: MIT
tags: [habits, self-improvement, behavior-change]
---
```

## Published Skills

| # | Skill | ClawHub | Tags |
|---|-------|---------|------|
| 1 | atomic-habits | [View](https://clawhub.ai/heardlyapp/atomic-habits) | habits, self-improvement |
| 2 | nonviolent-communication | [View](https://clawhub.ai/heardlyapp/nonviolent-communication) | communication, empathy |
| ... | 100+ skills | [View all](https://clawhub.ai/heardlyapp) | |

## Source

Powered by [Heardly App](https://www.heard.ly) — turning books into knowledge you can Listen and Execute.

All skills are MIT licensed.
