# GitHub Helper — Claude Code Skill

A Claude Code skill that helps non-technical users work safely with GitHub repositories. It provides guardrails, plain-language explanations, and workspace isolation to prevent common mistakes.

## What it does

- **Prevents dangerous actions** — blocks pushes to main/master, force-pushes, and silent branch switching
- **Isolates tasks** — each piece of work gets its own workspace so changes never get mixed up
- **Speaks plain English** — translates all git jargon into simple language
- **Manages context switching** — always asks before switching between tasks, never assumes
- **Audits on startup** — checks for in-progress work from previous sessions
- **Auto-updates** — checks for the latest version at the start of each session

## Installation

Tell Claude Code:

> Install the github-helper skill from https://github.com/CurtainWorld/github-helper

Claude will:
1. Clone this repo to `~/.claude/skills/github-helper/`
2. Add a reference to your global `~/.claude/CLAUDE.md` so the skill loads automatically
3. At the start of each session, Claude pulls the latest version

### Manual installation

```bash
# Clone the skill
git clone https://github.com/CurtainWorld/github-helper.git ~/.claude/skills/github-helper

# Add to your global CLAUDE.md (create the file if it doesn't exist)
echo '' >> ~/.claude/CLAUDE.md
echo '## GitHub Helper Skill' >> ~/.claude/CLAUDE.md
echo 'At the start of every session, run `git -C ~/.claude/skills/github-helper pull --quiet` to check for updates.' >> ~/.claude/CLAUDE.md
echo 'Then read and follow ALL instructions in `~/.claude/skills/github-helper/github-helper.md`.' >> ~/.claude/CLAUDE.md
```

## Updating

Updates are automatic. When the skill is updated in this repo, each user's Claude will pull the latest version at the start of their next session.

## Maintained by

Curtain World IT
