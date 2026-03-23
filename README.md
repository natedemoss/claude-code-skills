<div align="center">

[![Claude Code](https://img.shields.io/badge/Claude_Code-Skills-blueviolet?style=for-the-badge&logo=anthropic&logoColor=white)](https://claude.ai/claude-code)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

# Claude Code Skills

**A collection of `/skills` for [Claude Code](https://claude.ai/claude-code).**

</div>

---

## Skills

| Skill | Command | Description |
|:------|:--------|:------------|
| [**Wrapped**](skills/wrapped/) | `/wrapped` | Spotify Wrapped-style interactive recap of your Claude Code usage stats |
| [**Token Surgeon**](skills/token-surgeon/) | `/token-surgeon` | Audit prompts against 10 named waste patterns, score efficiency, and cut tokens |
| [**Onboarding**](skills/onboarding/) | `/onboarding` | Generate a comprehensive onboarding guide for any codebase |

---

## Installation

### Install all skills at once

```bash
git clone https://github.com/natedemoss/claude-code-skills.git

# macOS / Linux
cp -r claude-code-skills/skills/wrapped ~/.claude/skills/wrapped
cp -r claude-code-skills/skills/token-surgeon ~/.claude/skills/token-surgeon
cp -r claude-code-skills/skills/onboarding ~/.claude/skills/onboarding

# Windows (PowerShell)
Copy-Item -Recurse claude-code-skills\skills\wrapped "$env:USERPROFILE\.claude\skills\wrapped"
Copy-Item -Recurse claude-code-skills\skills\token-surgeon "$env:USERPROFILE\.claude\skills\token-surgeon"
Copy-Item -Recurse claude-code-skills\skills\onboarding "$env:USERPROFILE\.claude\skills\onboarding"
```

### Install a single skill

```bash
# macOS / Linux — example for onboarding
cp -r claude-code-skills/skills/onboarding ~/.claude/skills/onboarding

# Windows (PowerShell)
Copy-Item -Recurse claude-code-skills\skills\onboarding "$env:USERPROFILE\.claude\skills\onboarding"
```

Restart Claude Code (or open a new session). All installed skills load automatically.

---

## Skill Details

### `/wrapped` — Claude Code Wrapped

Like Spotify Wrapped, but for your AI coding sessions. Reads your local Claude Code session data and generates a slide-by-slide terminal recap with charts, stats, and your developer archetype.

**Slides:** Year at a Glance · Tools You Loved · When You Code · Legendary Session · Your AI Fleet · Estimated Cost · Files You Couldn't Quit · Developer Archetype

→ [Full docs](skills/wrapped/README.md)

---

### `/token-surgeon` — Token Surgeon

Scans any prompt against 10 named waste patterns, quotes every offending line, scores efficiency from 1–10, and estimates recoverable tokens. Never rewrites until you confirm.

**Patterns:** Hedging Language · Role Throat-Clearing · Restated Instructions · Politeness Padding · Filler Affirmations · Dead Context · Redundant Formatting · Negation Bloat · Over-Specified Examples · Scope Creep Instructions

→ [Full docs](skills/token-surgeon/README.md)

---

### `/onboarding` — Onboarding Guide Generator

Deep-analyzes any codebase and produces a structured Markdown onboarding guide. Every line is tailored to the specific project — no generic boilerplate.

**Sections:** What Is This · Tech Stack · Project Structure · How to Get Started · Architecture Overview · Key Files to Read First · Domain Knowledge · Running Tests · Common Gotchas · Where to Go Next

→ [Full docs](skills/onboarding/README.md)

---

<div align="center">

Made for [Claude Code](https://claude.ai/claude-code).

</div>
